---
description: Keys and Addresses, Wallet Recovery and Digital Signatures
---

# Week 1

We will start off with studying Cryptography. We will look at Keys and Addresses and Digital Signatures. We will also study how they are derived. We will also be studying Wallet Recovery.

## Prerequisites

We would like you to download some source code and attempt to compile it by following its build instructions. You will find yourself using these softwares throughout 
the course.

Please download/clone the following tools/repositories and try to follow and complete their build processes:

| Software       | Repository                                                                                   |
| -------------- | -------------------------------------------------------------------------------------------- |
| Bitcoin Core   | [https://github.com/bitcoin/bitcoin](https://github.com/bitcoin/bitcoin)                     |
| LND            | [https://github.com/lightningnetwork/lnd](https://github.com/lightningnetwork/lnd)           |
| Polar          | [https://lightningpolar.com/](https://lightningpolar.com)                                    |

{% hint style="warning" %}
Don't run `bitcoind` without specifying `regtest` (or `signet`) as the network in the configuration file (`bitcoin.conf`) or as a command line argument (see `bitcoind --help`). Otherwise you will start synchronising blocks for mainnet which is over 400 GB! At this point, you don't even need to run bitcoind just yet.
{% endhint %}


## Goals

* Become comfortable and proficient in setting up bitcoin developer environments
* Be able to run and interface with Bitcoin Core and LND
  * Understand signet, regtest and testnet.
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
  * The differences between keys, address and digital signatures


## Schedule: Topics, Goals and Resources

| Topic     | Goals                   | Resources                                                            |
|-----------|-------------------------|----------------------------------------------------------------------|
| Keys and Addresses | Understand: How to Generate Private and Public Keys <br/> Difference between compressed and uncompressed keys |  [Elliptic Curve Key Generation](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/appendix/elliptic-curve-math-review.ipynb) <br/> [Private Keys](https://learnmeabitcoin.com/beginners/private_keys)|
| Overview of Addresses | Understand: How addresses are created from scripts <br/> Address formats: Base58, bech32 and bech32m and their differences | [Addresses](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/appendix/addresses.ipynb)  <br/> [Keys and Addresses](https://learnmeabitcoin.com/beginners/keys_addresses)|
| Bitcoin CLI | Using the Bitcoin Cli <br/> Create an Address to Receive Bitcoin Funds <br/> Basic Wallet Commands | [Using the bitcoin CLI](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/blob/master/03_0_Understanding_Your_Bitcoin_Setup.md) |
| Wallet Recovery | Understand:  Hierarchical Deterministic Wallets <br/> child key derivation functions <br/> parent and child keys are derived from each other, and from a master seed <br/>  Mnemonics <br/> Derivation Paths  <br/> Output/Wallet descriptors <br/> | [BIP32](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki) <br/> [HD Wallets](https://learnmeabitcoin.com/technical/hd-wallets) <br/> [An Overview of the BIPs that Shape Modern HD Wallets](https://thunderbiscuit.com/posts/modern-wallets/)  <br/> [Learnmeabitcoin: Derivation Paths](https://learnmeabitcoin.com/technical/derivation-paths) <br/> [state of Wallet Recovery](https://walletsrecovery.org/)|
| Digital Signatures | Understand: How digital signatures work <br/>  how to sign a message and verify a signature <br/> Elliptic Curve Ditigal Signature Algorithm (ECDSA) <br/> Schnorr Signatures <br/> SIGHASH | [Digital Signatures](https://learnmeabitcoin.com/beginners/digital_signatures_signing_verifying) <br/> [Elliptic Curve Ditigal Signature Algorithm (ECDSA)](https://learnmeabitcoin.com/technical/ecdsa) <br/> [Schnorr Signatures ](https://www.youtube.com/watch?v=wybiVFdknhg&list=PLPrDsP88ifOVTEJf_jQGunDUS05M9GdIC) <br/> [Rene Pickhardt Schnorr Series](https://www.youtube.com/watch?v=n5aompcR9W0&list=PLaRKlIqjjguCILECVRXqVhec6yaNYyeMT) <br/> [SIGHASH](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter4-sighash/sighash-flags.ipynb) <br/> [SIGHASH Evolution](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter4-sighash/sighash-evolution.ipynb) |



### Exercise

1. Build a Bitcoin wallet and make a bitcoin transaction following this programming guide [here](https://medium.com/@bitcoindeezy/bitcoin-basics-programming-with-bitcoinjs-lib-4a69218c0431). 
    1. Note that the bitcoin library does not neccesarily have to be bitcoinjs-lib, any bitcoin library in the programming language of your choice can achieve the same results
    2. You can add an address functionality that allows you to generate one or more different address types e.g. P2PK, P2PKH, P2SH, P2WPKH, P2WSH, P2TR, for the user to choose from
2. Set up a manual Bitcoin and Lightning developer environment on regtest by following the guide from Bitstein: [Setting up a Bitcoin/Lightning test environment](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a)
   * Note, this environment should ideally be built using Bitcoin Core and LND which have been build from source by yourself.
3. Run all Bitcoin Core unit tests
4. Choose area of the codebase you're interested in, pick a functional test that covers it, and then run that test
   * hint: see documentation in `test/README.md` for clues on how to run individual tests)



### Deliverables

1. Take a screenshot of the address you created using the cli, send testnet funds to that address using this [faucet](https://bitcoinfaucet.uo1.net/) and share the screenshot of the transaction on the testnet [explorer](https://mempool.space/testnet) and its balance

2. Screenshot of your lightning developer environment resulting from the guide from Bitstein.

1. Take a screenshot of the address you created, the transaction on the testnet faucet and its balance



## Learning Resources

| Name                                                               | Link                                                                                                                                                                                                   |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Setting Up Bitcoin Core and Lightning On Windows using WSL | [https://tobiojuolape.hashnode.dev/preview/63ca548a415abc00080231c5](https://tobiojuolape.hashnode.dev/preview/63ca548a415abc00080231c5)|
| Setting Up a Bitcoin and Lightning Daemon on Mac from source | [https://dev.to/timothy_masiko/setting-up-a-bitcoin-and-lightning-network-daemon-on-mac-from-source-17hb](https://dev.to/timothy_masiko/setting-up-a-bitcoin-and-lightning-network-daemon-on-mac-from-source-17hb)|
| Lightning Book - Bitcoin Fundamentals review                       | [https://lnbook.256k1.dev/#bitcoin\_fundamentals\_review](https://lnbook.256k1.dev/#bitcoin\_fundamentals\_review)                                                                                     |
| BIP0032                                                            | [https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)                                                                       |
| Learn Bitcoin From The Command Line | [https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line)|
| Bitstein - Setting up a bitcoin lightning network test environment | [https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a) |
| Why Bitcoin Addreess is not like an account number | [https://sadeeqcode.medium.com/why-bitcoin-address-is-not-like-an-account-number-e5a5261a0605](https://sadeeqcode.medium.com/why-bitcoin-address-is-not-like-an-account-number-e5a5261a0605)|
| Learn me a bitcoin | [https://learnmeabitcoin.com/](https://learnmeabitcoin.com/)|
| Bitcoin Transaction tutorial | [https://github.com/chaincodelabs/bitcoin-tx-tutorial](https://github.com/chaincodelabs/bitcoin-tx-tutorial)|
| BIP0039   | [https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki)|
| Wallet Recovery | [https://walletsrecovery.org/](https://walletsrecovery.org/)|
| BIP0044   | [https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki)|
| BIP0049   | [https://github.com/bitcoin/bips/blob/master/bip-0049.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0049.mediawiki)|
| BIP0084   | [https://github.com/bitcoin/bips/blob/master/bip-0084.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0084.mediawiki)|
| BIP0086   | [https://github.com/bitcoin/bips/blob/master/bip-0086.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0086.mediawiki)|
