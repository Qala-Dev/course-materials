---
description: Beginning to build on bitcoin
---

# Week 1

### Preparation

We would like you to download some source code and attempt to compile it by following its build instructions before the course begins. This is to prevent and delays when starting on the day.

Please download the following repositories and try to follow and complete their build processes:

| Software       | Repository                                                                                   |
| -------------- | ---------------------------------------------------------------------------------------------|
| Bitcoin Core   | [https://github.com/bitcoin/bitcoin](https://github.com/bitcoin/bitcoin)                     |
| LND            | [https://github.com/lightningnetwork/lnd](https://github.com/lightningnetwork/lnd)           |
| TABconf wallet | [https://github.com/KayBeSee/tabconf-workshop](https://github.com/KayBeSee/tabconf-workshop) |
| Polar          | [https://lightningpolar.com/](https://lightningpolar.com/)                                   |
| NodeJS         | [https://nodejs.org/en/download/](https://nodejs.org/en/download/)                           |

### Goals

* Discuss and understand bitcoin philosophy
* Become comfortable and proficient in setting up bitcoin developer environments
* Be able to run and interface with Bitcoin Core and LND
  * Understand signet and regtest
  * Connect Bitcoin Core and LND programmatically
  * Interface with Bitcoin Core and LND using the CLI tools
  * Programmatic control of bitcoind and LND
  * Comfortable with running the full test suite(s) of Bitcoin Core and LND
* Build a toy bitcoin wallet using a library
  * Add additional functionality of your choosing
  *
* Develop a robust understanding of bitcoin topics both in theory and in practice:
  * Random number generation
  * Keys and key material
  * Derivation paths
  * Address types
  * Coin selection
* Gain experience with developing and using a Bitcoin wallet UI

### Wednesday

#### Resources

| Name                                                               | Link                                                                                             |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| TABConf 2021 Building Your own bitcoin wallet with BitcoinJS       | https://youtu.be/Bwz2P2hPVpk                                                                     |
| Lightning Book - Bitcoin Fundamentals review                       | https://lnbook.256k1.dev/#bitcoin\_fundamentals\_review                                          |
| BIP0032                                                            | https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki                                   |
| Bitstein - Setting up a bitcoin lightning network test environment | https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a|

#### Exercises

1. Run through the TABconf wallet demo video found in the link above, following along with the demonstration.
2. Read about Hierarchical Deterministic Wallets in BIP0032.
   1. You do not need to read/understand the child key derivation functions.
   2. You should conclude with a strong understanding of how parent and child keys are derived from each other, and from a master seed .
3. Set up a manual bitcoin and lightning developer environment on regtest by following the guide from Bitstein: [Setting up a Bitcoin/Lightning test environment](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a)
   1. Note, this environment should be using Bitcoin Core and LND which have been build from source by yourself.
4. If you finish all of the above, you can continue your progression by following the "TABConf wallet expansion" on [Thursday](week-1.md#thursday)

### Thursday

1. TABConf wallet expansion
   * Add functionality to the wallet:
     1. one or more different recieve address types, e.g. P2PK, P2PKH, P2SH, P2WPKH, P2WSH
     2. Add a watch-only wallet mode
        * i.e. ability to import an xPub
     3. Add full backup and restore functionality
        * i.e. ability to import and export seed (and optionally xPub, yPub, zPub)
     4. Improve UI/UX for a user who has many different sub-wallets derived from their seed
     5. Add ability to perform coin selection when sending payments
2. Bonus: Setup Bitcoin Core to use signet. Manually construct a uni-directional payment channel opening transaction with an instructor and produce (off-chain) update transactions for 3 purchases, and send us the transactions in hex format.



