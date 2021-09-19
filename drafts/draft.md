---
layout: post
toc: false
title: "Genesis 0x02: Basics of Blockchain"
categories: ["Blockchain-Security"]
tags: ["blockchain-security"]
author:
  - Devansh Batham
---


# `Blockchain`
Blockchains are trending, we hear about them almost everyday, and whenever we search about them on the internet we are blown away with **buzz** words like decentralized, distributed, time-stamped, etc. but do we really understand them? Let's do a quick exercise, I want you to search **What is Blockchain?** on Google, then after a minute or two, try to explain the definition that you learned from those  search results to yourself.

If you were able to successfully complete this exercise, congratulations 🎉. But If you still don't understand, that's fine as well and I am sure you are not alone, let me introduce you to the phenomenon of **The Curse of Knowledge** and why most of those tutorials and articles felt super complicated.

When better-informed people find it extremely difficult to think about problems from the perspective of less well-informed people, and those well-informed people subconsciously assume that you will be able to think about things the same way they do, which in the majority of cases does not hold true, as a result, articles and tutorials they produce are complicated and relatively complex for absolute beginners. 

With this series of articles, I am trying to lower that complexity and I am sure that by the end of this article you will have a pretty decent idea about what a blockchain is.

# `Explain like I'm five`

A blockchain is like a digital ledger used to hold transactions, transactions that transfer or hold instruments of value (that represent real money). Anyone can add a new transaction to a blockchain, however, the previous transactions cannot be tampered with without everyone noticing. 

**Decentralized blockchains** do not need any central authority for their functioning. Every participant in the blockchain has a copy of the exact same data in the form of a ledger, which is why it is called **distributed**, as a result it does not have any single point of failure. 

#### `Some common words that we will be using throughout this series:`

- **P2P:** Every computer or node can act as a server for the others, allowing shared access to resources without the need for a central server.

- **Decentralized and Distributed:** In a decentralized blockchain network, no one has to know or trust anyone else. Each member in the network has a copy of the exact same data in the form of a distributed ledger.

- **Timestamp:** It is a small data stored in each block as a unique serial number which can be used as the **proof for notarization**.

- **Hash Functions:** Hash functions are the backbone of any blockchain, The same data will always produce the same hashed value. Bitcoin's blockchain uses **SHA-256 (Secure Hash Algorithm)** hashing algorithm.

- **Immutable** - The use of cryptographic functions makes a Blockchain immutable. Cryptographic functions return a hash value, which cannot be reverse-engineered, as a result, transactions cannot be tampered with without everyone noticing. 

# `But why do we need a blockchain?`

Blockchain solves various problems, and I dont want to overwhelm you with all of its applications, however, for the sake of simplicity let's understand the most common problem that blockchain solves.

Let's imagine you have a candy store, and someone walks into your store with only **$1** in hand, one candy costs **$1**. He buys one candy with that **$1**, and then he buys another candy with the same **$1**, he used **$1** to buy 2 candies. This is the classic **double-spending** problem, while this appears to be physically impossible as the store owner can easily verify the fraudulent transactions in real-time, but with digital currency, it is very much possible.

That's where blockchain can be used to solve this problem, As stated previously, a blockchain uses a distributed ledger to publically record all transactions on the network, which allows anyone to view the entire history of each coin, and prove that no coin was spent twice.

# `History of Blockchain`
We know blockchain because of bitcoin, yes it is true that blockchain got popular after the release of bitcoin, however the concept of blockchain was coined way before that.

Let's go through [the brief history of blockchain](https://www.icaew.com/technical/technology/blockchain/blockchain-articles/what-is-blockchain/history) and it how evolved over time: 

- **1991** - The term blockchain was first introduced by **Stuart Haber** and **W Scott Stornetta** for describing a cryptographically secured chain of blocks.

- **1998** - Computer scientist **Nick Szabo** introduced **Bit Gold**.


- **2000** - **Stefan** Konst publishes his theory of cryptographic secured chains, along with ideas of implementation.

- **2008** - Developer or group of developers working under the pseudonym **Satoshi Nakamoto** released a white paper establishing the model for a blockchain.

- **2009** - **Bitcoin** was born.

- **2013-2015 - Blockchain 2.0:** Ethereum came into existence.

- **2016** - **Ethereum Classic** was born out of a contentious 2016 debate after a malicious hacker stole $60 million worth of ether.


- **2017** - A new blockchain protocol **EOS.IO** by **block.one** was created for the deployment of decentralized applications.


# `Cryptography`

Cryptography, in a nutshell, means, **"The art of communication in the presence of adversaries"**. Yes, that's it, that was the sole purpose of cryptography when it was created. 

Now, let's look at a more descriptive definition, Cryptography is the mathematical and computational practice of encoding and decoding data. 

In the context of a blockchain, we are only interested in **Asymmetric Cryptography** which makes use of public and private keys. Let's understand it using a scenario.



Alice and Bob are two best friends, Alice has a sensitive document that he wants to share with Bob, he uses a program to encrypt the document with a password of his choice, he then sends that password-protected document to Bob. Bob cannot open the document as he does not know the password Alice used to encrypt the document. Now the question arises, how Alice can securely share the password with Bob? If he sends it via email, there is a chance that someone might be able to access it in between the transmission, which is risky as anyone with the password can access that sensitive document, that's where **Asymmetric Cryptography** was born to solve this problem. 

**Asymmetric Cryptography** can be associated with the example of a mailbox on the street. The mailbox is installed in open, which means it is completely public and anyone who knows its address can go there and drop in a letter, however, only the owner of the mailbox will be able to access the contents in it. In this example, the address of mailbox is **public key**, and the key to the mailbox is **private key**.


Most blockchains make use of asymmetric cryptography to manage addresses on the blockchain. The public key is the address, which holds the tokens. The private key is used to access the address and authorize actions for the address.





That was all from my side in this article; See you very soon in `Genesis 0x03`, Keep warm, stay hydrated and have good day ahead :)

# 💌 **`Want to support my work?`**
If you think my work has added some value to your existing knowledge, then you can [Buy me a Coffee here](https://www.buymeacoffee.com/Asm0d3us) (and who doesn't loves a good cup of coffee?)

[![name](https://img.buymeacoffee.com/api/?url=aHR0cHM6Ly9jZG4uYnV5bWVhY29mZmVlLmNvbS91cGxvYWRzL3Byb2ZpbGVfcGljdHVyZXMvMjAyMS8wOS8wMGU4ZGJjODc0NzI0MmRjYTJmNGJkMmMzMzQ1ODUzZC5wbmdAMzAwd18wZS53ZWJw&creator=Asm0d3us&is_creating=creating%20educational%20cybersecurity%20related%20content.&design_code=1&design_color=%235F7FFF&slug=Asm0d3us)](https://www.buymeacoffee.com/Asm0d3us)

# `Genesis Newsletter`
Subscribe to Genesis's Newsletter to get future articles/updates/blockchain-related news directly in your mailbox.

<iframe
scrolling="no"
style="width:100%!important;height:220px;border:1px #ccc solid !important"
src="https://buttondown.email/genesis?as_embed=true"
></iframe>



