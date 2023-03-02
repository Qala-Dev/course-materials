---
description: project ideas for Qala development course
---

# Projects

## General

* We are going to be building our own projects and contributing code to existing open source projects over the duration of the course.
* Projects can be built as a front-end application, back end application, API or a command line tool.
* You can use the suggested project list as inspiration for your third project. We want you to work on something that is useful to the community and can be maintained even after the Qala program.
* Please run your own projects past the instructors first so we can check it is suitable and determine which skills it will require and exercise.
* Your first project will involve making use of Lightning Network invoices and payments probably leverage a bitcoin or lightning library or development kit, in order to facilitate fast iteration on end results.
* In your second/third project you should be considering not using a library to do as much of the heavy lifting, so that you can become more comfortable with how bitcoin and lightning work under the hood.

## Mini design document

The first step for all the projects is to create a design document that describes your project / pull request and approach. The goal of this document is to:
- think critically about what your application needs to do and what you'll need to achieve your goals
- ensure the scope is neither too broad nor too narrow
- enable early feedback to prevent spending too much time on an approach that may not be optimal

The design document should contain:
1. A basic outline of the project or PR.
1. Goals and non-goals. Define both what's in-, as well as out of scope.
1. For your application architecture (some of this may not be relevant to PRs):
    1. Components: the building blocks of your application, and which technologies you'll use (e.g. Rust backend and Vue.js frontend)
    1. Interface: which API endpoints, CLI commands or frontend views are required?
    1. Code structure: high-level organization of folders, files, classes
    1. Dependencies: (bitcoind/LND) RPC functions, libraries, ...
1. Introspection: what are the most difficult or risky parts of the project or PR, based on your own assessment of available skills?
1. What milestone you need to reach to consider the project have achieved Minimum Viable Product (MVP) state

**Ensure to maximize your time being able to work on Bitcoin/LN related tasks. Non-critical general software engineering work should be removed from scope as much as possible.**

Please create and share the design document using a collaborative document editor, so that we can add any comments or feedback that we have.
Examples of editors <https://hackmd.io> and <https://docs.google.com>, but you can choose any you're familiar with so long as we can easily log in to comment.


## Project 1 - "Magic internet money 🧙"

The purpose of this project is to demonstrate a basic working knowledge of Bitcoin and Lightning by building a way to accept Magic Internet Money! This project is meant to be simple, but don't worry: there will be plenty of time throughout the rest of the course for more complicated projects.

### Goals

* Demonstrate proficiency working on signet / testnet
* Get experience with writing your first design document
* Build a working payment workflow using either Bitcoin or Lightning
* Address UX challenges users might face

### Deliverables

* A design document
* Working infrastructure on signet / testnet
* A simple application which requires someone to make a payment, either with Bitcoin or Lightning (or both!)
  * This can be built as a front-end application, back end application, API or a command line tool but it must be something a user can interact with
* Confirmation to the user once payment has been received

This project is meant to be simple to allow you to get familiar with the process of writing a design doc and scoping features. Additionally, since you will all be working on the same prompt, you will be able to collaborate with your peers if you run into issues.

### Timeline

* Design document due by Friday, but the sooner the better
* Project demo due the following Friday
  * Projects can still be a work in progress, the goal is to show what you've done so far

## Project 2 - "Welcome to the community 🤗"

You're going to be doing some real contributing to existing open source projects in the wider community. We'll specifically be looking
at project issues labelled as `good first issue`. You'll first have to attend the contributing etiquette workshop as it's very important
we are respectful of maintainers' and other contributors' time and we know how to act appropriately.

### Open Source Project List with Issues

TBC

## Project 3 - "Spread your wings 🦅"

It's come down to this, your final project. Here you're going to get your creativity flowing and work on something really
great and beneficial to the wider Bitcoin community. If this project could be summarised in two words they would be "longevity"
and "impact". We want you to do something meaningful here and make your big debut.

You can use any programming language with which you are familiar. Remember that this project is not meant for learning
a new language, but to build an impactful Bitcoin/Lightning project - you have freedom to choose but don't let it be a barrier
to accomplishing your primary goals!


## Bitcoin projects

Topics to cover: transactions, scripting, reorgs, HD wallets

### Tier 1

