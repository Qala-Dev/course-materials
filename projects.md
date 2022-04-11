---
description: project ideas for Qala development course
---

# Projects

## General

* We are going to be building multiple projects over the duration of the course, so don't worry about being locked in to a project which you might change your mind about later.
* Projects can be built as a front-end application, back end application, API or a command line tool.
* _If_ you choose a project from the list, you can choose either a bitcoin or a lightning project.
* You may also have your own project or idea that you'd like to build out -- great! Please run your own projects past the instructors first so we can check it is suitable and determine which skills it will exercise.
* Your first project will probably leverage a bitcoin or lightning library or development kit, in order to facilitate fast iteration on end results.
* In your second/third project you should be considering not using a library to do as much of the heavy lifting, so that you can become more comfortable with how bitcoin and lightning work under the hood.

## Mini design document

When you've chosen your next project, we'll ask for a mini design document from you.
This document only wants to be about a page or less, and should contain your thoughts on the following:

1. A basic outline of the project
1. Chosen language/framework & any libraries you intend to use
1. Your high-level general approach 
    * what you will build first
    * what you will add later
1. What milestone you need to reach to consider the project have achieved minimum viable product (MVP) state

Please create and share the design document using a collaborative document editor, so that we can add any comments or feedback that we have.
Examples of editors <https://hackmd.io> and <https://docs.google.com>, but you can choose any you're familiar with so long as we can easily log in to comment.

## Bitcoin projects

Topics to cover: transactions, scripting, reorgs, HD wallets

### Tier 1

