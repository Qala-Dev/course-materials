---
description: Transactions, Authorization and Authentication
---

# Week 2

This week, we'll be studying Bitcoin Transactions. We will cover the structure of a Bitcoin Transaction and explore locking and unlocking scripts in a Bitcoin Transaction.

## Prerequisites

* You are expected to have completed Keys and Addresses as well as Digital Signatures. Additionally, we hoped that you've learned Schnorr Signatures and TapTweaks. 

## Goals

At the end of the week, we hope that you will:

* Understand the structure of a Bitcoin Transaction
    * Version
    * Inputs
    * Outputs
    * Locktime
* Learn Fundamental Concepts of Scripts
    * Opcodes
    * Parsing Scripts
    * Standard Scripts:
        * P2PK
        * P2PKH
        * P2SH
        * P2WPKH
        * P2WSH
* Learn How to Create Bitcoin Transaction
    * Legacy Transactions (P2PKH, P2SH)
    * Segwit V0 (P2WPKH, P2WSH)
    * Taproot (P2TR - Key path and Script path spends)
    * Transaction Timelocks
        * OP_CLTV and OP_CSV
        * nLocktime and nSequence
* Taproot and Tapscripts
* Other Transaction Forms:
    * MAST
    * Coinjoin
    * Payjoin
    * PSBT
    * Coinbase Transaction
    
## Schedule: Topics, Goals and Resources

| Day | Topic | Goals |Resources                                                                                                                                              |
|-----------|-------------------------|------------------------------------|----------------------------------------------------------------------------|
|Monday | Structure of a Transaction  | Understand: Structure of a Transaction <br/> Version <br/> Inputs <br/> Outputs <br/> Locktime  | [Chapter 6: Transactions](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch06.asciidoc) <br/> [Introduction to Transactions](https://developer.bitcoin.org/devguide/transactions.html#introduction)<br/> [Transaction: Programming Bitcoin](https://github.com/jimmysong/programmingbitcoin/blob/master/ch05.asciidoc#transactions) <br/> [Deconstructing a bitcoin transaction](https://dev.to/thunderbiscuit/deconstructing-a-bitcoin-transaction-4l2n)  |
|Tuesday | Transaction Script Basics | Understand: Bitcoin Transaction Scripts <br/> Opcodes <br/>Parsing Scripts <br/> Standard scripts: P2PK, P2PKH, P2SH, P2WPKH, P2WSH |[Bitcoin Scripts Basics](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/appendix/bitcoin-script.ipynb) <br/> [Scripts](https://github.com/jimmysong/programmingbitcoin/blob/master/ch06.asciidoc#script) <br/> [Chapter 7: Advanced Transactions and Scripting](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch07.asciidoc) <br/> [Scripts](https://learnmeabitcoin.com/technical/script) <br/> [Opcodes](https://btcinformation.org/en/developer-reference#transactions)  |
|Wednesday | Creating Bitcoin Transaction | Learn how to create these Transactions: <br/> P2PKH <br/> P2SH <br/> P2WPKH <br/> P2WSH <br/> Timelocks  | [Creating a P2PKH transaction](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter1-legacy/p2pkh.ipynb) <br/> [Creating a P2SH multisig transaction](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter1-legacy/p2sh-multisig.ipynb) <br/> [Creating a P2WPKH transaction](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter2-segwitv0/p2wpkh.ipynb) <br/> [Creating a P2WSH multisig transaction](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter2-segwitv0/p2wsh-2-of-2-multisig.ipynb) <br/> [P2TR Key Path and Script Path](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter3-taproot/p2tr-key-and-script-path.ipynb) <br/> [OP_CLTV and OP_CSV](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter5-timelocks/script-level-timelocks.ipynb) <br/> [nLocktime and nSequence](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter5-timelocks/transaction-level-timelocks.ipynb) <br/> [Transaction Creation and Validation](https://github.com/jimmysong/programmingbitcoin/blob/master/ch07.asciidoc) <br/> [Pay-to-Script Hash](https://github.com/jimmysong/programmingbitcoin/blob/master/ch08.asciidoc) <br/> [Segwit](https://github.com/jimmysong/programmingbitcoin/blob/master/ch13.asciidoc) |
|Thursday | Taproot  | Understand: Taproot <br/> Schnorr Signatures and TapTweaks <br/> Taproot TapTree | [P2TR Key Path and Script Path](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter3-taproot/p2tr-key-and-script-path.ipynb) <br/> [Taproot Multisig](https://youtu.be/Uo3uzofPlX0) <br/> [Taproot workshop by Bitcoin Optech Group ]( https://bitcoinops.org/en/schorr-taproot-workshop/ )   |
|Friday | Other Transaction Forms | Learn about: <br/> MAST <br/> Coinjoin <br/> Payjoin <br/> PSBT <br/> Coinbase Transaction | [Merklized Alternative Script Tree](https://bitcoinops.org/en/topics/mast) <br/> [BIP 114: MAST](https://github.com/bitcoin/bips/blob/master/bip-0114.mediawiki) <br/> [Coinjoin](https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2014-January/004191.html) <br/> [BIP 78: Payjoin](https://github.com/bitcoin/bips/blob/master/bip-0078.mediawiki) <br/> [BIP 174: PSBT](https://github.com/bitcoin/bips/blob/master/bip-0174.mediawiki) <br/> [Coinbase Transaction](https://learnmeabitcoin.com/technical/coinbase-transaction)  |



## Exercises
1. Given this raw transaction [hex](https://mempool.space/api/tx/6d9da35544e87a88279c5bfc66e08a873f3d456b4d6112620e2c41555863f920/hex), identify the version, inputs, outputs and the locktime.
2. Perform the stack evaluation of this Bitcoin script and indicate whether it will result in true or false:  hex: '010101029301038801027693010487'
3. Given the string 'Btrust Builders', whose bytes encoding is '427472757374204275696c64657273', which is our preimage, generate the redeem script in hex format for the given preimage. Note: redeem_script => OP_SHA256 <lock_hex> OP_EQUAL

4. Derive an address with from the above (2) redeemscript and construct a transaction that send Bitcoins to the address

5. Construct another transaction that spends from the above (3) transaction given that you have both locking and unlock scripts.
