---
description: Building on bitcoin and setting up a dev environment
---

# Week 1

## Prerequisites

We would like you to download some source code and attempt to compile it by following its build instructions before the course begins. This is to prevent any delays when starting on the day.

Please download/clone the following tools/repositories and try to follow and complete their build processes:

| Software       | Repository                                                                                   |
| -------------- | -------------------------------------------------------------------------------------------- |
| TABconf wallet | [https://github.com/KayBeSee/tabconf-workshop](https://github.com/KayBeSee/tabconf-workshop) |
| Bitcoin Core   | [https://github.com/bitcoin/bitcoin](https://github.com/bitcoin/bitcoin)                     |
| LND            | [https://github.com/lightningnetwork/lnd](https://github.com/lightningnetwork/lnd)           |
| Polar          | [https://lightningpolar.com/](https://lightningpolar.com)                                    |

{% hint style="warning" %}
Don't run `bitcoind` without specifying `regtest` (or `signet`) as the network in the configuration file (`bitcoin.conf`) or as a command line argument (see `bitcoind --help`). Otherwise you will start synchronising blocks for mainnet which is over 400 GB! At this point, you don't even need to run bitcoind just yet.
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

## Wednesday - Friday

### Resources

| Name                                                               | Link                                                                                                                                                                                                   |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| BIP0032                                                            | [https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)                                                                       |
| TABConf 2021 Building Your own bitcoin wallet with BitcoinJS       | [https://youtu.be/Bwz2P2hPVpk](https://youtu.be/Bwz2P2hPVpk)                                                                                                                                           |
| Bitstein - Setting up a bitcoin lightning network test environment | [https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a) |

### Exercises

1. Read the Mastering Lightning book [appendix on bitcoin transactions](https://github.com/lnbook/lnbook/blob/develop/appendix_bitcoin_fundamentals_review.asciidoc#bitcoin-transactions).
1. Read about Hierarchical Deterministic Wallets in BIP0032.
   * You do not need to read/understand the child key derivation functions.
   * You should conclude with a strong understanding of how parent and child keys are derived from each other, and from a master seed .
1. Run through the TABconf wallet demo video found in the link above, following along with the demonstration.
1. Set up a manual bitcoin and lightning developer environment on regtest by following the guide from Bitstein: [Setting up a Bitcoin/Lightning test environment](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a)
   * Note, this environment should ideally be built using Bitcoin Core and LND which have been build from source by yourself.
1. Run all Bitcoin Core unit tests
1. Choose area of the codebase you're interested in, pick a functional test that covers it, and then run that test
   * hint: see documentation in `test/README.md` for clues on how to run individual tests)
1. OPTIONAL: Set up a simulated Lightning Network with Polar using at least three lightning nodes with two channels connecting them.
   * Try create some invoices and paying them. See how the balances of the channels change.
   * Play around a bit and expand your network. Try adding some more nodes.
   * NOTE: Knowing your way around Polar will be useful for upcoming weeks' exercises as we'll be using it as
     part of our development environment.

### Deliverables

1. TABConf: please send us file: `src/util/bitcoinjs-lib.ts`.
1. Screenshot of your lightning developer environment resulting from the guide from Bitstein.
1. Screenshot of your simulated lightning network on Polar.
1. A P2WPKH transaction in hex format

