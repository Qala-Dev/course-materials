---
description: Setting Up a Dev Environment | Mastering Bitcoin Refresher
---

# Week 1

We're going to help you get ready to work with Bitcoin by setting up your developer environments. We'll also go over some important aspects of the Mastering Bitcoin book that are most essential to becoming efficient and effective Bitcoin/LN builders. Essentially, we will be covering Keys, Addresses, Digital Signatures and Wallet Recovery.

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

* Keys and key derivation

<!---->

* Derivation paths

<!---->

* Address types

<!---->

* Differences between keys, address and digital signatures

</details>

<details>

<summary>Wallet Recovery</summary>

* Understand Hierarchical Deterministic Wallets (BIP0032).

<!---->

* Read about Mnemonics (BIP0039), understanding how to move from key to Mnemonics and vice versa.

<!---->

* Understand Key Derivation Paths (BIP 44, BIP 49, BIP 84, BIP 86) and the derivation structures proposed by the different BIPS

<!---->

* Read about Output/Wallet descriptors (BIP 380 - 386) and understand the purpose of wallet descriptors.

<!---->

* Read about Wallet Recovery

</details>

<details>

<summary>Digital Signatures</summary>

* Learn how digital signatures work and how to sign a message and verify a signature

<!---->

* Learn Elliptic Curve Digital Signature Algorithm (ECDSA)

<!---->

* Study Schnorr Signatures and understand why they are better than ECDSA, and their linearity property
* Learn about SIGHASH and it's Evolution

</details>

## Reading and Discussion

