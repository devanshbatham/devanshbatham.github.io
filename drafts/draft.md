---
layout: post
toc: false
title: "Genesis 0x04: How to Learn Solidity in 30 Days"
categories: ["Blockchain-Security"]
tags: ["blockchain-security"]
author:
  - Devansh Batham
---


Can you master Solidity in 30 days? **No, you cannot.**

Can you learn about the basics and get started with the development of real-world projects using Solidity in 30 days?  **Yes, you sure can**, and this article aims to provide you with a roadmap following which you can learn Solidity in a much more efficient way.


# 💡 Learning Hacks

> "I realized that becoming a master of karate was not about learning 4,000 moves but about doing just a handful of moves 4,000 times."
— Chet Holmes

Before we proceed further, let's talk about some hacks that I use for learning any skill or programming language in a faster manner.

- Before going to bed, recite what you learned for 5 mins.

- Don't push yourself beyond your capacity, always keep in mind that excellence can only be attained when it is organic.

- Teach someone else (or just pretend to) what you learned.

- Get proper sleep, research shows that sleeping between two learning sessions greatly improves retention.

- Take notes by hand (Yes, I agree that this might sound anti-digital, but believe me, it improves our knowledge retention).


- Stay hydrated and exercise regularly. A healthy mind breeds a healthy body, and vice versa!



# 🏷️ [Day 1 - Day 5] Javascript: The Starting Block

We all have different levels of experience and familiarity with programming languages. Now that you are here, I assume you are already familiar with basic Javascript syntax and the Object-Oriented paradigm. If you are not, I would suggest you should learn JavaScript before starting with Solidity. You don't need to learn A-Z of JavaScript. All you need for getting started is a basic understanding of JS syntax and object-oriented programming.