1. [Satoshi dice/game](#satoshi-dice)
1. [Fork monitor](#fork-monitor)
1. [Block explorer](#block-explorer)
1. [Mempool/fee analysis](#mempool-fee-analysis)
1. [P2P network analysis](#p2p-network-analysis)
1. [Transaction propagation](#transaction-propagation)
1. [Build your own signet](#build-your-own-signet)
1. [Bitcoin paywall](#bitcoin-paywall)
1. [Bitkinship](#bitkinship)
1. [TABConf wallet overhaul](#tabconf-wallet-overhaul)

### Tier 2

1. [Bitcoin wallet contact lists](#bitcoin-wallet-contact-lists)
1. [Graph wallet UTXOs](#graph-wallet-utxos)
1. [Exchange or remittance service](#exchange-or-remittance-service)
1. [Bitcoin bank](#bitcoin-bank)
1. [Chain analysis](#chain-analysis)
1. [Timelock refresher](#timelock-refresher)
1. [Multi-sig collaborative custody provider](#multi-sig-collaborative-custody-provider)
1. [Joinmarket UI](#joinmarket-ui)

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

### TABConf wallet overhaul

**Outline:** Overhaul the TABConf wallet. This might mean translating into a language you're familiar with and using a different bitcoin wallet library, or upgrading the UX.

**Format:** Casino server back-end (required); Client application (optional, GUI or CLI)

**BTC/LN topics:** creating and parsing Bitcoin transactions, 0-conf protocols, provable fairness

### Bitcoin wallet contact lists

**Outline:** Improve bitcoin wallet "contact" lists by checking for bitcoin privacy best practices which could include coinselection based on the other contacts you’ve interacted with “coins known by…”, “coins known by other contacts” … etc.

When querying a contact, coin or transaction a (JSON?) response could be given which included warnings of address re-use etc.
A pretty comprehensive overview of the commonly-used privacy heuristics can be found [here](https://en.bitcoin.it/wiki/Privacy).

**Format:**

### Graph wallet UTXOs

**Outline:**

**Format:**

### Exchange or remittance service

**Outline:**

**Format:**

### Bitcoin bank

**Outline:** Bitcoin “bank” (hot, warm, cold wallet backend)
A bitcoin bank provides security guarantees for its users by not storing all bitcoins online in a hot wallet.
Instead a scheme should be devised whereby an attacker, even with total remote access to the bank's computers, cannot steal all the bitcoins.
You may want to incorporate threshold multisignature schemes, timeouts, and other scripting capabilities.
You should also decide how partially signed transactions can be communicated between different stages in the bank "vault", creating any required facilities to import/export, verify and sign for them.
The bank will need some nominal amount of its total reserve in a hot wallet to perform everyday operations. Decide on an amount and also consider how hot and cold wallets will be balanced.
Finally, consideration should be given to the privacy of your users and the privacy of your own bank when thinking about implementing any internal UTXO consolidation and transaction batching for user withdrawals.

**Format:** Software to manage the bank wallet. Optional frontend website for users to log in, see their balance and make deposits and withdrawals. If frontend website not provided, backend software should expose API to request transactions and user balances.

### Chain analysis

**Outline:** Perform chain analysis on a set of provided UTXOs (or descriptors).

The collection of UTXOs that form a "wallet" can leak information with use over time. Providing information to users and wallets can help them (or their wallets) to make better decisions about which UTXOs to select in future transactions.

You can read more about "chainalysis" here: [bitcoin privacy with OXT](https://medium.com/oxt-research/understanding-bitcoin-privacy-with-oxt-part-1-4-8177a40a5923) (and the following 3 parts of the blog).
You can see some other implementations of wallet clustering/graphing [here](https://bitquery.io/blog/best-blockchain-analysis-tools-and-software).
A comprehensive overview of the commonly-used heuristics can be found [here](https://en.bitcoin.it/wiki/Privacy).

Decide on what information you want to reveal to the user. Decide which heuristics you'll need and how you will parse the blockchain.

**Format:** Can be an "all-in-one" (with frontend UI), backend only with endpoints, or as a library which other wallets could re-use.

### Timelock refresher

**Outline:** To ensure your heirs can access your bitcoin after you pass away, all of your P2WSH addresses contain a second spending clause that after 1 year, a second key (held by your heir) can spend all of your outputs. With this program/script, you want to be able to quickly "refresh" all outputs that are coming close to being unlocked, e.g. within 3 months of the second spending path becoming viable. See [https://bitcointalk.org/index.php?topic=5185907.0](https://bitcointalk.org/index.php?topic=5185907.0) for an example of the original setup.

**Format:** Client application, short lived.

**BTC/LN topics:** creating transaction, advanced scripting, timelocks

**Bonus:** multisig instead of single sig; use taproot

### Multi-sig collaborative custody provider

**Outline:** Create your own service such as [Casa](https://keys.casa/) that provides secure and collaborative custody of bitcoin. You need to create a 2-of-3 multi-sig wallet where the user holds two of the keys and the service holds one. In this setup, it's impossible for the service to move any user funds as they only posses a single key. In normal operation, the user makes use of both of their own keys and the service just coordinates the signing process. You must also allow the user to ask the service to sign with its key in the event the user does not have access to one of theirs. Allowing a hardware wallet as one of the user keys would be a bonus, where the client can interact with the hardware wallet to sign.

**Format:** Backend service and client (Web/Mobile)

### JoinMarket UI

**Outline:** [JoinMarket](https://github.com/JoinMarket-Org/joinmarket-clientserver) is an implementation of CoinJoin transactions that creates a market of makers who are available to take part in a CoinJoin at any time, and takers who can create a CoinJoin at any time. Your goal is to create a frontend UI for the JoinMarket client server that allows you to interact with JoinMarket in a more user-friendly manner. There is an effort such as [JAM](https://github.com/joinmarket-webui/joinmarket-webui) to do just this!

**Format:** Frontend UI (Web/Mobile)

## Lightning projects

1. [Lightning web store](projects.md#lightning-web-store) e.g. [starblocks.acinq.co](https://starblocks.acinq.co)
1. Satoshi dice/game
1. Satoshi's place
1. [Network graph visualiser](projects.md#undefined)
1. getAlby hacking
1. Messaging app
1. Something related to social networking
1. [Paywall](projects.md#undefined)
1. LND -> Core Lightning (CLN) database migration tool
1. Exchange / remittance service Look around Galoy for more ideas Ask Galoy
1. [Build your own lightning node](projects.md#build-your-own-lightning-node) with LDK and accompanying crates (Rust)
1. A service involving [submarine swaps](#submarine-swaps)

{% hint style="info" %}
Where possible, try and use signet. It might be helpful to start off a project with regtest for easy iteration, but ideally it would be great to be able to interact with your projects from our end!
{% endhint %}

### Lightning web store

**Outline:** Create a web store like [starblocks.acinq.co](https://starblocks.acinq.co) that accepts signet lightning payments. You can sell any virtual products you want!

**Format:** Web front-end and a backend that communicates with LND

### Network graph visualiser

**Outline**: Create a web application that shows a visualisation of the lightning network graph on signet. You will need a backend that communicates with LND (or another implementation if you wish) via a REST or equivalent API to get the channels and nodes in the graph. Your web application should update the graph in real time as nodes and channels are added or removed. You may use [this tutorial](https://bmancini55.github.io/building-lightning/) as a starting point.

**Format**: Web front-end and a backend that communicates with LND.

### Paywall

**Outline**: Create a simple paywalled website such as a blog or news site that requires you to pay some small fee in satoshis to be able to access content. One example is a site like [yalls.org](https://yalls.org). It's important that the user does not need to pay more than once (for example, when refreshing their browser) so ensure that there is some way anonymously identify that a user has already paid by having some credential stored in a browser cookie. You can look into using something such as LSATs for this. There are libraries and proxies such as [boltwall](projects.md#javascript) and [aperture](projects.md#go) that can help.

### Build your own lightning node

**Outline:** Build your own lightning node with the Lightning Development Kit (LDK) following the outline [here](https://lightningdevkit.org/tutorials/build\_a\_node\_in\_rust/). Use your `bitcoind` node (on signet) as a block source and wallet. Additionally, create a CLI tool that can interact with the node via RPCs, like `lncli` does for `lnd`. Your CLI should have commands to:
  * Generate an address to fund your on-chain wallet
  * Connect to a peer
  * List all peers
  * Open a channel with any other lightning node
  * List all channels
  * Create an invoice
  * Pay an invoice

**Format:** Lightning node with CLI

### Submarine Swaps

**Outline:** Build a service that utilises Submarine Swaps between the bitcoin and lightning network.
See the LND submarine swaps [guide](https://docs.lightning.engineering/the-lightning-network/lightning-overview/understanding-submarine-swaps), the ION [technical details](https://wiki.ion.radar.tech/tech/research/submarine-swap), a nice [guide](https://blog.muun.com/a-closer-look-at-submarine-swaps-in-the-lightning-network/) from Muun wallet, the [explanation](https://github.com/submarineswaps/swaps-service/blob/master/docs/chain_swap_script.md#simple-case) from Alex Bosworth's Submarine Swap Service and this great [explainer](https://medium.com/boltzhq/submarine-swaps-c509ce0fb1db) from Boltz, a decentralised swap service.

Also be sure to check out the [Boltz Exchange](https://boltz.exchange/) itself.

**Format:** The service will essentially permit trustless swaps between the bitcoin and lightning network. It can be a website, CLI tool or other accessible service.

## Bitcoin/LN libraries and tools you may find useful

The ecosystem of libraries for each language is quite diverse. Here are some of the most popular ones, but it's up to you to search for more. And remember, _don't trust, verify_!

### Primary languages

The languages we _highly_ encourage you to use for your first projects. All of you have indicated you know at least one of these and so it will make
getting started and peer review much easier. We want to make sure that learning a new language does not get in the way of completing your first project
in a timely manner. There will be ample opportunity to try out something like Go, Rust, and so on in future projects/exercises!

#### JavaScript/TypeScript

* [bitcoinjs-lib](https://github.com/bitcoinjs/bitcoinjs-lib) - A javascript Bitcoin library for node.js and browsers. 
* [bolt11](https://github.com/bitcoinjs/bolt11) - A library for encoding and decoding lightning network payment requests as defined in BOLT #11.
* [bip38](https://github.com/bitcoinjs/bip38) - BIP38 is a standard process to encrypt Bitcoin and crypto currency private keys that is less susceptible to brute force attacks thus protecting the user.
* [bip39](https://github.com/bitcoinjs/bip39) - JavaScript implementation of Bitcoin BIP39: Mnemonic code for generating deterministic keys
* [coinselect](https://github.com/bitcoinjs/coinselect) - An unspent transaction output (UTXO) selection module for bitcoin.
* [bitcoinjs Org](https://github.com/bitcoinjs) - All the above and more!
* [boltwall](https://github.com/Tierion/boltwall) - Bitcoin Lightning paywall and authentication using LSATs. Built with LND, Nodejs, and TypeScript.
* [bcrpc](https://github.com/dgarage/bcrpc) - Tiny Bitcoin RPC wrapper for Node.js.
* [bitcoinerlab/secp256k1](https://github.com/bitcoinerlab/secp256k1) - A library for performing elliptic curve operations on the secp256k1 curve. It is designed to integrate into the BitcoinJS & BitcoinerLAB ecosystems and uses the audited noble-secp256k1 library.
* [bitcoinerlab/descriptors](https://github.com/bitcoinerlab/descriptors) - A JavaScript library for parsing and interpreting Bitcoin descriptors, including those based on the Miniscript language. 

#### Python

* [buidl](https://github.com/buidl-bitcoin/buidl-python) - python3 bitcoin library with no dependencies and extensive test coverage
* [bitcoin-lib](https://github.com/petertodd/python-bitcoinlib) - "The Swiss Army Knife of the Bitcoin protocol." - Wladimir J. van der Laan
* [CLN plugins](https://github.com/lightningd/plugins) - Community curated plugins for core-lightning
* [python-mnemonic](https://github.com/trezor/python-mnemonic) - Mnemonic code for generating deterministic keys, BIP39
* [python-bip380](https://github.com/darosior/python-bip380) - Bitcoin Output Script Descriptors with Miniscript extension - Work in progress, ready for hacking and contributions welcomed.

### Other languages

We only encourage moving onto these languages after your first project, unless you have made an arrangement with one of the teachers.

#### Java

* [bitcoinj](https://github.com/bitcoinj/bitcoinj) - A library for working with Bitcoin in Java.

#### Rust

* [bitcoin](https://github.com/rust-bitcoin/rust-bitcoin) - Library with support for de/serialisation, parsing and executing on data-structures and network messages related to Bitcoin. You can use this library to create private keys and addresses, for PSBT operations and other nifty things.
* [bdk](https://github.com/bitcoindevkit/bdk) - Bitcoin Development Kit is a modern, lightweight, descriptor-based wallet library written in Rust! If you're looking for a great library with high-level APIs for building a Bitcoin wallet then check this out.
* [bitcoincore-rpc](https://github.com/rust-bitcoin/rust-bitcoincore-rpc) - Contains an implementation of an RPC client that exposes the Bitcoin Core JSON-RPC APIs as rust functions.
* Some crates from [LDK](https://github.com/lightningdevkit/rust-lightning) (check README):
  * **lightning** - The Core of the LDK library, implements the lightning protocol, channel state machine, and on-chain logic. Supports no-std and exposes on relatively low-level interfaces.
  * **lightning-background-processor** - Utilities to perform required background tasks for Rust Lightning.
  * **lightning-block-sync** - Utilities to fetch the chain data from a block source and feed them into Rust Lightning.
  * **lightning-invoice Data** - Structures to parse and serialise BOLT11 lightning invoices.

#### Go

* Many in [btcsuite](https://github.com/btcsuite) - Super popular and complete set of packages and tools for working with Bitcoin in Go.
* [lndclient](https://github.com/lightninglabs/lndclient) - A Go native wrapper for `lnd`'s gRPC interface. Useful for interacting with an LND node.
* [aperture](https://github.com/lightninglabs/aperture) - HTTP 402 Lightning Service Authentication Token Reverse Proxy
