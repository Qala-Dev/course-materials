---
description: Transactions, Authorization and Authentication
---

# Week 2

This week, we'll be studying Bitcoin Transactions. We will also cover Authorization and Authentication.
In Bitcoin Transactions, we will cover the structure of a Bitcoin Transaction and explore locking and unlocking scripts in a Bitcoin Transaction.

## Prerequisites

* You are expected to have completed Keys and Addresses as well as Digital Signatures. Additionally, we hoped that you've learned Schnorr Signatures and TapTweaks. 

## Goals

At the end of the week, we hope that you will:

* Learn the Components of a Bitcoin Transaction
    * TXID
    * Transaction Data
    * Transaction Fee
    * Transaction Weight
    * UTXO
* Understand how to authorize a bitcoin transaction
* Understand how a transaction is authenticated
* Understand how to parse a Bitcoin Transaction
* Understand Standard Transaction Locking and Unlocking Scripts for Legacy Transactions (P2PKSH, P2SH)
* Understand Standard Transaction
    * Legacy Transactions (P2PK, P2PKH, P2SH)
    * Segwit V0 (P2WPKH, P2WSH)
    * Taproot (P2TR - Key path and Script path spends)
    * Tapscript
* Transaction Timelocks (nLocktime and nSequence)
* Understand the basics of Bitcoin Script language
* Learn fundamental concepts of Scripts
    * Opcodes
    * Input Scripts
    * Output Scripts
    * Script Execution Stack
* Explore Script Complexities
    * Simple Scripts
    * Scripts With Flow Control(Conditional Clauses)
    * Complex Scripts
* Learn about more types of Scripts
    * Scripted Multisignatures
    * Merklized Alternative Scrip Trees(MAST)
    * Scriptless Multisignatures and Threshold Signatures
    * Tapscript




## Schedule: Topics and Resources

| Day | Topic |Resources                                                                                                                                              |
|-----------|-------------------------|----------------------------------------------------------------------------------------------------------------|
|Monday | Structure of a Transaction <br/> TXID <br/> Transaction Data <br/> Transaction Fee <br/> Transaction Weight <br/> UTXO <br/> Timelocks  | [Chapter 6: Transactions](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch06.asciidoc) <br/> [Transactions](https://github.com/chaincodelabs/bitcoin-tx-tutorial ) (Chapters 1, 2 & 3) <br/> [Introduction to Transactions](https://developer.bitcoin.org/devguide/transactions.html#introduction) <br/> [Deconstructing a bitcoin transaction](https://dev.to/thunderbiscuit/deconstructing-a-bitcoin-transaction-4l2n) <br/> [TXID](https://learnmeabitcoin.com/technical/txid) <br/> [Transaction Data](https://learnmeabitcoin.com/technical/transaction-data) <br/> [Transaction Fee](https://learnmeabitcoin.com/technical/transaction-fee) <br/> [Weight](https://learnmeabitcoin.com/technical/transaction-weight) <br/> [UTXO](https://learnmeabitcoin.com/technical/utxo) <br/>  [Transaction Level Timelocks](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter5-timelocks/transaction-level-timelocks.ipynb)  |
|Tuesday | Scripts and Script Construction | [Bitcoin Scripts Basics](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/appendix/bitcoin-script.ipynb) <br/> [Chapter 7: Advanced Transactions and Scripting](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch07.asciidoc) <br/> [Opcodes](https://btcinformation.org/en/developer-reference#transactions) <br/> [Script Construction](https://learn.saylor.org/mod/book/view.php?id=36364&chapterid=18948) <br/> [Scripts](https://learnmeabitcoin.com/technical/script)  |
|Wednesday | Taproot  | [P2TR Key Path and Script Path](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter3-taproot/p2tr-key-and-script-path.ipynb) <br/> [Taproot workshop by Bitcoin Optech Group ]( https://bitcoinops.org/en/schorr-taproot-workshop/ )   |
|Thursday | Scriptless Multisignatures and Threshold Signature | [Scriptless Multisignatures](https://bitcoinops.org/en/topics/multisignature) <br/> [Threshold Signature](https://bitcoinops.org/en/topics/threshold-signature)  |
|Friday | Other Script Types | [Merklized Alternative Script Tree](https://bitcoinops.org/en/topics/mast) <br/> [Tapscript](https://bitcoinops.org/en/topics/tapscript)



## Exercises
1. Perform the stack evaluation of this Bitcoin script and indicate whether it will result in true or false:  hex: '010101029301038801027693010487'
2. Given the string 'Btrust Builders', whose bytes encoding is '427472757374204275696c64657273', which is our preimage, generate the redeem script in hex format for the given preimage. Note: redeem_script => OP_SHA256 <lock_hex> OP_EQUAL

3. Derive an address with from the above (2) redeemscript and construct a transaction that send Bitcoins to the address

4. Construct another transaction that spends from the above (3) transaction given that you have both locking and unlock scripts.
