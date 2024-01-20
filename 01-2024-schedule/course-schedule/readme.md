---
description: Setting Up a Dev Environment | Mastering Bitcoin Refresher
---

# Week 1

We're going to help you get ready to work with Bitcoin by setting up your developer environments. We'll also go over some important aspects of the Mastering Bitcoin book that are most essential to becoming efficient and effective Bitcoin/LN builders. 

First, we'll learn about Cryptography, exploring Keys, Addresses, and Digital Signatures. Our focus will include understanding how they are derived. We'll also cover Wallet Recovery.

## Prerequisites

We would like you to download some source code and attempt to compile it by following its build instructions. You will find yourself using these software throughout the course.

Please download/clone the following tools/repositories and try to follow and complete their build processes:

| Software     | Repository                                                                         |
| ------------ | ---------------------------------------------------------------------------------- |
| Bitcoin Core | [https://github.com/bitcoin/bitcoin](https://github.com/bitcoin/bitcoin)           |
| LND          | [https://github.com/lightningnetwork/lnd](https://github.com/lightningnetwork/lnd) |
| Polar        | [https://lightningpolar.com/](https://lightningpolar.com)                          |

{% hint style="warning" %}
Don't run `bitcoind` without specifying `regtest` (or `signet`) as the network in the configuration file (`bitcoin.conf`) or as a command line argument (see `bitcoind --help`). Otherwise you will start synchronising blocks for mainnet which is over 400 GB! At this point, you don't even need to run bitcoind just yet.
{% endhint %}

## Goals

<details>

<summary>Become comfortable and proficient in setting up bitcoin developer environments</summary>

</details>

<details>

<summary>Be able to run and interface with Bitcoin Core and LND</summary>

* Understand signet, regtest and testnet.

<!---->

* Connect Bitcoin Core and LND programmatically

<!---->

* Interface with Bitcoin Core and LND using the CLI tools

<!---->

* Programmatic control of bitcoind and LND

<!---->

* Comfortable with running the full test suite(s) of Bitcoin Core

</details>

<details>

<summary>Build a toy bitcoin wallet using a library</summary>

* Add additional functionality of your choosing

</details>

<details>

<summary>Develop a robust understanding of bitcoin topics both in theory and in practice</summary>

* Random number generation

<!---->

* Keys and key material

<!---->

* Derivation paths

<!---->

* Address types

<!---->

* Differences between keys, address and digital signatures

</details>

## Schedule

The Mastering Bitcoin book (3rd edition) can be accessed [here](https://drive.google.com/file/d/1h6YD9XR8-G2MUwpRVSEjwfERIqgsBqb\_/view?usp=sharing). Discussion questions are available on [Btrust Builders' GitHub](https://github.com/Qala-Dev/discussion-questions/tree/main/mastering-bitcoin). An overview of the questions for which you will be the discussion leader will be shared over the usual channels, and the daily discussions will be scheduled on calendar.&#x20;

***

## Monday

1. Introduction to Btrust Builders Programme
2. Programme structure
3. Icebreakers
4. Why we bitcoin
5. Maximizing the builders fellowship

## Tuesday

### Keys and Addresses

| Action                                                                                                                         | Context                                                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Finish reading the chapter(s) for the day                                                                                      | Chapter 4: [Keys, Addresses](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch04.asciidoc)                                           |
| Prepare and research your assigned question(s), make sure you can host the discussion and think about follow-up questions etc. | [Discussion questions](https://github.com/Qala-Dev/discussion-questions/tree/main/mastering-bitcoin#chapter-4) for Chapter 4: Keys, Addresses |
| Attend the study session                                                                                                       | Check your calendar for the meeting information                                                                                               |
| Try out any of the practice activities below                                                                                   | [Practice activities](./#practice-activities)                                                                                                 |


### Practice Activities

These activities assume that you have been able to setup Bitcoin core and the bitcoin-tx-tutorial environment on your system

1. Quick revision of Elliptic Curve Key Generation. [Practice here](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/appendix/elliptic-curve-math-review.ipynb)
   * Develop a good practical understanding of how to generate private and public keys.
   * Develop an understanding of the difference between compressed and uncompressed keys.
   * Supplementary materials:
     * [Search the topic on Learnmeabitcoin](https://learnmeabitcoin.com/)
2. Overview of Addresses. [Practice here](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/appendix/addresses.ipynb)
   * Get a good understanding of how addresses are created from scripts
   * Develop a good understanding of Base58, bech32 and bech32m addresses.
   * Develop an understanding of what differentiate these different address types.
   * Supplementary materials:
     * [Search the topic on Learnmeabitcoin](https://learnmeabitcoin.com/)
3. Learn Bitcoin From The Command Line: [Using the bitcoin CLI](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/blob/master/03\_0\_Understanding\_Your\_Bitcoin\_Setup.md). You are expected to:
   1. Become comfortable working with the bitcoin-cli command-line interface
   2. Create an Address to Receive Bitcoin Funds
   3. Use Basic Wallet Commands
   4. Create an Address to Receive Bitcoin Funds

### Deliverables

{% hint style="success" %}
Take a screenshot of the address you created using the cli, send testnet funds to that address using this [faucet](https://bitcoinfaucet.uo1.net/) and share the screenshot of the transaction on the testnet [explorer](https://mempool.space/testnet) and its balance
{% endhint %}

## Wednesday

### Set-up Bitcoin/Lightning Developer Environment

### Practice Activities

1. Set up a manual Bitcoin and Lightning developer environment on regtest by following the guide from Bitstein: [Setting up a Bitcoin/Lightning test environment](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a)

{% hint style="info" %}
This environment should ideally be built using Bitcoin Core and LND installed by you from source
{% endhint %}

2. Run all Bitcoin Core unit tests
3. Choose area of the codebase you're interested in, pick a functional test that covers it, and then run that test.

{% hint style="info" %}
see documentation in `test/README.md` for clues on how to run individual tests
{% endhint %}

### Deliverables

{% hint style="success" %}
A screenshot of your lightning developer environment resulting from the guide from Bitstein
{% endhint %}

***

## Thursday

### Wallet Recovery

1. Read about Hierarchical Deterministic Wallets in BIP0032.
   * You do not need to read/understand the child key derivation functions.
   * You should conclude with a strong understanding of how parent and child keys are derived from each other, and from a master seed .
   * Supplementary materials:
     * [Learnmeabitcoin: HD Wallets](https://learnmeabitcoin.com/technical/hd-wallets)
2. Read about Mnemonics in BIP0039
   * Understand how to move from a key to Mnemonics.
   * Understand how to move from Mnemonics to keys.
3. Read Key Derivation Paths (BIP 44, BIP 49, BIP 84, BIP 86)
   * Understand all the derivation structures proposed by the different BIPS
   * Supplementary materials:
     * [An Overview of the BIPs that Shape Modern HD Wallets](https://thunderbiscuit.com/posts/modern-wallets/)
     * [Learnmeabitcoin: Derivation Paths](https://learnmeabitcoin.com/technical/derivation-paths)
4. Read about Output/Wallet descriptors (BIP 380 - 386)
   * Understand the purpose of wallet descriptors.
   * Understand how descriptors enhance wallets.
5. Read about the state of [Wallet Recovery](https://walletsrecovery.org/)
   * Understand why some wallets might not be able to recover your balance
   * Understand the dangers of not using BIP standards in your wallet.

### Exercise

1. Build a Bitcoin wallet and make a bitcoin transaction following this programming guide [here](https://medium.com/@bitcoindeezy/bitcoin-basics-programming-with-bitcoinjs-lib-4a69218c0431).
   1. Note that the bitcoin library does not necessarily have to be bitcoinjs-lib, any bitcoin library in the programming language of your choice can achieve the same results
   2. You can add an address functionality that allows you to generate one or more different address types e.g. P2PK, P2PKH, P2SH, P2WPKH, P2WSH, P2TR, for the user to choose from

### Deliverables

{% hint style="success" %}
Take a screenshot of the address you created, the transaction on the testnet faucet and its balance
{% endhint %}

***

### Friday

### Digital Signatures

1. Learn [how digital signatures work](https://learnmeabitcoin.com/beginners/digital\_signatures\_signing\_verifying)&#x20;
   * Learn how to sign a message and verify a signature
2. Learn more about [Elliptic Curve Digital Signature Algorithm (ECDSA) ](https://learnmeabitcoin.com/technical/ecdsa)
   * Learn how this signature algorithm is implemented using the Elliptic curve
3. [Schnorr Signatures](https://www.youtube.com/watch?v=wybiVFdknhg\&list=PLPrDsP88ifOVTEJf\_jQGunDUS05M9GdIC)
   * Understand why they are better than ECDSA
   * Develop an understanding of their linearity property
   * Supplementary Material:
     * [Rene Pickhardt Schnorr Series](https://www.youtube.com/watch?v=n5aompcR9W0\&list=PLaRKlIqjjguCILECVRXqVhec6yaNYyeMT)&#x20;
4. Learn about [SIGHASH](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter4-sighash/sighash-flags.ipynb)
5. [SIGHASH Evolution](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter4-sighash/sighash-evolution.ipynb)

## Learning Resources

<table data-column-title-hidden data-view="cards" data-full-width="false"><thead><tr><th>Name</th><th>Link</th><th data-hidden data-type="content-ref"></th><th data-hidden data-card-cover data-type="files"></th></tr></thead><tbody><tr><td>Setting Up Bitcoin Core and Lightning On Windows using WSL</td><td><a href="https://tobiojuolape.hashnode.dev/preview/63ca548a415abc00080231c5">https://tobiojuolape.hashnode.dev/preview/63ca548a415abc00080231c5</a></td><td></td><td></td></tr><tr><td>Setting Up a Bitcoin and Lightning Daemon on Mac from source</td><td><a href="https://dev.to/timothy_masiko/setting-up-a-bitcoin-and-lightning-network-daemon-on-mac-from-source-17hb">https://dev.to/timothy_masiko/setting-up-a-bitcoin-and-lightning-network-daemon-on-mac-from-source-17hb</a></td><td></td><td></td></tr><tr><td>Lightning Book - Bitcoin Fundamentals review</td><td><a href="https://lnbook.256k1.dev/#bitcoin_fundamentals_review">https://lnbook.256k1.dev/#bitcoin_fundamentals_review</a></td><td></td><td></td></tr><tr><td>BIP0032</td><td><a href="https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki">https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki</a></td><td></td><td></td></tr><tr><td>Learn Bitcoin From The Command Line</td><td><a href="https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line">https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line</a></td><td></td><td></td></tr><tr><td>Bitstein - Setting up a bitcoin lightning network test environment</td><td><a href="https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a">https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a</a></td><td></td><td></td></tr><tr><td>Why Bitcoin Address is not like an account number</td><td><a href="https://sadeeqcode.medium.com/why-bitcoin-address-is-not-like-an-account-number-e5a5261a0605">https://sadeeqcode.medium.com/why-bitcoin-address-is-not-like-an-account-number-e5a5261a0605</a></td><td></td><td></td></tr><tr><td>Learn me a bitcoin</td><td><a href="https://learnmeabitcoin.com/">https://learnmeabitcoin.com/</a></td><td></td><td></td></tr><tr><td>Bitcoin Transaction tutorial</td><td><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial">https://github.com/chaincodelabs/bitcoin-tx-tutorial</a></td><td></td><td></td></tr><tr><td>BIP0039</td><td><a href="https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki">https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki</a></td><td></td><td></td></tr><tr><td>Wallet Recovery</td><td><a href="https://walletsrecovery.org/">https://walletsrecovery.org/</a></td><td></td><td></td></tr><tr><td>BIP0044</td><td><a href="https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki">https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki</a></td><td></td><td></td></tr><tr><td>BIP0049</td><td><a href="https://github.com/bitcoin/bips/blob/master/bip-0049.mediawiki">https://github.com/bitcoin/bips/blob/master/bip-0049.mediawiki</a></td><td></td><td></td></tr><tr><td>BIP0084</td><td><a href="https://github.com/bitcoin/bips/blob/master/bip-0084.mediawiki">https://github.com/bitcoin/bips/blob/master/bip-0084.mediawiki</a></td><td></td><td></td></tr><tr><td>BIP0086</td><td><a href="https://github.com/bitcoin/bips/blob/master/bip-0086.mediawiki">https://github.com/bitcoin/bips/blob/master/bip-0086.mediawiki</a></td><td></td><td></td></tr></tbody></table>
