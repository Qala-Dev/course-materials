---
description: Deep Dive into Bitcoin Blockchain, Network, and Transaction Fees
---

# Week 3

This week, we will be studying the Bitcoin Blockchain and it's P2P Network. We will also be looking at Transaction Fees and how they are calculated.

## Prerequisites

- Bitcoind installed with access to signet and regtest chains.

## Schedules

| **Goal(s)**     | **Resource(s)**          | **Exercise(s)**                                          |
|------------|--------------------------------------|----------------------------------------------------|
| Understand: <ul><li> Blockchain.</li><li>Block Creation.</li> <li>Block headers contents.</li> <li> Blocks template.</li></ul> | <ul><li>[The Blockchain Mastering Bitcoin Chapter 9](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch09.asciidoc).</li> <li>[Consensus Algorithms, Blockchain Technology (Video)](https://youtu.be/fw3WkySh_Ho?feature=shared).</li> </ul> | <ul><li>Complete the Block constructor code challenge</li> </ul> |
|Understand: <ul><li> Compact Blocks</li> <li> Compact Blocks Relay</li>  </ul>  | <ul><li>[Compact Blocks FAQ](https://bitcoincore.org/en/2016/06/07/compact-blocks-faq/).</li> <li> [Compact Block Filters](https://bitcoinops.org/en/topics/compact-block-filters/). </li> <li> [Compact Block Relay](https://bitcoinops.org/en/topics/compact-block-relay/). </li> <li> [GetBlocktemplate BIP](https://github.com/bitcoin/bips/blob/master/bip-0022.mediawiki).</li></ul> |  <ul><li>None</li></ul> |
| Understand:<ul><li> The mining process.</li> <li> Mining pools. </li> <li> ***Bonus***: Stratum v2.</li> <li> mining attack vectors. </li> <li> block re-orgs </li> </ul> | <ul> <li> [Mining and Consensus Chapter 10 Mastering Bitcoin](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch10.asciidoc)</li> <li> [Mining the Good, the Bad, and the Ugly](https://btctranscripts.com/magicalcryptoconference/2019/the-state-of-bitcoin-mining/). </li> <li> [Stratum v2](https://docsend.com/view/szk48syby33q28zq#).</li> <li> [Ancestor Fee Rate Based Mining](https://btctranscripts.com/magicalcryptoconference/2019/the-state-of-bitcoin-mining/). </li> <li> [What is Bitcoin mining? *video explanation*](https://www.youtube.com/watch?v=MJ0OzrkHvXA)</li> <li> [Mining Pools](https://en.wikipedia.org/wiki/Mining_pool) </li> <li> [Chain Reorgs](https://learnmeabitcoin.com/technical/chain-reorganisation) </li></ul> | <ul><li> Mine a block, and reorg the chain with a double spend on regtest. </li></ul> |
| Understand:<ul><li> How the Bitcoin network works. </li> <li> the P2P network. </li> <li> Network Messages </li> <li> What P2P Attack vectors are </li> <li> How node peer discovery works. <li> How blocks are propagated in the network </li> </ul> | <ul><li> [The Bitcoin Network Mastering Bitcoin Chapter 8](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch08.asciidoc)</li> <li> [P2p Network, John New Berry](https://www.youtube.com/watch?v=eVerdR2hOMw). </li> <li> [P2P Design](https://www.youtube.com/watch?t=351&v=H-wH6mY9pZo&feature=youtu.be).</li> <li>[P2P Design Presentation](https://residency.chaincode.com/presentations/bitcoin/P2P_Design_Bitcoin_Core.pdf) </li> <li> [P2P Attack vectors](https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/heilman)</li></ul> | <ul> <li> [Run Tiny Bitcoin peer locally](https://github.com/willcl-ark/tinybitcoinpeer)</li> <li> Explain the bootstrapping process of a node. </li> </ul> |
| Understand: <ul> <li>How fees are estimated for transactions. </li> <li>The difference between absolute and variable fee rate. </li> <li>The difference betwwen RBF and CPFP for fee bumping transactions. </li> <li> Pinning attacks. </li> </ul> | <ul><li>[Transactions fees Structure](https://learnmeabitcoin.com/technical/transaction-fee)</li> <li> [How Wallets Can Handle Transaction Fees](https://bramcohen.medium.com/how-wallets-can-handle-transaction-fees-ff5d020d14fb). </li>  <li> [Fee Estimation by Wallets](https://btctranscripts.com/scalingbitcoin/montreal-2015/transaction-fee-estimation/). </li> <li> [Out of Band](https://bitcoinops.org/en/topics/out-of-band-fees/). </li> <li> [An Intro to Bitcoin Core Fee Estimation](https://johnnewbery.com/an-intro-to-bitcoin-core-fee-estimation/).</li>  <li> [Challenges of Fee Estimation](https://hackmd.io/_vQeKNLeSPeh0g-uhbA5_A). </li> <li> [Coinselection](https://bitcoinops.org/en/topics/coin-selection/).  </li> <li> [Transaction Pinning](https://bitcoinops.org/en/topics/transaction-pinning/). </li> <li> [Replace By Fee (RBF)](https://bitcoinops.org/en/topics/replace-by-fee/). </li> <li> [Replace By Fee Fee BIP](https://github.com/bitcoin/bips/blob/master/bip-0125.mediawiki) </li></ul>  |  <ul> <li> Create transactions on regtest with 2s/vb, 10s/vb, 15s/vb, and 10,000 sats absolute fee. </li> </ul> |

*Note: If you complete the day's readings ahead of schedule, consider progressing to the next day's material, as repetition enhances knowledge absorption.*

## Deliverables

- Complete the Block constructor code challenge.
- Conduct the mining exercise: 51% attacks, mine a block, and reorg the chain with a double spend on regtest.
- Run the Tiny Bitcoin peer and provide an explanation of the boot process.
- Create transactions on regtest as per the specified exercise.


**Bonus Exercise**
* <b>Wednesday</b> - Use your block construction algorithm on the live mempool to create a block template. Compare it with getblocktemplate RPC. Simulate using regtest.
    
* <b>Friday </b> - Create a 2-generation chain of transactions with an ancestor score of 20s/vb. 
