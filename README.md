[![Slack Status](http://slack.crypti.me/badge.svg)](http://slack.crypti.me)

# Welcome!

Welcome to Crypti DApps documentation. Here is:

 * Tutorials.
 * Documentations.
 * API.

This all will allow you to make any DApp what you want.

## Table of contents

TODO

## Crypti DApps


Crypti DApps are decentralized application, that working in Sidechain, and allow developers create new decentralzied products, and use XCR or BTC in this projects.
It's means each dapp contains their own sidechain, blocks of this sidechain generated by dapps forgers, that will take fee for it.

Users of DApps can easy deposit each DApp, use deposited XCR in DApp, and then withdrawal XCR from DApp. Deposit/withdrawal it's special transactions in Crypti, that move your XCR funds from main Crypti chain,
to sidechain, and allow use this XCR in DApp.

Just few examples of dapps and how it can work:

  * **Messaging DApp** - Users deposits messaging DApp, send message and pay fees for each message to owner of DApp.
  * **Decentralized Exchange** - Users deposits decentralized exchange DApp and pays fees for open new order, etc.
  * **Decentralized Torrent Traker** - Users posts new torrents files to DApp and get XCR as "thanks" for sharing.
  
It's make for Crypti some economies and real world use, support DApps developer. 

## How to make DApp?

All DApps written in full-stack web technologies:

  * **Nodejs/Javascript** - for backend and frontend.
  * **CSS3/HTML5** - For UI.
  
A lot of developers already know all or some of this technlogoies, that allows developers fast and easy create new decentralized applications and take some profit. 

Then using our Command Line Interface *crypti-cli* developer can easy generate new genesis block for sidechain, clone **Crypti Toolkit** as base project structure, easy create new contract.

Use our tutorials to know more how to make DApps. All tutorials in this repository. 

## Crypti DApps working in Nodejs?

Yes, it's working in sandboxed Nodejs. We prevent 90% of low system calls with [Seccomp](https://en.wikipedia.org/wiki/Seccomp). It's because you can run master node only on Linux and can't run master node on Mac OS/Windows, but you can develop there.

So, when Crypti launch new DApp, it's launch new Nodejs process, secured by Seccomp, and it communicate with Crypti via pipes. There is not limit of message size, we made some work to prevent it, because by default pipes have some limitations.

## Who is DApp forgers?

It's forgers, who generate blocks in sidechain. This forgers approved by owner of DApp, they will generate new blocks and get part of fees. It's done to make community interesting in support dapps by community nodes. 

Genesis block contains base list of forgers, but it can be changed later. All operations with genesis block works via **crypti-cli**.

## How Deposit/Withdrawal works?

When you deposit or withdrawal, you send special type of transaction. In case of deposit, it's sent deposit transaction from mainchain, then DApp recieve it, create new transaction, that will save transactionId in DApp blockchain, to prevent double spending attack, and then it will add funds on your account. 

All funds that was deposited stored on DApp owner account. So, this funds don't real move from mainchain, it's just stored on owner account of DApp. To prevent scam projects, and theft of DApp funds, we added multisignature functional, and recommend to use open sourced DApps, where one of known escrow under multisignature.

When you withdrawal you funds from DApp, you send new transaction to withdrawal in DApp, once this transaction applied in block, DApp master nodes will create withdrawal transaction, that will send in mainchain, and mainchain will store transaction id from sidechain, to prevent double spending attacks.

# API

API to communicate between DApp and Crypti can be found [here](http://docs.crypti.me).

## Help?

We ready to help! Just join our slack: http://slack.crypti.me , we there all time and ready to help you with your great idea!
