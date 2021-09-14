---
layout: post
toc: false
title: "Genesis 0x01: Ultimate Roadmap for Blockchain Security"
categories: ["Blockchain-Security"]
tags: ["blockchain-security"]
author:
  - Devansh Batham
---

# `👋Howdy`
Welcome to the awesome world of Blockchain Security. As promised in my introductory [Genesis 0x00 post](https://devansh.xyz/blockchain-security/2021/09/13/genesis.html), I am back with the first edition of our `Genesis Series`. For those who don't know what `Genesis` is; Let's do a quick introduction to this series.



`Genesis` is a series of weekly articles on Blockchain Security, which will include interesting topics such as Blockchain basics, Blockchain Development, Ethereum 101, Building Dapps, Common vulnerabilities in smart contracts, Auditing Solidity source code, Static analysis of Smart contracts, latest news and the future state of DeFi.

# `🏗️🔨 Building vs Breaking`


Without knowing how an application/protocol/framework is built or structured, we cannot proceed further with its security audit or find any vulnerabilities in it, however, If you do manage to find `actual` vulnerabilities in a smart contract or any blockchain protocol, without having any prior knowledge of how it is built and structured; You were just throwing arrows in the dark, and got lucky.

To a great extent, your ability to break into an application is directly proportional to your ability to build the same application, that being the reason we will be focusing on blockchain development before we jump to the security aspects related to it. 

This article will be laying down a path/roadmap for us, following which we will enter into the field of Blockchain Security together 🤝.

> All you need is the plan, the road map, and the courage to press on to your destination. - Earl Nightingale



# `✔️The only Roadmap you need`

**Note:** This Roadmap is not exhaustive, but it is organized and covers all rudimentary topics that one needs to know in order to get into the field of Blockchain Security. It also acts as a guide to our future articles in `Genesis Series`.


  - [ ] **Elementary Topics:**
    - [ ] [Familiarity with Linux OS.]()
    - [ ]  [Understanding of commonly used `bash` commands.]()
    - [ ]  [Understanding of version control systems such as `Git` ,`Github`, `Gitlab` , etc.]()
    - [ ]  [What is `CI/CD` pipeline.]()
    - [ ]  [JavaScript.]()
    - [ ]  [Python.]()
    - [ ]  [Good understanding of Object Oriented programming.]()
    - [ ]  [Familiarity with Package Managers (`npm`, `yarn`, `pnpm`, `pip`).]()

- [ ]  **Basics of Internet:**
    - [ ]  [Good understanding of Networking concepts.]()
    - [ ]  [How a Web Browser works.]()
    - [ ]  [What is **DNS** (What happens behind the scenes when you type `google.com` in web browser).]()
    - [ ]  [What is `HTTP` Protocol and how it works.]()
    - [ ]  [What are `HTTP` Request and Response headers.]()
    - [ ]  [What is `RPC` Protocol.]()
    - [ ]  [Familiarity with Browser's developer tools.]()
    - [ ]  [`Web2.0` (how a typical `Web2.0` application is packaged and deployed).]()
    - [ ]  **Existing Authentication/Authorization models in `Web2.0` applications.**
        - [ ]  SSO — Single Sign On
        - [ ]  OAuth — Open Authorization
        - [ ]  JWT Authentication
        - [ ]  Token Based Authentication
        - [ ]  Session Based Authentication
        - [ ]  Basic Authentication
    - [ ]  What is HTTP Caching.
- [ ]  `Web 2.0` **Security:**
    - [ ]  **OWASP Top 10:**
        - [ ]  Broken Access Control vulnerabilities.
        - [ ]  Cryptographic Failures.
        - [ ]  Injection vulnerabilities.
        - [ ]  Insecure Design.
        - [ ]  Security Misconfigurations.
        - [ ]  Vulnerable and Outdated Components.
        - [ ]  Identification and Authentication Failures.
        - [ ]  Software and Data Integrity Failures.
        - [ ]  Security Logging and Monitoring Failures.
        - [ ]  Server-Side Request Forgery.
- [ ]  **Basics of Blockchain:**
    - [ ]  [What is Asymmetric Cryptography.]()
    - [ ]  [What is Elliptic Curve Cryptography.]()
    - [ ]  [Understanding of commonly used words in Blockchain world, such as Programmable, Distributed, Decentralized, Immutable, Unanimous, Time-Stamped, etc.]()
    - [ ]  [Bitcoin Whitepaper.]()
    - [ ]  [What is Double-spending problem and how bitcoin solves it.]()
    - [ ]  [What is Consensus Algorithm.]()
    - [ ]  [Proof of work vs Proof of stake.]()
    - [ ]  [What is Bitcoin Mining and how ASIC is better than regular mining gig.]()
    - [ ]  [What is 51% Attack.]()

- [ ]  **Basics of Ethereum:**
    - [ ]  [What is Etheruem.]()
    - [ ]  [Why Etheruem is termed as `World Computer`.]()
    - [ ]  [How Ethereum is different from its predecessor blockchains.]()
    - [ ]  [What is Ethereum Protocol and how it works.]()
    - [ ]  [The Ethereum Foundation and the ether presale]()
    - [ ]  [What is Ether Currency.]()
    - [ ]  [What are transactions in ethereum ecosystem.]()
    - [ ]  [What are different types of accounts (EOAs vs contract accounts).]()
    - [ ]  [Wallets and Ethereum clients.]()
    - [ ]  [Public Key vs Private Key.]()
    - [ ]  [What is Gas.]()
    - [ ]  [What is a message.]()
    - [ ]  [What is Mining.]()
    - [ ]  [What is a block explorer.]()
    - [ ]  [What are different types of networks in ethereum (Mainnet vs Testnet).]()
    - [ ]  [What is EIP.]()
    - [ ]  [What are ERC standards.]()
    - [ ]  [What is ERC20 Standard.]()
    - [ ]  [What is ERC721 Standard.]()
    - [ ]  [What is Turing Completeness.]()
    - [ ]  [What is Ethereum Virtual Machine(EVM).]()
    - [ ]  [What are Smart Contracts.]()
    - [ ]  [Ethereum Higher Level languages (Solidity, Vyper, LLL, Serpent).]()
- [ ]  **Understanding Solidity**
    - [ ]  [What is Solidity.]()
    - [ ]  [What is Remix IDE.]()
    - [ ]  [What are different Data Types in Solidity (Boolean, Integer, Fixed point, Address, Byte array, Enum, Arrays, Struct, Mapping, Time units, Ether units).]()
    - [ ]  [What are Predefined Global Variables and Functions (`msg.sender`, `msg.value`, `msg.gas`, `msg.data`, `msg.sig`, etc).]()
    - [ ]  [Error handing in Solidity.]()
    - [ ]  [What is Ethereum Contract ABI.]()
    - [ ]  [Life Cycle of Smart Contract.]()
    - [ ]  [Compiling, testing, Deploying smart Contracts.]()
    - [ ]  [What is JSON RPC.]()
    - [ ]  [Interacting with smart contracts using an external library such as `web3.js` or `web3.py`]()
- [ ]  **Frameworks for Ethereum development:**
    - [ ]  [Truffle Suit (Truffle, Ganache, Drizzle).]()
    - [ ]  [Populus (written in Python).]()
    - [ ]  [Infura.]()
    - [ ]  [Openzeppelin.]()
- [ ]  **Smart Contract Security:**
    - [ ]  **Visualization Tools:**
        - [ ]  [Solidity Visual Developer](https://marketplace.visualstudio.com/items?itemName=tintinweb.solidity-visual-auditor)
        - [ ]  [Surya](https://github.com/ConsenSys/surya)
        - [ ]  [Solgraph](https://github.com/raineorshine/solgraph)
        - [ ]  [EVM Lab](https://github.com/ethereum/evmlab)
        - [ ]  [ethereum-graph-debugger](https://github.com/fergarrui/ethereum-graph-debugger)
        - [ ]  [Piet](https://github.com/blockchainsllc/piet)
    - [ ]  **Linters and formatters:**
        - [ ]  [Ethlint](https://github.com/duaraghav8/Ethlint).
        - [ ]  [Prettier + Solidity Plugin.](https://prettier.io/)
        - [ ]  [Solhint.](https://github.com/protofire/solhint)
    - [ ]  **Common Vulnerabilities in Smart contracts:**
        - [ ]  [What is Reentrancy.]()
        - [ ]  [What is Junk code (Code With No Effects).]()
        - [ ]  [What is Unencrypted Private Data On-Chain.]()
        - [ ]  [What is Integer Overflow and Underflow.]()
        - [ ]  [What is Floating `Pragma`.]()
        - [ ]  [What is Unchecked Call Return Value.]()
        - [ ]  [What is Unprotected `SELFDESTRUCT` Instruction.]()
        - [ ]  [State Variable Default Visibility.]()
        - [ ]  [What is Uninitialized Storage Pointer.]()
        - [ ]  [Use of Deprecated Solidity Functions.]()
        - [ ]  [DoS with Failed Call.]()
        - [ ]  [Authorization through `tx.origin`]()
        - [ ]  [Signature Malleability.]()
        - [ ]  [Weak Sources of Randomness from Chain Attributes.]()
        - [ ]  [Lack of Proper Signature Verification.]()
        - [ ]  [Missing Protection against Signature Replay Attacks.]()
        - [ ]  [Insufficient Gas Griefing.]()
        - [ ]  [DoS With Block Gas Limit.]()
        - [ ]  [Hash Collisions With Multiple Variable Length Arguments.]()
        - [ ]  [Message call with hardcoded gas amount.]()
        - [ ]  [Oracle Manipulation.]()
    - [ ]  **Static and Dynamic Analysis:**
        - [ ]  [Oyente](https://github.com/enzymefinance/oyente)
        - [ ]  [Octopus](https://github.com/pventuzelo/octopus)
        - [ ]  [Vertigo](https://github.com/JoranHonig/vertigo)
        - [ ]  [MythX](https://mythx.io/)
        - [ ]  [Mythril](https://github.com/ConsenSys/mythril)
        - [ ]  [Slither](https://github.com/crytic/slither)
        - [ ]  [Echidna](https://github.com/crytic/echidna)
- [ ]  **Blockchain CTFs:**
    - [ ]  [Openzeppelin's Ethernaut.](https://ethernaut.openzeppelin.com)
    - [ ]  [Damn Vulnerable DeFi.](https://www.damnvulnerabledefi.xyz/)
    - [ ]  [Smart Contract CTF.](https://blockchain-ctf.securityinnovation.com)
    - [ ]  [Capture the Ether.](https://capturetheether.com/)
    - [ ]  [GOATCasino](https://github.com/nccgroup/GOATCasino).
    - [ ]  [Paradigm CTF.](https://ctf.paradigm.xyz/)
- [ ]  **Bug Bounty Platforms with Crypto Programs:**
    - [ ]  [Immunefi]()
    - [ ]  [HackerOne]()
    - [ ]  [Bugcrowd]()
- [ ]  **The future of Ethereum:**
    - [ ]  [What is Ethereum 2.0.]()

## `Genesis Newsletter`
Subscribe to Genesis's Newsletter to get future articles/updates/blockchain-related news directly in your mailbox.

<iframe
scrolling="no"
style="width:100%!important;height:220px;border:1px #ccc solid !important"
src="https://buttondown.email/genesis?as_embed=true"
></iframe>

## **`Want to support my work?`**
If you think my work has added some value to your existing knowledge, then you can [Buy me a Coffee here](https://www.buymeacoffee.com/Asm0d3us) (and who doesn't loves a good cup of coffee?')

[![name](https://img.buymeacoffee.com/api/?url=aHR0cHM6Ly9jZG4uYnV5bWVhY29mZmVlLmNvbS91cGxvYWRzL3Byb2ZpbGVfcGljdHVyZXMvMjAyMS8wOS8wMGU4ZGJjODc0NzI0MmRjYTJmNGJkMmMzMzQ1ODUzZC5wbmdAMzAwd18wZS53ZWJw&creator=Asm0d3us&is_creating=creating%20educational%20cybersecurity%20related%20content.&design_code=1&design_color=%235F7FFF&slug=Asm0d3us)](https://www.buymeacoffee.com/Asm0d3us)