---
description: Deep Dive into Bitcoin Blockchain, Network, and Transaction Fees
---

# Week 3

We will be studying the Bitcoin Blockchain and it's P2P Network. We'll also explore Transaction Fees and how they are calculated.

## Prerequisites

Bitcoind installed with access to signet and regtest chains.

## Schedule

<table data-header-hidden><thead><tr><th width="232.33333333333331"></th><th width="278"></th><th></th></tr></thead><tbody><tr><td><strong>Goal(s)</strong></td><td><strong>Resource(s)</strong></td><td><strong>Exercise(s)</strong></td></tr><tr><td><p>Understand:</p><ul><li>Blockchain</li><li>Block Creation</li><li>Block headers contents</li><li>Blocks template</li></ul></td><td><ul><li><a href="https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch09.asciidoc">The Blockchain Mastering Bitcoin Chapter 9</a></li><li><a href="https://youtu.be/fw3WkySh_Ho?feature=shared">Consensus Algorithms, Blockchain Technology (Video)</a></li></ul></td><td>Complete the Block constructor code challenge</td></tr><tr><td><p>Understand:</p><ul><li>Compact Blocks</li><li>Compact Blocks Relay</li></ul></td><td><ul><li><a href="https://bitcoincore.org/en/2016/06/07/compact-blocks-faq/">Compact Blocks FAQ</a></li><li><a href="https://bitcoinops.org/en/topics/compact-block-filters/">Compact Block Filters</a></li><li><a href="https://bitcoinops.org/en/topics/compact-block-relay/">Compact Block Relay</a></li><li><a href="https://github.com/bitcoin/bips/blob/master/bip-0022.mediawiki">GetBlocktemplate BIP</a></li></ul></td><td>None</td></tr><tr><td><p>Understand:</p><ul><li>The mining process.</li><li>Mining pools.</li><li><em><strong>Bonus</strong></em>: Stratum v2.</li><li>mining attack vectors.</li><li>block re-orgs</li></ul></td><td><ul><li><a href="https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch10.asciidoc">Mining and Consensus Chapter 10 Mastering Bitcoin</a></li><li><a href="https://btctranscripts.com/magicalcryptoconference/2019/the-state-of-bitcoin-mining/">Mining the Good, the Bad, and the Ugly</a></li><li><a href="https://docsend.com/view/szk48syby33q28zq">Stratum v2</a></li><li><a href="https://btctranscripts.com/magicalcryptoconference/2019/the-state-of-bitcoin-mining/">Ancestor Fee Rate Based Mining</a></li><li><a href="https://www.youtube.com/watch?v=MJ0OzrkHvXA">What is Bitcoin mining? <em>video explanation</em></a></li><li><a href="https://en.wikipedia.org/wiki/Mining_pool">Mining Pools</a></li><li><a href="https://learnmeabitcoin.com/technical/chain-reorganisation">Chain Reorgs</a></li></ul></td><td>Mine a block, and reorg the chain with a double spend on regtest</td></tr><tr><td><p>Understand:</p><ul><li>How the Bitcoin network works.</li><li>the P2P network.</li><li>Network Messages</li><li>What P2P Attack vectors are</li><li>How node peer discovery works.</li><li>How blocks are propagated in the network</li></ul></td><td><ul><li><a href="https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch08.asciidoc">The Bitcoin Network Mastering Bitcoin Chapter 8</a></li><li><a href="https://www.youtube.com/watch?v=eVerdR2hOMw">P2p Network, John New Berry</a></li><li><a href="https://www.youtube.com/watch?t=351&#x26;v=H-wH6mY9pZo&#x26;feature=youtu.be">P2P Design</a></li><li><a href="https://residency.chaincode.com/presentations/bitcoin/P2P_Design_Bitcoin_Core.pdf">P2P Design Presentation</a></li><li><a href="https://www.usenix.org/conference/usenixsecurity15/technical-sessions/presentation/heilman">P2P Attack vectors</a></li></ul></td><td><p><a href="https://github.com/willcl-ark/tinybitcoinpeer">Run Tiny Bitcoin peer locally</a></p><p></p><p>Explain the bootstrapping process of a node</p></td></tr><tr><td><p>Understand:</p><ul><li>How fees are estimated for transactions</li><li>The difference between absolute and variable fee rate</li><li>The difference betwen RBF and CPFP for fee bumping transactions</li><li>Pinning attacks</li></ul></td><td><ul><li><a href="https://learnmeabitcoin.com/technical/transaction-fee">Transactions fees Structure</a></li><li><a href="https://bramcohen.medium.com/how-wallets-can-handle-transaction-fees-ff5d020d14fb">How Wallets Can Handle Transaction Fees</a></li><li><a href="https://btctranscripts.com/scalingbitcoin/montreal-2015/transaction-fee-estimation/">Fee Estimation by Wallets</a></li><li><a href="https://bitcoinops.org/en/topics/out-of-band-fees/">Out of Band</a></li><li><a href="https://johnnewbery.com/an-intro-to-bitcoin-core-fee-estimation/">An Intro to Bitcoin Core Fee Estimation</a></li><li><a href="https://hackmd.io/_vQeKNLeSPeh0g-uhbA5_A">Challenges of Fee Estimation</a></li><li><a href="https://bitcoinops.org/en/topics/coin-selection/">Coinselection</a></li><li><a href="https://bitcoinops.org/en/topics/transaction-pinning/">Transaction Pinning</a></li><li><a href="https://bitcoinops.org/en/topics/replace-by-fee/">Replace By Fee (RBF)</a></li><li><a href="https://github.com/bitcoin/bips/blob/master/bip-0125.mediawiki">Replace By Fee Fee BIP</a></li></ul></td><td>Create transactions on regtest with 2s/vb, 10s/vb, 15s/vb, and 10,000 sats absolute fee</td></tr></tbody></table>

If you finish the day's reading ahead of schedule, feel free to move on to the next day's material, as repetition is key when it comes to absorbing so much knowledge.

## Deliverables

{% hint style="success" %}
* Complete the Block constructor code challenge
* Conduct the mining exercise: 51% attacks, mine a block, and reorg the chain with a double spend on regtest
* Run the Tiny Bitcoin peer and provide an explanation of the boot process
* Create transactions on regtest as per the specified exercise
{% endhint %}

**Bonus Exercises**

* Wednesday - Use your block construction algorithm on the live mempool to create a block template. Compare it with getblocktemplate RPC. Simulate using regtest
* Friday - Create a 2-generation chain of transactions with an ancestor score of 20s/vb
