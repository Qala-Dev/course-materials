---
description: Building on bitcoin and setting up a dev environment
---

# Week 1

## Prerequisites

We would like you to download some source code and attempt to compile it by following its build instructions before the course begins. This is to prevent any delays when starting on the day.

Please download the following repositories and try to follow and complete their build processes:

| Software       | Repository                                                                                   |
| -------------- | -------------------------------------------------------------------------------------------- |
| NodeJS         | [https://nodejs.org/en/download/](https://nodejs.org/en/download/)                           |
| TABconf wallet | [https://github.com/KayBeSee/tabconf-workshop](https://github.com/KayBeSee/tabconf-workshop) |
| Bitcoin Core   | [https://github.com/bitcoin/bitcoin](https://github.com/bitcoin/bitcoin)                     |
| LND            | [https://github.com/lightningnetwork/lnd](https://github.com/lightningnetwork/lnd)           |
| Polar          | [https://lightningpolar.com/](https://lightningpolar.com)                                    |

{% hint style="warning" %}
Don't run `bitcoind` without specifying `regtest` (or `signet`) as the network in the configuration file (`bitcoin.conf`) or as a command line argument (see `bitcoind --help`). At this point, you don't even need to run it just yet.
{% endhint %}

## Goals

* Discuss and understand bitcoin philosophy
* Become comfortable and proficient in setting up bitcoin developer environments
* Be able to run and interface with Bitcoin Core and LND
  * Understand signet and regtest
  * Connect Bitcoin Core and LND programmatically
  * Interface with Bitcoin Core and LND using the CLI tools
  * Programmatic control of bitcoind and LND
  * Comfortable with running the full test suite(s) of Bitcoin Core
* Build a toy bitcoin wallet using a library
  * Add additional functionality of your choosing
* Develop a robust understanding of bitcoin topics both in theory and in practice:
  * Random number generation
  * Keys and key material
  * Derivation paths
  * Address types
  * Coin selection
* Gain experience with developing and using a Bitcoin wallet UI

## Monday & Tuesday

1. Introduction to Qala
2. Programme structure
3. Icebreakers
4. Bitcoin Philosophy
5. Why we bitcoin

## Wednesday

### Resources

| Name                                                               | Link                                                                                                                                                                                                   |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Lightning Book - Bitcoin Fundamentals review                       | [https://lnbook.256k1.dev/#bitcoin\_fundamentals\_review](https://lnbook.256k1.dev/#bitcoin\_fundamentals\_review)                                                                                     |
| BIP0032                                                            | [https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)                                                                       |
| TABConf 2021 Building Your own bitcoin wallet with BitcoinJS       | [https://youtu.be/Bwz2P2hPVpk](https://youtu.be/Bwz2P2hPVpk)                                                                                                                                           |
| Bitstein - Setting up a bitcoin lightning network test environment | [https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a) |

### Exercises

1. Read the Mastering Lightning book appendix on bitcoin transactions.
   * The username:password to access the book is: `qala:lightning`
2. Read about Hierarchical Deterministic Wallets in BIP0032.
   * You do not need to read/understand the child key derivation functions.
   * You should conclude with a strong understanding of how parent and child keys are derived from each other, and from a master seed .
3. Run through the TABconf wallet demo video found in the link above, following along with the demonstration.
4. Set up a manual bitcoin and lightning developer environment on regtest by following the guide from Bitstein: [Setting up a Bitcoin/Lightning test environment](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a)
   * Note, this environment should be using Bitcoin Core and LND which have been build from source by yourself.
5. If you finish all of the above, you can continue your progression by following the "TABConf wallet expansion" on [Thursday](week-1.md#thursday)

## Thursday

### Exercises

1. TABConf wallet expansion. Add some or all of the following functionality to the wallet:
   1. one or more different receive address types, e.g. P2PK, P2PKH, P2SH, P2WPKH, P2WSH, for the user to choose from
   2. Add a "watch-only wallet" mode
   3. Add full backup and restore functionality
   4. Improve UI/UX for a user who has many different sub-wallets derived from their seed
   5. Add ability to perform coin selection when sending payments
2. Bonus: Setup Bitcoin Core to use signet. Manually construct a transaction that could represent a 'uni-directional payment channel opening transaction' with an instructor, and produce (off-chain) update transactions for 3 purchases in hex format and send them to us.

## Friday

### Exercises

* Run Bitcoin Core, which has been built from source, in Signet mode
* Run all Bitcoin Core unit tests
* Choose area of the codebase you're interested in, pick a functional test that covers it, and then run that test
* Follow through the Bitcoin Core v23.0 [Release Candidate Testing Guide](https://github.com/bitcoin-core/bitcoin-devwiki/wiki/23.0-Release-Candidate-Testing-Guide), report any bugs or issue that you find to the Bitcoin Core GitHub issue tracker.
  * You might find answers to questions you have in the meeting logs for a bitcoin-core-pre-review (club) meeting held on the guide: [meeting log](https://bitcoincore.reviews/v23-rc-testing).
* Send a regular P2WPKH tx to an instructor on signet.
* Run the [Miner simulation](https://chaincode.gitbook.io/seminars/bitcoin-protocol-development/mining-network-prop#optional-practical-exercise) optional exercise.
* Connect to the Bitcoin Network using [tinybitcoinpeer](https://github.com/willcl-ark/tinybitcoinpeer).
  * Extend the functionality of tinybitcoinpeer to do something interesting!
* BONUS: Modify bitcoind User Agent string in the source code and recompile
* OPTION: Interact with a Signet instance of [LightningK0ala/satoshis.place](https://github.com/LightningK0ala/satoshis.place)
