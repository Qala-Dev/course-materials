---
description: Transactions, Authorisation and Authentication
---

# Week 2

This week, we'll be studying Bitcoin Transactions. We will also cover Authorisation and Authentication.
In Bitcoin Transactions, we will cover the structure of a Bitcoin Transaction and explore locking and unlocking scripts in a Bitcoin Transaction.

## Prerequisites

* You are expected to have completed Keys and Addresses as well as Digital Signatures. Additionally, we hoped that you've learned Schnorr Signatures and TapTweaks. 

## Goals

At the end of the week, we hope that you will:

* Learn the Components of a Bitcoin Transaction
* Understand how to parse a Bitcoin Transaction
* Understand Standard Transaction Locking and Unlocking Scripts for Legacy Transactions (P2PKSH, P2SH)
* Understand Standard Transaction
    * Legacy Transactions (P2PK, P2PKH, P2SH)
    * Segwit V0 (P2WPKH, P2WSH)
    * Taproot (P2TR - Key path and Script path spends)
* Transaction Timelocks (nLocktime and nSequence)

## Topics and Resources

| Topic      | Resources                                                                                                                                                                                                                                        |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Structure of a Transaction    | [Chapter 6: Transactions](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch06.asciidoc) <br/> [Transactions](https://github.com/chaincodelabs/bitcoin-tx-tutorial ) (Chapters 1, 2 & 3)  |
| Scripts and Script Construction | [Bitcoin Scripts Basics](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/appendix/bitcoin-script.ipynb) <br/> [Chapter 7: Advanced Transactions and Scripting](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch07.asciidoc) <br/> [Opcodes](https://btcinformation.org/en/developer-reference#transactions) <br/> [Script Construction](https://learn.saylor.org/mod/book/view.php?id=36364&chapterid=18948)  |
| Taproot  | [P2TR Key Path and Script Path](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter3-taproot/p2tr-key-and-script-path.ipynb) <br/> [Taproot workshop by Bitcoin Optech Group ]( https://bitcoinops.org/en/schorr-taproot-workshop/ )   |
| Timelocks    | [Transaction Level Timelocks](https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter5-timelocks/transaction-level-timelocks.ipynb)                                                                                  |


## Exercises
