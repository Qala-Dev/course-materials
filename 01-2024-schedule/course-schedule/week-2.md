---
description: Transactions, Authorization and Authentication
---

# Week 2

This week, we'll be studying Bitcoin Transactions. We will cover the structure of a Bitcoin Transaction and explore locking and unlocking scripts in a Bitcoin Transaction.

## Prerequisites

- You are expected to have completed Keys and Addresses as well as Digital Signatures. Additionally, we hoped that you've learned Schnorr Signatures and TapTweaks.

## Goals
<details>

<summary>Understand the structure of a Bitcoin Transaction</summary>

* Version

<!---->

* Inputs

<!---->

* Outputs

<!---->

* Locktime

</details>

<details>

<summary>Learn the fundamental concepts of Scripts</summary>

* Opcodes

<!---->

* Parsing Scripts

<!---->

* Standard Scripts:
  * P2PK
  * P2PKH
  * P2SH
  * P2WPKH
  * P2WSH

<!---->

* Miniscript

<!---->

* Tapscript

</details>

<details>

<summary>Create Bitcoin Transactions</summary>

* Legacy Transactions (P2PKH, P2SH)

<!---->

* Segwit V0 (P2WPKH, P2WSH)

<!---->

* Taproot (P2TR - Key path and Script path spends)

<!---->

* Transaction Timelocks
  * OP\_CLTV and OP\_CSV
  * nLocktime and nSequence

</details>

<details>

<summary>Explore Taproot, Tapscripts and other Transaction Forms</summary>

Other Transaction Forms:

* MAST
* Coinjoin
* Payjoin
* PSBT
* Coinbase Transaction

</details>

## Schedule

