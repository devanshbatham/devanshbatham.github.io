---
layout: post
toc: false
title: "PHP Tricks in Web CTF challenges"
categories: ["CTFs"]
tags: [ctf, web-security, php-security]
author:
  - Devansh Batham
---


![](https://cdn-images-1.medium.com/max/1166/0*OHr-8NUQfLrpykeh)

**Kon’nichiwa Folks**. I spent lot a time playing **CTFs** in last few years(2019), especially Web Challenges. I find them very fascinating as the thrill you get after capturing the flags cannot be described in words , That **adrenaline rush** is heaven for me. For me **CTFs** are the best way to practice,improve and test your hacking skills.

In this article I will be covering walkthroughs of some common/easy PHP based Web Challenges I solved during various CTFs and some simple tricks. This post is intended for absolute beginners.

# 1- A Casual Warmup

![](https://cdn-images-1.medium.com/max/2070/1*lqddvGiVtqzhdbwvFxKWPA.png)

Challenge Description gives us a very vital hint i.e. **HINT : see how preg_replace works**

It also says **Try to reach super_secret_function().** Now lets see the source code.

![index.php](https://cdn-images-1.medium.com/max/1494/1*19JnNOj9k8H17jOwDV_vIQ.png)

Lets breakdown the source code.

```
>  anime_is_bae: It is a GET parameter. we can supply its value as:

[`https://asm0d3us-ctf.herokuapp.com/Challenge1/index.php?anime_is_bae=[some](https://a`sm0d3us-ctf.herokuapp.com/Challenge1/index.php?anime_is_bae=)-text-here]

> your_entered_string : Our supplied input via anime_is_bae parameter is stored in this variable.

> intermediate_string : it contains a string ‘hellotherehooman’.

> final_string : It contains the result of the preg_replace function.

Then a final check is taking place, if final_string is equals to intermediate_string(i.e. `hellotherehooman` ) then the super_secret_function() is getting called and eventually we will get the flag.
```

Now lets focus on **preg_replace** function , it is taking three arguments `intermediate_string, '', your_entered_string` .

PHP’s manual for preg_replace can be found here : [https://www.php.net/manual/en/function.preg-replace.php](https://www.php.net/manual/en/function.preg-replace.php)

After reading the preg_replace function’s manual it is evident that our supplied input(or substring of our input) is getting compared to string hellotherehooman, and if they are equal then our supplied input is getting replaced with `nothing/blank/''` . Pretty neat? ugh. But in the final_string we need hellotherehooman , how it is possible when it is getting replaced with `nothing/blank/''` ?.

Lets run our code and test our crafted inputs.

![](https://cdn-images-1.medium.com/max/2462/1*bxeZM0d2vTkId72CygwKkg.png)

I supplied hellotherehooman as our input , hellotherehooman is getting compared with hellotherehooman and it is replaced with `''` .

Lets run our code with various test cases/Inputs

```
1 - when your_entered_string is : hello

$php main.php
Final String is : hello
No Success

2 - when your_entered_string is : hellothere

$php main.php
Final String is : hellothere
No Success

3 - when our supplied input is : hellotherehooman

$php main.php
Final String is :
No Success
```

Now we know how it is working , it is just checking if **hellotherehooman** is present in the string or not , if it is present then it is replacing **hellotherehooman** with `''`

So we can create a final input like :

hello**hellotherehooman**therehooman , here even if that highlighted **hellotherehooman** gets replaced with **' '** the starting **hello** and ending **therehooman** will addup and make a new **hellotherehooman**

```
3 - when our supplied input is : hellohellotherehoomantherehooman
$php main.php
Final String is : hellotherehooman
Success
```

**Final URL :** 

```
https://asm0d3us-ctf.herokuapp.com/Challenge1/index.php?anime_is_bae=hellohellotherehoomantherehooman
```

![yay](https://cdn-images-1.medium.com/max/2460/1*0D9x23DtotC5rauJ4j7Opw.png)

Okay now , The above challenge was just a basic one , Now lets discuss some issues with php.

# 2- Type Juggling

**PHP is easy** until you come across the variable types and context in which the variable is used.

For now lets focus on four **major** types of variables `integer` , `float` , `string` , `bool` .

![variables variables everywhere](https://cdn-images-1.medium.com/max/1030/1*lzXVwnjE10Vb9S6m-ukxkQ.png)

As you have see above that in php there is no need of specifying types of the variables, Rather, it requires only the name of the variable with its value, if any, to be assigned to them.

**Type Juggling** is not a vulnerability or flaw,rather it is a feature of php. As we have seen already, PHP is a loosely typed language, and hence, capable of taking the data type of the value, as that of the variable, to which that value is assigned.

#### Example :

![](https://cdn-images-1.medium.com/max/868/1*d9uY64jo_wQZvQjOlxLDgg.png)

We got our answer as **1338** , wierd ? no it isnt .! thats how php works.We are given so much independence while working with variables, In the above above example **\$var1** is integer , while **\$var2** is a string . Since one of the operand is integer then the other one (string) will automatically be converted into integer. While conversion usually the integer in front of the string is taken as the value of the variable, if there is no integer in front of the string then its value will be **0**.

**Example**

![](https://cdn-images-1.medium.com/max/1294/1*9KfM-WUGH32LyX6hjUhL5A.png)

Before going forward lets understand a bit about comparisons in php , there are two types of comparison in php , loose comparison(== / !=) and strict comparison (=== / !==) . Loose comparison in itself is not a vulnerability rather it is feature , but developers generally make mistakes while dealing with the edge cases of loose comparisons. And as far as I have seen loose comparison+type juggling give birth to serious vulnerability(ofcourse depending upon the context), In worst cases they can lead to “Authentication Bypass” , “Account Takeover” , “Breaking of Cryptographic functions”. Scary isnt it ?

**Loose Comparison**

![from official php documentation](https://cdn-images-1.medium.com/max/2520/1*Og3My2fW2EMO58CMK-UhCQ.png)

**Strict Comparison**

![from official php documentation](https://cdn-images-1.medium.com/max/2502/1*HintAs5R55wcRwhwHyxliQ.png)

Now lets take some **Classic CTF** examples.

#### **Example**

![](https://cdn-images-1.medium.com/max/956/1*XNV1pyxnlQKk16PpZBkylA.png)

In the above example ,Our goal is to print the message **You Win Boi** ,The only variable we can control is **passwd** , this variable **passwd** is getting converted to its md5 hash and then it is compared with 0 if true then the message **You Win Boi** will be printed. However it seems impossible as md5 hashes are of 16bytes (32 bytes if you hexlify them), In short **practically they can never be 0**. If we look closely at the source code we can see that that there is a loose comparison (==) between the md5 hash and 0(In loose comparison **only** value is checked not the **type** of the variable), we can exploit this comparison to print our win message. So somehow we need to find a value whose md5 hash starts with`0e`(e is exponential operator in php) then the whole md5 hash will be treated as 0,(all thanks to type juggling and php loose comparison).`240610708`has its md5 hash starting with`0e`, hence we can set`passwd`variable to`240610708` , then our win message will be printed.

`Important : A pattern of 0e\d+ must be satisfied, if not then the condition will result ‘False’.`

![win win](https://cdn-images-1.medium.com/max/2274/1*Perd7ZtPbGyiqlIvLzc79g.png)

#### Another Example

![](https://cdn-images-1.medium.com/max/1216/1*93hhSek-JT8e-Gbpwt0XjA.png)

The objective again is same(printing win message) , this time it is md4 hash, the win message will be printed if the value of `passwd` will be equal to its md4 hash , which seems impossible but thanks to php’s loose comparison and type juggling we can do it , we just need to find out a value that starts with `0e` and its md4 hash must also start with `0e`then in loose comparison these two values will be treated as 0 and **0==0 is True** hence our win message will be printed.

I found a value which starts with `0e` and its md4 hash also starts with `0e` from [**John Hammond’s CTF Katana**](https://github.com/JohnHammond/ctf-katana)

```
plaintext :  0e001233333333333334557778889
md4 hash  :  0e434041524824285414215559233446
```

![win win](https://cdn-images-1.medium.com/max/2272/1*HFpxGZI5jdfhw_6b-wSeRw.png)

# 3- Controlling the types of variables

Lets try to get the flag here

![](https://cdn-images-1.medium.com/max/1498/1*RzNI1Kqr77tKmfzHUuQGjQ.png)

**Code breakdown :**

```
> A file flag.php is included which stores our flag.

> First 'if' condition uses isset() functions which is just for making sure that the name and password variables are not empty.

> Second 'if'(nested one) makes sure that they are not equal.

> 'else if' computes the SHA1 hashes of both name and password , and if they are equal then we will get our flag.
```

It is not possible for two non-equal entities to have same SHA1 hash, also it is to be noted that there is a strict comparison (===) not a loose one. (so our `0e` trick will not work here). The values (name and password) are being entered through GET request parameter , and hence we can control the value as well as the **type** of the variable , if we send variables (name and password) of type array then we can bypass the SHA1 check , as that SHA1 check will only be executed if the type of the variables (name and password) is string , remember strict comparison checks for both type and value, and if the type doesnt matches then it will simply ignore the condition and **we will get our flag**.

**Exploit :**

```
http://vulnerable/?name[]=x&password[]=y
```

Make sure that the values of name and password are different (x and y) , as the second if (that checks if the values are equal or not) is still getting executed.

![](https://cdn-images-1.medium.com/max/1102/1*NhMQwrzNucMmscw4BLWAFw.png)

Figure out how you can get the flag , **DM me the answer**: [here](https://twitter.com/0xAsm0d3us)

# 4- Regex Bypass using Null Bytes in ereg(Deprecated Now)

ereg() searches a `string` for matches to the regular expression given in `pattern` in a case-sensitive way. (This function was _DEPRECATED_ in PHP 5.3.0, and _REMOVED_ in PHP 7.0.0.) .So whenever you see ereg being used in a php CTF challenge then something is fishy

```
Syntax : ereg ( string $pattern,string $string [,array &$regs ]): int
```

![](https://cdn-images-1.medium.com/max/1104/1*aityGxeE42RS7cQ0TmXLPQ.png)

In the above example , the regex could be bypassed using Null Byte(%00)

![](https://cdn-images-1.medium.com/max/1902/1*i3JoXX3acOgcKRtvNLpjag.png)

Reference : [https://bugs.php.net/bug.php?id=44366](https://bugs.php.net/bug.php?id=44366) (not a bug tho )

# 5- Code Execution

Below are some php functions that can be used to achieve a direct code execution.

```
eval();

assert();

system();

exec();

shell_exec();

passthru();

escapeshellcmd();

pcntl_exec();
```


That's all for now, Have a good day, stay hydrated :)

## __Want to support my work?__
If you think my work has added some value to your existing knowledge, then you can [Buy me a Coffee here](https://www.buymeacoffee.com/Asm0d3us) (and who doesn't loves a good cup of coffee?')

![](https://img.buymeacoffee.com/api/?url=aHR0cHM6Ly9jZG4uYnV5bWVhY29mZmVlLmNvbS91cGxvYWRzL3Byb2ZpbGVfcGljdHVyZXMvMjAyMS8wOS8wMGU4ZGJjODc0NzI0MmRjYTJmNGJkMmMzMzQ1ODUzZC5wbmdAMzAwd18wZS53ZWJw&creator=Asm0d3us&is_creating=creating%20educational%20cybersecurity%20related%20content.&design_code=1&design_color=%235F7FFF&slug=Asm0d3us)