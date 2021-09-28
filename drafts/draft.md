---
layout: post
toc: false
title: "Genesis 0x03: Basics of Ethereum"
categories: ["Blockchain-Security"]
tags: ["blockchain-security"]
author:
  - Devansh Batham
---


# Ethereum's Creation
We learned about blockchains in [our previous article](https://devansh.xyz/blockchain-security/2021/09/23/genesis-0x02.html). We also discussed a little about Bitcoin and how it solves the double-spending problem by maintaining a distributed ledger to publicly record all transactions on the network, which allows anyone to view the entire history of each coin, and prove that no coin was spent twice. So far, so good.

Bitcoin was created solely for storing/sending/receiving digital money in a safe, secure, and decentralized manner without the involvement of any governing body, which started the new era, called **Cryptoeconomics**, however seeing the potential of blockchain and its applications, people started proposing various use-cases of blockchain for solving a wide range of problems. Creating separate blockchains from scratch for different tasks was time-consuming and not scalable at all, as a result, **Ethereum** was created, which enabled developers to build and publish smart contracts (self-executing/autonomous blocks of code) and distributed applications that can be used without the risks of downtime, fraud, or interference from a third party.


[Ethereum](https://en.wikipedia.org/wiki/Ethereum) was conceived in 2013 by a Canadian-Russian programmer
 **Vitalik Buterin**. Its Development started in **2014**, and the network went live on **30 July 2015**.


**Vitalik** wrote a [detailed article](https://vitalik.ca/general/2017/09/14/prehistory.html) in 2017 titled **A Prehistory of the Ethereum Protocol**, following are few excerpts from [that article](https://vitalik.ca/general/2017/09/14/prehistory.html). I highly recommend everyone to read that article thoroughly for better understanding of how Ethereum evolved over time.


> This was the time when the Ethereum protocol was entirely my own creation. From here on, however, new participants started to join the fold. By far the most prominent on the protocol side was Gavin Wood, who reached out to me in an about.me message in December 2013. - Vitalik

-----
> Gavin can also be largely credited for the subtle change in vision from viewing Ethereum as a platform for building programmable money, with blockchain-based contracts that can hold digital assets and transfer them according to pre-set rules, to a general-purpose computing platform. This started with subtle changes in emphasis and terminology, and later this influence became stronger with the increasing emphasis on the “Web 3” ensemble, which saw Ethereum as being one piece of a suite of decentralized technologies, the other two being Whisper and Swarm. - Vitalik

---------

> By the summer of 2014, the protocol had considerably stabilized, with the major exception of the proof of work algorithm which would not reach the Ethash phase until around the beginning of 2015, and a semi-formal specification existed in the form of Gavin's yellow paper. - Vitalik





# Ethereum "The World Computer"

We are already aware that Ethereum enables developers to build and publish smart contracts and distributed applications aka Dapps, in simple terms, it acts as a platform for storing smart contracts, and when certain preconditions are met, the contract gets executed. The real question is, How Ethereum as a platform manages to do so? Lots of nodes participate in this process for getting a few ethers(mining reward) for doing it. These nodes or computers work together and share a common blockchain.


Ethereum simulates a perfect Turing complete machine, a thing which could never exist in nature because of the laws of physics, but which can be simulated by a large enough computer network, that's why Ethereum is referred to as **World Computer**.

In colloquial usage, the terms "Turing-complete" and "Turing-equivalent" are used to mean that any real-world general-purpose computer or computer language can approximately simulate the computational aspects of any other real-world general-purpose computer or computer language.

# Ethereum Development Stages
- **Frontier:** The initial stage of Ethereum.


- **Ice Age:** A hard fork to introduce an exponential difficulty increase.


- **Homestead:** The second stage of Ethereum.


- **DAO:** A hard fork that caused Ethereum and Ethereum Classic to split into two competing systems.


- **Tangerine Whistle:** A hard fork to change the gas calculation for certain I/O-heavy operations and to clear the accumulated state from a denial-of-service (DoS) attack that exploited the low gas cost of those operations.


- **Spurious Dragon:** A hard fork to address more DoS attack vectors.


- **Metropolis Byzantium:**  The third stage of Ethereum. 

- **Constantinople / St. Petersburg:** Constantinople was planned to be the second part of Metropolis with similar improvements. A few hours before its activation, a critical bug was discovered. The hard fork was therefore postponed and renamed St. Petersburg.


- **Istanbul:** An additional hard fork with the same approach, and naming convention, as for the prior two.


- **Muir Glacier:** A hard fork whose sole purpose was to adjust the difficulty again due to the exponential increase introduced by Ice Age.

# Smart Contracts

The word **contract** means a set of promises between two or more parties. With that logic, **Smart** contracts should be set of promises but in some kind of digital form, right? Well... The word **contract** has no legal meaning in the context of Ethereum. **Smart Contracts** are simply programs(self-executing autonomous blocks of code) stored on a blockchain.

For the sake of simplicity, whenever you hear the word **smart contract**, think of it as some kind of computer program that gets executed when certain preconditions are met. There is no need to overcomplicate things, keep them simple and you will soon learn a lot about smart contracts when we will be programming them using Solidity and deploying those smart contracts as well.

## Characteristics of a smart contract
- Immutable
- Deterministic
- EVM compatible
- Self-executing
- Autonomous


# Types of accounts in  Ethereum

### Ethereum has two account types:

**Externally-owned accounts (EOAs):** They can be controlled by anyone with the private keys.

**Contract Accounts:** They are controlled by code to the network in the form of smart contracts.

It is important to know that both accounts have the ability to receive, hold and send ETH and interact with deployed smart contracts.

Moreover, Transactions between externally-owned accounts can only be ETH/token transfers, while Transactions from an external account to a contract account can trigger code which can execute many different actions, such as transferring tokens or even creating a new contract.


# Ethereum Virtual Machine (EVM)


# Fast Track Learning
**Q- What do I mean by the term Ethereum?** 

Well... it can be used to refer to three distinct things:

- The Ethereum protocol.
- The Ethereum network.
- The Ethereum project.  

**Q- Is Ethereum and Ether the same thing?**

**Ethereum** is a decentralized, open-source, programmable blockchain which enables developers to build and publish smart contracts (self-executing/autonomous blocks of code) and distributed applications that can be used without the risks of downtime, fraud, or interference from a third party. While **Ether (ETH or Ξ)** is the native cryptocurrency of the platform.

**Q- How Ethereum is different from Bitcoin?**

Bitcoin was too limited in its functionality. In an interview with [Business Insider](https://www.businessinsider.com/vitalik-buterin-created-ethereum-one-of-the-worlds-three-largest-cryptocurrencies-2019-1?r=US&amp;IR=T), Vitalik compared it to a pocket calculator that **does one thing well**, whereas he said Ethereum is more like a smartphone with multiple applications you can use.

**Q- Is Ethereum Better Than Bitcoin?**

Can you compare a mango with a banana? **No**. In other words, Ethereum has much wider ambitions. It wants to be a decentralized computing platform for creating other decentralized applications, while Bitcoin is digital gold. 

**Q- What are smart contracts?**

Smart contracts are simply programs(self-executing autonomous blocks of code) stored on a blockchain that run when certain predetermined conditions are met.

**Q- What are some benefits of smart contracts?**

- Speed, efficiency and accuracy
- Trust and transparency
- Security
- No need of intermediaries to handle transactions.


# Further reading
**Note:** Some of the information mentioned in this article is taken from the below sources, I highly recommend readers to go through these resources/articles thoroughly. 

- [Ethereum, Smart Contracts, and the World Computer
](https://consensys.net/blog/news/programmable-blockchains-in-context-ethereum-smart-contracts-and-the-world-computer/)
- [Ethereum Wikipedia](https://en.wikipedia.org/wiki/Ethereum)
- [Turing Completeness](https://en.wikipedia.org/wiki/Turing_completeness)
- [Ethereumbook](https://github.com/ethereumbook/ethereumbook)
- [Ethereum Account Types](https://github.com/ethereum.org/en/developers/docs/accounts/)

That was all from my side in this article; See you very soon in **Genesis 0x04**, Keep warm, stay hydrated and have good day ahead :)

# 💌 **Want to support my work?**
If you think my work has added some value to your existing knowledge, then you can [Buy me a Coffee here](https://www.buymeacoffee.com/Asm0d3us) (and who doesn't loves a good cup of coffee?)

[![name](https://img.buymeacoffee.com/api/?url=aHR0cHM6Ly9jZG4uYnV5bWVhY29mZmVlLmNvbS91cGxvYWRzL3Byb2ZpbGVfcGljdHVyZXMvMjAyMS8wOS8wMGU4ZGJjODc0NzI0MmRjYTJmNGJkMmMzMzQ1ODUzZC5wbmdAMzAwd18wZS53ZWJw&creator=Asm0d3us&is_creating=creating%20educational%20cybersecurity%20related%20content.&design_code=1&design_color=%235F7FFF&slug=Asm0d3us)](https://www.buymeacoffee.com/Asm0d3us)

# Newsletter
Subscribe to Genesis's Newsletter to get future articles/updates/blockchain-related news directly in your mailbox.

<iframe
scrolling="no"
style="width:100%!important;height:220px;border:1px #ccc solid !important"
src="https://buttondown.email/genesis?as_embed=true"
></iframe>