<table><thead><tr><th width="181.33333333333331">Topic</th><th width="293">Goals</th><th>Resources</th></tr></thead><tbody><tr><td>Structure of a Transaction</td><td>Understand: Structure of a Transaction<br>Version<br>Inputs<br>Outputs<br>Locktime</td><td><a href="https://drive.google.com/file/d/1gcXBZosFGHmu4UU6afKHYpXJHpeIU3BK/view?usp=sharing">Mastering Bitcoin Chapter 6: Transactions</a><br><a href="https://developer.bitcoin.org/devguide/transactions.html#introduction">Introduction to Transactions</a><br><a href="https://github.com/jimmysong/programmingbitcoin/blob/master/ch05.asciidoc#transactions">Transaction: Programming Bitcoin</a><br><a href="https://dev.to/thunderbiscuit/deconstructing-a-bitcoin-transaction-4l2n">Deconstructing a bitcoin transaction</a><br><a href="https://www.youtube.com/watch?v=Shd9nXe1X-0">Introduction to Transaction</a></td></tr><tr><td>Transaction Script Basics</td><td>Understand: Bitcoin Transaction Scripts<br>Opcodes<br>Parsing Scripts<br>Standard scripts: P2PK, P2PKH, P2SH, P2WPKH, P2WSH<br>Miniscript<br>Tapscript</td><td><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/appendix/bitcoin-script.ipynb">Bitcoin Scripts Basics</a><br><a href="https://github.com/jimmysong/programmingbitcoin/blob/master/ch06.asciidoc#script">Scripts</a><br><a href="https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch07.asciidoc">Chapter 7: Advanced Transactions and Scripting</a><br><a href="https://learnmeabitcoin.com/technical/script">Scripts</a><br><a href="https://btcinformation.org/en/developer-reference#transactions">Opcodes</a><br><a href="https://bitcoin.sipa.be/miniscript/">Sipa: Miniscript</a><br><a href="https://bitcoinops.org/en/topics/miniscript/">Miniscript</a><br><a href="https://bitcoinops.org/en/topics/tapscript/">Tapscript</a></td></tr><tr><td>Creating Bitcoin Transactions</td><td>Learn how to create these transactions:<br>P2PKH<br>P2SH<br>P2WPKH<br>P2WSH<br>Timelocks</td><td><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter1-legacy/p2pkh.ipynb">Creating a P2PKH transaction</a><br><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter1-legacy/p2sh-multisig.ipynb">Creating a P2SH multisig transaction</a><br><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter2-segwitv0/p2wpkh.ipynb">Creating a P2WPKH transaction</a><br><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter2-segwitv0/p2wsh-2-of-2-multisig.ipynb">Creating a P2WSH multisig transaction</a><br><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter3-taproot/p2tr-key-and-script-path.ipynb">P2TR Key Path and Script Path</a><br><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter5-timelocks/script-level-timelocks.ipynb">OP_CLTV and OP_CSV</a><br><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter5-timelocks/transaction-level-timelocks.ipynb">nLocktime and nSequence</a><br><a href="https://github.com/jimmysong/programmingbitcoin/blob/master/ch07.asciidoc">Transaction Creation and Validation</a><br><a href="https://github.com/jimmysong/programmingbitcoin/blob/master/ch08.asciidoc">Pay-to-Script Hash</a><br><a href="https://github.com/jimmysong/programmingbitcoin/blob/master/ch13.asciidoc">Segwit</a></td></tr><tr><td>Taproot</td><td>Understand: Taproot<br>Schnorr Signatures and TapTweaks<br>Taproot TapTree</td><td><a href="https://github.com/chaincodelabs/bitcoin-tx-tutorial/blob/main/chapter3-taproot/p2tr-key-and-script-path.ipynb">P2TR Key Path and Script Path</a><br><a href="https://youtu.be/Uo3uzofPlX0">Taproot Multisig</a><br><a href="https://bitcoinops.org/en/schorr-taproot-workshop/">Taproot workshop by Bitcoin Optech Group</a></td></tr><tr><td>Other Transaction Forms</td><td>Learn about:<br>MAST<br>Coinjoin<br>Payjoin<br>PSBT<br>Coinbase Transaction</td><td><a href="https://bitcoinops.org/en/topics/mast">Merklized Alternative Script Tree</a><br><a href="https://github.com/bitcoin/bips/blob/master/bip-0114.mediawiki">BIP 114: MAST</a><br><a href="https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2014-January/004191.html">Coinjoin</a><br><a href="https://github.com/bitcoin/bips/blob/master/bip-0078.mediawiki">BIP 78: Payjoin</a><br><a href="https://github.com/bitcoin/bips/blob/master/bip-0174.mediawiki">BIP 174: PSBT</a><br><a href="https://learnmeabitcoin.com/technical/coinbase-transaction">Coinbase Transaction</a></td></tr><tr><td>Authorization and Authentication</td><td>Understand: How to authorize and authenticate transactions</td><td><a href="https://drive.google.com/file/d/1cYAUK98pf48SEUD9LT4zttlVWI8CLCxz/view?usp=sharing">Mastering Bitcoin Chapter 7: Authorization and Authentication</a></td></tr></tbody></table>

## Exercises

1. Given the following transaction hexs:

   - [Legacy](https://mempool.space/api/tx/27f1d66f8a1ee5280f4e92508dcb647e954d53004905d08a75574daee4988360/hex)
   - [Segwit with RBF](https://mempool.space/tx/1e300f8666ab9a3970a628196196f5b4707604bf7e7b03d37f902e7817623bfd)
   - [Taproot](https://mempool.space/api/tx/6d9da35544e87a88279c5bfc66e08a873f3d456b4d6112620e2c41555863f920/hex)
   <p>build a transaction parser to identify the transaction type, extracting the version, inputs, outputs and the locktime.</p>

2. Perform the stack evaluation of this Bitcoin script and indicate whether it will result in true or false: hex: '010101029301038801027693010487'. Your solution should output the op_codes and/or values.
3. Given the string 'Btrust Builders', whose bytes encoding is '427472757374204275696c64657273', which is our preimage, generate the redeem script in hex format for the given preimage. Note: redeem_script => OP_SHA256 <lock_hex> OP_EQUAL

   - Derive an address with from the above (2) redeemscript and construct a transaction that send Bitcoins to the address

   - Construct another transaction that spends from the above (3) transaction given that you have both locking and unlock scripts. Ideally, this would mean you write a transaction builder that constructs the transaction and outputs the transaction ID. Broadcast the transaction on you local bitcoin network via the CLI.

4. [BONUS]: Write tests to validate the methods in your transaction parser. Hint: Your parser should have methods to decode the version, inputs, outputs, and locktime of any given transaction.

5. [BONUS]: Write tests to validate the methods in your transaction builder.