The Mastering Bitcoin book (3rd edition) can be accessed [here](https://drive.google.com/file/d/1h6YD9XR8-G2MUwpRVSEjwfERIqgsBqb\_/view?usp=sharing). Discussion questions are available on [Btrust Builders' GitHub](https://github.com/Qala-Dev/discussion-questions/tree/main/mastering-bitcoin). An overview of the questions for which you will be the discussion leader will be shared over the usual channels, and the daily discussions will be scheduled on calendar.

***

| Action                                                                                                                         | Context                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Finish reading the chapter(s) for the day                                                                                      | <p>Chapter 4: Keys, Addresses<br>Chapter 5: Wallet Recovery<br>Chapter 8: Digital Signatures</p>                                                                                                                                                                                                                                                                                                                                                      |
| Prepare and research your assigned question(s), make sure you can host the discussion and think about follow-up questions etc. | <p>Discussion questions for; <br>- <a href="https://github.com/Qala-Dev/discussion-questions/tree/main/mastering-bitcoin#chapter-4">Chapter 4: Keys, Addresses</a><br>- <a href="https://github.com/Qala-Dev/discussion-questions/tree/main/mastering-bitcoin#chapter-5">Chapter 5: Wallet Recovery</a> <br>- <a href="https://github.com/Qala-Dev/discussion-questions/tree/main/mastering-bitcoin#chapter-8">Chapter 8: Digital Signatures</a> </p> |
| Attend the study session                                                                                                       | Check your calendar for the meeting information                                                                                                                                                                                                                                                                                                                                                                                                       |
| Try out any of the practice activities below                                                                                   | [Practice activities](week-1.md#practice-activities)                                                                                                                                                                                                                                                                                                                                                                                                  |

## Schedule: Topics, Goals and Resources

<table><thead><tr><th width="198.33333333333331">Topic</th><th width="295">Goals</th><th>Resources</th></tr></thead><tbody><tr><td>Wallet Recovery</td><td>Understand: Hierarchical Deterministic Wallets<br>Child key derivation functions<br>How parent and child keys are derived from each other, and from a master seed<br>Mnemonics<br>Derivation Paths<br>Output/Wallet descriptors<br></td><td><a href="https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki">BIP32</a><br><a href="https://learnmeabitcoin.com/technical/hd-wallets">HD Wallets</a><br><a href="https://thunderbiscuit.com/posts/modern-wallets/">An Overview of the BIPs that Shape Modern HD Wallets</a><br><a href="https://learnmeabitcoin.com/technical/derivation-paths">Learnmeabitcoin: Derivation Paths</a><br><a href="https://walletsrecovery.org/">state of Wallet Recovery</a></td></tr><tr><td>Digital Signatures</td><td>Understand: How digital signatures work<br>how to sign a message and verify a signature<br>Elliptic Curve Ditigal Signature Algorithm (ECDSA)<br>Schnorr Signatures<br>SIGHASH</td><td><a href="https://learnmeabitcoin.com/beginners/digital_signatures_signing_verifying">Digital Signatures</a><br><a href="https://learnmeabitcoin.com/technical/ecdsa">Elliptic Curve Ditigal Signature Algorithm (ECDSA)</a><br><a href="https://www.youtube.com/watch?v=wybiVFdknhg&#x26;list=PLPrDsP88ifOVTEJf_jQGunDUS05M9GdIC">Schnorr Signatures</a><br><a href="https://www.youtube.com/watch?v=n5aompcR9W0&#x26;list=PLaRKlIqjjguCILECVRXqVhec6yaNYyeMT">Rene Pickhardt Schnorr Series</a><br><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter4-sighash/sighash-flags.ipynb">SIGHASH</a><br><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter4-sighash/sighash-evolution.ipynb">SIGHASH Evolution</a></td></tr></tbody></table>

### Practice Activities

1. Mastering Bitcoin Activities: These activities assume that you have been able to setup Bitcoin core and the bitcoin-tx-tutorial environment on your system

* Quick revision of Elliptic Curve Key Generation. [Practice here](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/appendix/elliptic-curve-math-review.ipynb)
  * Develop a good practical understanding of how to generate private and public keys.
  * Develop an understanding of the difference between compressed and uncompressed keys.
  * Supplementary materials:
    * [Search the topic on Learnmeabitcoin](https://learnmeabitcoin.com/)
* Overview of Addresses. [Practice here](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/appendix/addresses.ipynb)
  * Get a good understanding of how addresses are created from scripts
  * Develop a good understanding of Base58, bech32 and bech32m addresses.
  * Develop an understanding of what differentiate these different address types.
  * Supplementary materials:
    * [Search the topic on Learnmeabitcoin](https://learnmeabitcoin.com/)
* Learn Bitcoin From The Command Line: [Using the bitcoin CLI](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/blob/master/03\_0\_Understanding\_Your\_Bitcoin\_Setup.md). You are expected to:
  * Become comfortable working with the bitcoin-cli command-line interface
  * Create an Address to Receive Bitcoin Funds
  * Use Basic Wallet Commands
  * Create an Address to Receive Bitcoin Funds

2. Setting up Bitcoin/LN Environment Activities:

* Set up a manual Bitcoin and Lightning developer environment on regtest by following the guide from Bitstein: [Setting up a Bitcoin/Lightning test environment](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a)

{% hint style="info" %}
This environment should ideally be built using Bitcoin Core and LND installed by you from source
{% endhint %}

* Run all Bitcoin Core unit tests
* Choose area of the codebase you're interested in, pick a functional test that covers it, and then run that test.

{% hint style="info" %}
see documentation in `test/README.md` for clues on how to run individual tests
{% endhint %}

### Exercises

1. Build a Bitcoin wallet and make a bitcoin transaction following this programming guide [here](https://medium.com/@bitcoindeezy/bitcoin-basics-programming-with-bitcoinjs-lib-4a69218c0431).
   * Note that the bitcoin library does not neccesarily have to be bitcoinjs-lib, any bitcoin library in the programming language of your choice can achieve the same results
   * You can add an address functionality that allows you to generate one or more different address types e.g. P2PK, P2PKH, P2SH, P2WPKH, P2WSH, P2TR, for the user to choose from
2. Set up a manual Bitcoin and Lightning developer environment on regtest by following the guide from Bitstein: [Setting up a Bitcoin/Lightning test environment](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a)
   * Note, this environment should ideally be built using Bitcoin Core and LND which have been build from source by yourself.
3. Run all Bitcoin Core unit tests
4. Choose area of the codebase you're interested in, pick a functional test that covers it, and then run that test
   * hint: see documentation in `test/README.md` for clues on how to run individual tests)

### Deliverables

1. Take a screenshot of the address you created using the cli, send testnet funds to that address using this [faucet](https://bitcoinfaucet.uo1.net/) and share the screenshot of the transaction on the testnet [explorer](https://mempool.space/testnet) and its balance
2. Screenshot of your lightning developer environment resulting from the guide from Bitstein.
3. Take a screenshot of the address you created, the transaction on the testnet faucet and its balance

## Learning Resources

| Name                                                               | Link                                                                                                                                                                                                                 |
| ------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Setting Up Bitcoin Core and Lightning On Windows using WSL         | [https://tobiojuolape.hashnode.dev/preview/63ca548a415abc00080231c5](https://tobiojuolape.hashnode.dev/preview/63ca548a415abc00080231c5)                                                                             |
| Setting Up a Bitcoin and Lightning Daemon on Mac from source       | [https://dev.to/timothy\_masiko/setting-up-a-bitcoin-and-lightning-network-daemon-on-mac-from-source-17hb](https://dev.to/timothy\_masiko/setting-up-a-bitcoin-and-lightning-network-daemon-on-mac-from-source-17hb) |
| Lightning Book - Bitcoin Fundamentals review                       | [https://lnbook.256k1.dev/#bitcoin\_fundamentals\_review](https://lnbook.256k1.dev/#bitcoin\_fundamentals\_review)                                                                                                   |
| BIP0032                                                            | [https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)                                                                                     |
| Learn Bitcoin From The Command Line                                | [https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line)                                                           |
| Bitstein - Setting up a bitcoin lightning network test environment | [https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a)               |
| Why Bitcoin Addreess is not like an account number                 | [https://sadeeqcode.medium.com/why-bitcoin-address-is-not-like-an-account-number-e5a5261a0605](https://sadeeqcode.medium.com/why-bitcoin-address-is-not-like-an-account-number-e5a5261a0605)                         |
| Learn me a bitcoin                                                 | [https://learnmeabitcoin.com/](https://learnmeabitcoin.com/)                                                                                                                                                         |
| Bitcoin Transaction tutorial                                       | [https://github.com/chaincodelabs/bitcoin-tx-tutorial](https://github.com/chaincodelabs/bitcoin-tx-tutorial)                                                                                                         |
| BIP0039                                                            | [https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki)                                                                                     |
| Wallet Recovery                                                    | [https://walletsrecovery.org/](https://walletsrecovery.org/)                                                                                                                                                         |
| BIP0044                                                            | [https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki)                                                                                     |
| BIP0049                                                            | [https://github.com/bitcoin/bips/blob/master/bip-0049.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0049.mediawiki)                                                                                     |
| BIP0084                                                            | [https://github.com/bitcoin/bips/blob/master/bip-0084.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0084.mediawiki)                                                                                     |
| BIP0086                                                            | [https://github.com/bitcoin/bips/blob/master/bip-0086.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0086.mediawiki)                                                                                     |