1. [Satoshi dice/game](projects.md#Satoshi-dice)
2. [Fork monitor](projects.md#Fork-monitor)
3. [Block explorer](projects.md#Block-explorer)
4. [Mempool/fee analysis](projects.md#Mempool-fee-analysis)
5. [P2P network analysis](projects.md#P2P-netowork-analysis)
6. [Transaction propagation](projects.md#Transaction-propagation)
7. [Build your own signet](projects.md#Build-your-own-signet)
8. [Bitcoin paywall](projects.md#Bitcoin-paywall)
9. [Bitkinship](projects.md#Bitkinship)
10. [TABConf wallet overhaul](projects.md#TABConf-wallet-overhaul)

### Tier 2

1. Simulate "push payments" using Bitcoin
2. Improve bitcoin wallet "contact" lists
3. Graph your bitcoin wallet's UTXOs (+ chain analysis)
4. Exchange / remittance service
5. Bitcoin “bank” (hot, warm, cold wallet backend)
6. Chain analysis tool/UI/library
7. [Timelock refresher](projects.md#Timelock-refresher)
8. Multi-sig collaborative custody provider
9. Joinmarket UI

### Satoshi dice

**Outline:** A provably fair gambling application, where payments to and from the casino are made on-chain or in Lightning. See [bitcoin.it/wiki/Satoshi\_Dice](https://en.bitcoin.it/wiki/Satoshi\_Dice) for more background information, and [this Stack Exchange question](https://bitcoin.stackexchange.com/questions/7369/how-to-implement-a-game-like-satoshidice) for a high-level on-chain implementation.

**Format:** Casino server back-end (required); Client application (optional, GUI or CLI)

**BTC/LN topics:** creating and parsing Bitcoin transactions, 0-conf protocols, provable fairness

### Fork monitor

**Outline:** Monitor blockchain and send an alert when a fork (exceeding n blocks) occurs, and another one when it is "resolved" (m blocks ahead)

**Format:** Server back-end; simple front-end or API to subscribe (email, pub/sub, webhooks, ...)

**BTC/LN topics:** chain reorgs, block propagation

### Block explorer

**Outline:** given a block hash, visualize block header and transaction information. Given a transaction hash, visualize input and output information. See e.g. https://blockstream.info/

**Format:** Client application (GUI or CLI)

**BTC/LN topics:** parsing blocks, parsing transactions

### Mempool fee analysis

**Outline:** Create a service which monitors the current state of the mempool with respect to fees. Provide APIs or a GUI which users (and optionally services) can connect to in order to retrieve relevant information. Include facility for users to _upload_ their own transactions via the service.

**Format:** Backend with APIs or front end with GUI

**BTC/LN topics:** transactions, fees, mempool, p2p

### P2P network analysis

**Outline:** Create a service which monitors messages over the P2P network. The service might be able to monitor node information such as user agent, version, services. Connection metrics such as uptime, churn could also be monitored. P2P traffic can also be inspected in order to determine message contents, e.g. transactions, blocks, as well as estimating bandwidth usage per message type. Provide APIs or a GUI which users (and optionally services) can connect to in order to retrieve relevant information.

**Format:** Backend with APIs or front end with GUI

**BTC/LN topics:** P2P, networking, mempool

### Transaction propagation

**Outline:** Create a service which monitors messages over the P2P network from multiple endpoints in order to estimate transaction (and block) propagation times over the network. Consider that many bitcoin nodes may be running only connected to Tor or I2P networks.

**Format:** Backend with APIs or front end with GUI/graphs

**BTC/LN topics:** P2P, networking, mempool

### Build your own signet

**Outline:** Create your own signet network with yourself as the primary "miner". In order to allow other miners to join in the future, use a signet challenge that related to a multisig address. Configure your signet to perform semi-regular re-orgs which can be used to test software in re-org situations. Have someone else connect to your signet either as a miner or a regular node, and start making transactions.

**Format:** Backend/CLI

**BTC/LN topics:** transactions, scripting, re-orgs

### Bitcoin paywall

**Outline:** Implement a paywall which requires a micro-donation of bitcoin to remove. Whilst this style of paywall is largely not practicable on bitcoin mainnet today the implementation could be upgraded in a future project extension to use lightning.

**Format:** Library

**BTC/LN topics:** transactions

### Bitkinship

**Outline:** Given two UTXOs, calculate how related they are

**Format:** Library and CLI

**BTC/LN topics:** transactions

**Bonus:** Given an xPub, calculate relatedness between all UTXOs belonging to xPub.

### Timelock refresher

**Outline:** To ensure your heirs can access your bitcoin after you pass away, all of your P2WSH addresses contain a second spending clause that after 1 year, a second key (held by your heir) can spend all of your outputs. With this program/script, you want to be able to quickly "refresh" all outputs that are coming close to being unlocked, e.g. within 3 months of the second spending path becoming viable. See [https://bitcointalk.org/index.php?topic=5185907.0](https://bitcointalk.org/index.php?topic=5185907.0) for an example of the original setup.

**Format:** Client application, short lived.

**BTC/LN topics:** creating transaction, advanced scripting, timelocks

**Bonus:** multisig instead of single sig; use taproot

### TABConf wallet overhaul

**Outline:** Overhaul the TABConf wallet. This might mean translating into a language you're familiar with and using a different bitcoin wallet library, or

**Format:** Casino server back-end (required); Client application (optional, GUI or CLI)

**BTC/LN topics:** creating and parsing Bitcoin transactions, 0-conf protocols, provable fairness

## Lightning projects

1. [Lightning web store](projects.md#Lightning-web-store) e.g. [starblocks.acinq.co](https://starblocks.acinq.co)
2. Satoshi dice/game
3. Satoshi's place
4. [Network graph visualiser](projects.md#undefined)
5. getAlby hacking
6. Messaging app
7. Something related to social networking
8. [Paywall](projects.md#undefined)
9. LND -> Core Lightning (CLN) database migration tool
10. Exchange / remittance service Look around Galoy for more ideas Ask Galoy
11. [Build your own lightning node](projects.md#Build-your-own-lightning-node) with LDK and accompanying crates (Rust)

{% hint style="info" %}
Where possible, try and use signet. It might be helpful to start off a project with regtest for easy iteration, but ideally it would be great to be able to interact with your projects from our end!
{% endhint %}

### Lightning web store

* **Outline:** Create a web store like [starblocks.acinq.co](https://starblocks.acinq.co) that accepts signet lightning payments. You can sell any virtual products you want!
* **Format:** Web front-end and a backend that communicates with LND

### Network graph visualiser

* **Outline**: Create a web application that shows a visualisation of the lightning network graph on signet. You will need a backend that communicates with LND (or another implementation if you wish) via a REST or equivalent API to get the channels and nodes in the graph. Your web application should update the graph in realtime as nodes and channels are added or removed. You may use [this tutorial](https://bmancini55.github.io/building-lightning/) as a starting point.
* **Format**: Web front-end and a backend that communicates with LND.

### Paywall

* **Outline**: Create a simple paywalled website such as a blog or news site that requires you to pay some small fee in satoshis to be able to access content. One example is a site like [yalls.org](https://yalls.org). It's important that the user does not need to pay more than once (for example, when refreshing their browser) so ensure that there is some way anonymously identify that a user has already paid by having some credential stored in a browser cookie. You can look into using something such as LSATs for this. There are libraries and proxies such as [boltwall](projects.md#javascript) and [aperture](projects.md#go) that can help.

### Build your own lightning node

* **Outline:** Build your own lightning node with the Lightning Development Kit (LDK) following the outline [here](https://lightningdevkit.org/tutorials/build\_a\_node\_in\_rust/). Use your `bitcoind` node (on signet) as a block source and wallet. Additionally, create a CLI tool that can interact with the node via RPCs, like `lncli` does for `lnd`. Your CLI should have commands to:
  * Generate an address to fund your on-chain wallet
  * Connect to a peer
  * List all peers
  * Open a channel with any other lightning node
  * List all channels
  * Create an invoice
  * Pay an invoice
* **Format:** Lightning node with CLI

## Bitcoin/LN libraries and tools you may find useful

The ecosystem of libraries for each language is quite diverse. Here are some of the most popular ones, but it's up to you to search for more. And remember, _don't trust, verify_!

### Rust

* [bitcoin](https://github.com/rust-bitcoin/rust-bitcoin) - Library with support for de/serialisation, parsing and executing on data-structures and network messages related to Bitcoin. You can use this library to create private keys and addresses, for PSBT operations and other nifty things.
* [bdk](https://github.com/bitcoindevkit/bdk) - Bitcoin Development Kit is a modern, lightweight, descriptor-based wallet library written in Rust! If you're looking for a great library with high-level APIs for building a Bitcoin wallet then check this out.
* [bitcoincore-rpc](https://github.com/rust-bitcoin/rust-bitcoincore-rpc) - Contains an implementation of an RPC client that exposes the Bitcoin Core JSON-RPC APIs as rust functions.
* Some crates from [LDK](https://github.com/lightningdevkit/rust-lightning) (check README):
  * **lightning** - The Core of the LDK library, implements the lightning protocol, channel state machine, and on-chain logic. Supports no-std and exposes on relatively low-level interfaces.
  * **lightning-background-processor** - Utilities to perform required background tasks for Rust Lightning.
  * **lightning-block-sync** - Utilities to fetch the chain data from a block source and feed them into Rust Lightning.
  * **lightning-invoice Data** - Structures to parse and serialise BOLT11 lightning invoices.

### Go

* Many in [btcsuite](https://github.com/btcsuite) - Super popular and complete set of packages and tools for working with Bitcoin in Go.
* [lndclient](https://github.com/lightninglabs/lndclient) - A Go native wrapper for `lnd`'s gRPC interface. Useful for interacting with an LND node.
* [aperture](https://github.com/lightninglabs/aperture) - HTTP 402 Lightning Service Authentication Token Reverse Proxy

### JavaScript

* [bitcoinjs-lib](https://github.com/btcsuite) - A JavaScript Bitcoin library for Node.JS and browsers.
* [boltwall](https://github.com/Tierion/boltwall) - Bitcoin Lightning paywall and authentication using LSATs. Built with LND, Nodejs, and TypeScript.

### Python

* [bitcoin-lib](https://github.com/petertodd/python-bitcoinlib) - "The Swiss Army Knife of the Bitcoin protocol." - Wladimir J. van der Laan

### Java

* [bitcoinj](https://github.com/bitcoinj/bitcoinj) - A library for working with Bitcoin in Java.