## JavaScript Fundamentals
- [ ] [An Introduction to JavaScript](https://javascript.info/intro)
- [ ] [Manuals and specifications](https://javascript.info/manuals-specifications)
- [ ] [Code editors](https://javascript.info/code-editors)
- [ ] [Developer console](https://javascript.info/devtools)
- [ ] [Hello, world!](https://javascript.info/hello-world)
- [ ] [Variables](https://javascript.info/variables)
- [ ] [Data types](https://javascript.info/types)
- [ ] [Type Conversions](https://javascript.info/type-conversions)
- [ ] [Basic operators, maths](https://javascript.info/operators)
- [ ] [Comparisons](https://javascript.info/comparison)
- [ ] [Conditional branching: if, '?'](https://javascript.info/ifelse)
- [ ] [Logical operators](https://javascript.info/logical-operators)
- [ ] [Nullish coalescing operator '??'](https://javascript.info/nullish-coalescing-operator)
- [ ] [Loops: while and for](https://javascript.info/while-for)
- [ ] [The "switch" statement](https://javascript.info/switch)
- [ ] [Functions](https://javascript.info/function-basics)
- [ ] [Function expressions](https://javascript.info/function-expressions)
- [ ] [Arrow functions, the basics](https://javascript.info/arrow-functions-basics)
- [ ] [Objects](https://javascript.info/object)
- [ ] [Object references and copying](https://javascript.info/object-copy)
- [ ] [Garbage collection](https://javascript.info/garbage-collection)
- [ ] [Object methods, "this"](https://javascript.info/object-methods)
- [ ] [Constructor, operator "new"](https://javascript.info/constructor-new)
- [ ] [Object to primitive conversion](https://javascript.info/object-toprimitive)
- [ ] [Class basic syntax](https://javascript.info/class)
- [ ] [Class inheritance](https://javascript.info/class-inheritance)
- [ ] [Static properties and methods](https://javascript.info/static-properties-methods)
- [ ] [Private and protected properties and methods](https://javascript.info/private-protected-properties-methods)
- [ ] [Extending built-in classes](https://javascript.info/extend-natives)
- [ ] [Class checking: "instanceof"](https://javascript.info/instanceof)
- [ ] [Callbacks](https://javascript.info/callbacks)
- [ ] [Promise](https://javascript.info/promise-basics)
- [ ] [Promises chaining](https://javascript.info/promise-chaining)
- [ ] [Error handling with promises](https://javascript.info/promise-error-handling)
- [ ] [Promise API](https://javascript.info/promise-api)
- [ ] [Promisification](https://javascript.info/promisify)
- [ ] [Async/Await](https://javascript.info/async-await)
- [ ] [Generators](https://javascript.info/generators)



# 🏷️ [Day 6] Frameworks
We learned javascript and now we have a fairly decent understanding of object-oriented programming as well. What next? Can we start learning solidity now? Yes, we can. 

As we are just getting started with Solidity, I would suggest you use [Remix IDE](https://remix.ethereum.org/) for writing and compiling solidity code for now. As we gain more experience and familiarity with Solidity, we will start using a more robust Dapp development framework (such as Truffle, Hardhat, Dapptools, etc) because building a full-fledged decentralized application requires different pieces of technologies, and software frameworks include many of those needed features.

Even though we are not going to use any of these frameworks as of now, but we need to know what different frameworks are available to build dapps.


- [ ] [Truffle](https://www.trufflesuite.com/) - A development environment, testing framework, build pipeline, and other tools.
- [ ] [Hardhat](https://hardhat.org/) - Ethereum development environment for professionals.
- [ ] [Brownie](https://eth-brownie.readthedocs.io/en/latest/) - Python-based development environment and testing framework.
- [ ] [Embark](https://framework.embarklabs.io/docs/) - A development environment, testing framework, and other tools integrated with Ethereum, IPFS, and Whisper.
- [ ] [Web3j](https://www.web3labs.com/web3j-sdk) - A platform for developing blockchain applications on the JVM.
- [ ] [OpenZeppelin SDK](https://openzeppelin.com/sdk/) - The Ultimate Smart Contract Toolkit: A suite of tools to help you develop, compile, upgrade, deploy and interact with smart contracts.
- [ ] [Create Eth App](https://github.com/paulrberg/create-eth-app) - Create Ethereum-powered apps with one command. Comes with a wide offering of UI frameworks and DeFi templates to choose from.
- [ ] [Scaffold-Eth](https://github.com/austintgriffith/scaffold-eth) - Ethers.js + Hardhat + React components and hooks for web3: everything you need to get started building decentralized applications powered by smart contracts.
- [ ] [Alchemy](https://www.alchemy.com/) - Ethereum Development Platform.
- [ ] [Dapptools](https://dapp.tools/) - A suite of Ethereum focused CLI tools following the Unix design philosophy, favoring composability, configurability and extensibility.


# 🏷️ [Day 7 - Day 10] Understanding Solidity
Solidity is an object-oriented/contract-oriented, high-level language for writing smart contracts. It is statically typed, supports inheritance, and is highly influenced by C++, Python and JavaScript.

**⚠️ Note:** Following URLs will get outdated as soon as new versions of Solidity will be released, I will try to update these URLs every month, but if I fail to do so for some reason, it is advised readers should refer to the latest documentation.

## Day 7
- [ ] [Introduction to Smart Contracts](https://docs.soliditylang.org/en/v0.8.9/introduction-to-smart-contracts.html)
- [ ] [Installing the Solidity Compiler](https://docs.soliditylang.org/en/v0.8.9/installing-solidity.html)
- [ ] [Layout of a Solidity Source File](https://docs.soliditylang.org/en/v0.8.9/layout-of-source-files.html)
- [ ] [Structure of a Contract](https://docs.soliditylang.org/en/v0.8.9/structure-of-a-contract.html)
- [ ] [Data Types](https://docs.soliditylang.org/en/v0.8.9/types.html)
- [ ] [Units and Globally Available Variables](https://docs.soliditylang.org/en/v0.8.9/units-and-global-variables.html)


## Day 8
- [ ] [Expressions and Control Structures](https://docs.soliditylang.org/en/v0.8.9/control-structures.html)
- [ ] [Inline Assembly](https://docs.soliditylang.org/en/v0.8.9/assembly.html)
- [ ] [Language Grammar](https://docs.soliditylang.org/en/v0.8.9/grammar.html)


## Day 9
- [ ] [Using the Compiler](https://docs.soliditylang.org/en/v0.8.9/using-the-compiler.html)
- [ ] [Analysing the Compiler Output](https://docs.soliditylang.org/en/v0.8.9/analysing-compilation-output.html)
- [ ] [Layout of State Variables in Storage](https://docs.soliditylang.org/en/v0.8.9/internals/layout_in_storage.html)
- [ ] [Layout in Memory](https://docs.soliditylang.org/en/v0.8.9/internals/layout_in_memory.html)

## Day 10
- [ ] [Contract Metadata](https://docs.soliditylang.org/en/v0.8.9/metadata.html)
- [ ] [Contract ABI Specification](https://docs.soliditylang.org/en/v0.8.9/abi-spec.html)


# 🏷️ [Day 11] Break
We are on a learning streak for the past ten consecutive days. I believe it is time you should take a day out for yourself. You are doing very well so far and you deserve a break. Go out, Treat yourself to your favorite food, give food to some street animals, spread love and have fun ❤️😊. 

# 🏷️[Day 12 - Day 17] On-hands Practice
We are familiar with Solidity documentation now. It is time to write actual code, let's practice Solidity by understanding and re-writing the following example contracts:

## Day 12: 
- [ ] [Hello World](https://solidity-by-example.org/hello-world/)
- [ ] [First App](https://solidity-by-example.org/first-app/)
- [ ] [Primitive Data Types](https://solidity-by-example.org/variables/)
- [ ] [Variables](https://solidity-by-example.org/variables/)
- [ ] [Reading and Writing to a State Variable](https://solidity-by-example.org/state-variables/)
- [ ] [Ether and Wei](https://solidity-by-example.org/ether-units/)

## Day 13:
- [ ] [Gas and Gas Price](https://solidity-by-example.org/gas/)
- [ ] [If / Else](https://solidity-by-example.org/if-else/)
- [ ] [For and While Loop](https://solidity-by-example.org/loop/)
- [ ] [Mapping](https://solidity-by-example.org/mapping/)
- [ ] [Array](https://solidity-by-example.org/array/)
- [ ] [Enum](https://solidity-by-example.org/enum/)
- [ ] [Structs](https://solidity-by-example.org/structs/)

## Day 14:
- [ ] [Data Locations - Storage, Memory and Calldata](https://solidity-by-example.org/data-locations/)
- [ ] [Function](https://solidity-by-example.org/function/)
- [ ] [View and Pure Functions](https://solidity-by-example.org/view-and-pure-functions/)
- [ ] [Error](https://solidity-by-example.org/error/)
- [ ] [Function Modifier](https://solidity-by-example.org/function-modifier/)
- [ ] [Events](https://solidity-by-example.org/events/)

## Day 15:
- [ ] [Constructor](https://solidity-by-example.org/constructor/)
- [ ] [Inheritance](https://solidity-by-example.org/inheritance/)
- [ ] [Shadowing Inherited State Variables](https://solidity-by-example.org/shadowing-inherited-state-variables/)
- [ ] [Calling Parent Contracts](https://solidity-by-example.org/super/)
- [ ] [Visibility](https://solidity-by-example.org/visibility/)
- [ ] [Interface](https://solidity-by-example.org/interface/)
- [ ] [Payable](https://solidity-by-example.org/payable/)

## Day 16:
- [ ] [Sending Ether - Transfer, Send, and Call](https://solidity-by-example.org/sending-ether/)
- [ ] [Fallback](https://solidity-by-example.org/fallback/)
- [ ] [Call](https://solidity-by-example.org/call/)
- [ ] [Delegatecall](https://solidity-by-example.org/delegatecall)
- [ ] [Function Selector](https://solidity-by-example.org/function-selector/)
- [ ] [Calling Other Contract](https://solidity-by-example.org/calling-contract/)

## Day 17:


- [ ] [Creating Contracts from a Contract](https://solidity-by-example.org/new-contract/)
- [ ] [Try / Catch](https://solidity-by-example.org/try-catch/)
- [ ] [Import](https://solidity-by-example.org/import/)
- [ ] [Library](https://solidity-by-example.org/library/)
- [ ] [Hashing with Keccak256](https://solidity-by-example.org/hashing/)
- [ ] [Verifying Signature](https://solidity-by-example.org/signature/)

# 🏷️ [Day 18 - Day 19] Micro-projects
From Day 12 to Day 17, we completed code practice of various Solidity concepts, now it is time to put all of those learnings from previous days into micro-projects.

## Day 18:
- [ ] [Multi Sig Wallet](https://solidity-by-example.org/app/multi-sig-wallet/)
- [ ] [Merkle Tree](https://solidity-by-example.org/app/merkle-tree/)
- [ ] [Iterable Mapping](https://solidity-by-example.org/app/iterable-mapping/)
- [ ] [ERC 20](https://solidity-by-example.org/app/erc20/)

## Day 19:
- [ ] [Precompute Contract Address with Create2](https://solidity-by-example.org/app/create2/)
- [ ] [Minimal Proxy Contract](https://solidity-by-example.org/app/minimal-proxy/)
- [ ] [Uni-directional Payment Channel](https://solidity-by-example.org/app/uni-directional-payment-channel/)
- [ ] [Bi-directional Payment Channel](https://solidity-by-example.org/app/bi-directional-payment-channel/)


# 🏷️ [Day 20] Break
We are on a learning streak for the past eight consecutive days. I believe it is time you should take a day out for yourself. You are doing very well so far and you deserve a break. Go out, Treat yourself to your favorite food, give food to some street animals, spread love and have fun ❤️😊. 


# 🏷️ [Day 21 - Day 25] Secrurity Considerations
We are now familiar with foundations concepts of Solidity programming, it is right time for us to understand what common vulnerabilities can be present in smart contracts and how you can spot and mitigate them. 
       
## Day 21:
- [ ]  [What is Reentrancy.](https://swcregistry.io/docs/SWC-107)
- [ ]  [What is Junk code (Code With No Effects).](https://swcregistry.io/docs/SWC-135)
- [ ]  [What is Unencrypted Private Data On-Chain.](https://swcregistry.io/docs/SWC-136)
- [ ]  [What is Integer Overflow and Underflow.](https://swcregistry.io/docs/SWC-101)

## Day 22:
- [ ]  [What is Floating `Pragma`.](https://swcregistry.io/docs/SWC-103)
- [ ]  [What is Unchecked Call Return Value.](https://swcregistry.io/docs/SWC-104)
- [ ]  [What is Unprotected `SELFDESTRUCT` Instruction.](https://swcregistry.io/docs/SWC-106)
- [ ]  [State Variable Default Visibility.](https://swcregistry.io/docs/SWC-108)

## Day 23:
- [ ]  [What is Uninitialized Storage Pointer.](https://swcregistry.io/docs/SWC-109)
- [ ]  [Use of Deprecated Solidity Functions.](https://swcregistry.io/docs/SWC-111)
- [ ]  [DoS with Failed Call.](https://swcregistry.io/docs/SWC-113)
- [ ]  [Authorization through `tx.origin`](https://swcregistry.io/docs/SWC-115)

## Day 24:
- [ ]  [Signature Malleability.](https://swcregistry.io/docs/SWC-117)
- [ ]  [Weak Sources of Randomness from Chain Attributes.](https://swcregistry.io/docs/SWC-120)
- [ ]  [Lack of Proper Signature Verification.](https://swcregistry.io/docs/SWC-122)
- [ ]  [Missing Protection against Signature Replay Attacks.](https://swcregistry.io/docs/SWC-121)

## Day 25:
- [ ]  [Insufficient Gas Griefing.](https://swcregistry.io/docs/SWC-126)
- [ ]  [DoS With Block Gas Limit.](https://swcregistry.io/docs/SWC-128)
- [ ]  [Hash Collisions With Multiple Variable Length Arguments.](https://swcregistry.io/docs/SWC-133)
- [ ]  [Message call with hardcoded gas amount.](https://swcregistry.io/docs/SWC-134)
- [ ]  [Oracle Manipulation.](https://hackernoon.com/how-dollar100m-got-stolen-from-defi-in-2021-price-oracle-manipulation-and-flash-loan-attacks-explained-3n6q33r1)



# 🏷️ [Day 25 - Day 27] Tools and Frameworks
During these three days, our goal is to get familiar with existing tools and frameworks which can be useful while performing security audits related to smart contracts. Please note that there is no need to know A-Z about these tools, for now, just play around with them, get familiar, and test them out, and most importantly, Have fun!

## Day 25:
- [ ]  **Visualization Tools:**
    - [ ]  [Solidity Visual Developer](https://marketplace.visualstudio.com/items?itemName=tintinweb.solidity-visual-auditor)
    - [ ]  [Surya](https://github.com/ConsenSys/surya)
    - [ ]  [Solgraph](https://github.com/raineorshine/solgraph)
    - [ ]  [EVM Lab](https://github.com/ethereum/evmlab)
    - [ ]  [ethereum-graph-debugger](https://github.com/fergarrui/ethereum-graph-debugger)
    - [ ]  [Piet](https://github.com/blockchainsllc/piet)

## Day 26:
- [ ]  **Linters and formatters:**
    - [ ]  [Ethlint](https://github.com/duaraghav8/Ethlint).
    - [ ]  [Prettier + Solidity Plugin.](https://prettier.io/)
    - [ ]  [Solhint.](https://github.com/protofire/solhint)
    
## Day 27:
- [ ]  **Static and Dynamic Analysis:**
    - [ ]  [Oyente](https://github.com/enzymefinance/oyente)
    - [ ]  [Octopus](https://github.com/pventuzelo/octopus)
    - [ ]  [Vertigo](https://github.com/JoranHonig/vertigo)
    - [ ]  [MythX](https://mythx.io/)
    - [ ]  [Mythril](https://github.com/ConsenSys/mythril)
    - [ ]  [Slither](https://github.com/crytic/slither)
    - [ ]  [Echidna](https://github.com/crytic/echidna)


# 🏷️ [Day 28 - Day 29] Reading audit reports
During these 2 days, we will be going through publicly available smart contracts audit reports, and see what kind of real-world vulnerabilities are generally present in Solidity code. I believe there is no need for me to include a list of URLs that host public audit reports, as they are just a Google search away.

![](https://raw.githubusercontent.com/devanshbatham/devanshbatham.github.io/master/assets/images/blockchain/smart-contract-audits.PNG)

# 🏷️ [Day 30] Break
We are on a learning streak for the past eight consecutive days. I believe it is time you should take a day out for yourself. You are doing very well so far and you deserve a break. Go out, Treat yourself to your favorite food, give food to some street animals, spread love and have fun ❤️😊. 


# 30 Days Challenge
If you do start this 30 days challenge, you can post your progress on Twitter with hashtag #30DaysOfSolidity and don't forget to tag me [@0xAsm0d3us](https://twitter.com/0xAsm0d3us). I'll be happy to see your progress. For any query, you can reach out to me via Twitter, I'll be glad to help. All the best ❤️


# 💌 **Want to support my work?**
If you think my work has added some value to your existing knowledge, then you can [Buy me a Coffee here](https://www.buymeacoffee.com/Asm0d3us) (and who doesn't loves a good cup of coffee?)

[![name](https://img.buymeacoffee.com/api/?url=aHR0cHM6Ly9jZG4uYnV5bWVhY29mZmVlLmNvbS91cGxvYWRzL3Byb2ZpbGVfcGljdHVyZXMvMjAyMS8wOS8wMGU4ZGJjODc0NzI0MmRjYTJmNGJkMmMzMzQ1ODUzZC5wbmdAMzAwd18wZS53ZWJw&creator=Asm0d3us& is_creating=creating%20educational%20cybersecurity%20related%20content.&design_code=1&design_color=%235F7FFF&slug=Asm0d3us)](https://www.buymeacoffee.com/Asm0d3us)

# Newsletter
Subscribe to Genesis's Newsletter to get future articles/updates/blockchain-related news directly in your mailbox.

<iframe
scrolling="no"
style="width:100%!important;height:220px;border:1px #ccc solid !important"
src="https://buttondown.email/genesis?as_embed=true"
></iframe>