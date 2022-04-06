# Projects

### General

* Projects can be built as a front-end application, back end application, or a command line tool.
* You can choose a bitcoin or lightning project.
* Your first project might leverage a bitcoin or lightning library in order to facilitate fast iteration on end results.
* In your second/third project you should be considering not using a library to do as much of the heavy lifting, so that you can become more comfortable with how bitcoin and lightning are working under the hood.

### Bitcoin projects

Topics to cover: transactions, scripting, reorgs, HD wallets

#### Tier 1

1. Re-skin Kevin's wallet-building workshop
2. Satoshi dice/game
3. Fork monitor
4. Block explorer
5. Mempool/fee analysis
6. P2P network analysis
7. Transaction propagation
8. Build your own signet
9. Bitcoin paywall
10. Bitkinship

#### Tier 2

1. Simulate "push payments" using Bitcoin
2. Improve bitcoin wallet "contact" lists
3. Graph your bitcoin wallet's UTXOs (+ chain analysis)
4. Exchange / remittance service
5. Bitcoin “bank” (hot, warm, cold wallet backend)
6. Chain analysis tool/UI/library
7. Timelock refresher
8. Multi-sig collaborative custody provider

#### To be sorted

* Build a node from LDK
* Joinmarket UI

#### Satoshi dice

**Outline:** A provably fair gambling application, where payments to and from the casino are made on-chain or in Lightning. See [bitcoin.it/wiki/Satoshi\_Dice](https://en.bitcoin.it/wiki/Satoshi\_Dice) for more background information, and [this Stack Exchange question](https://bitcoin.stackexchange.com/questions/7369/how-to-implement-a-game-like-satoshidice) for a high-level on-chain implementation. **Format:** Casino server back-end (required); Client application (optional, GUI or CLI) **BTC/LN topics:** creating and parsing Bitcoin transactions, 0-conf protocols, provable fairness

#### Fork monitor

**Outline:** Monitor blockchain and send an alert when a fork (exceeding n blocks) occurs, and another one when it is "resolved" (m blocks ahead) **Format:** Server back-end; simple front-end or API to subscribe (email, pub/sub, webhooks, ...) **BTC/LN topics:** chain reorgs, block propagation

#### Block explorer

**Outline:** given a block hash, visualize block header and transaction information. Given a transaction hash, visualize input and output information. See e.g. https://blockstream.info/ **Format:** Client application (GUI or CLI) **BTC/LN topics:** parsing blocks, parsing transactions

#### Mempool fee analysis

**Outline:** Create a service which monitors the current state of the mempool with respect to fees. Provide APIs or a GUI which users (and optionally services) can connect to in order to retrieve relevant information. Include facility for users to _upload_ their own transactions via the service. **Format:** Backend with APIs or front end with GUI **BTC/LN topics:** transactions, fees, mempool, p2p

#### Bitkinship

**Outline:** Given two UTXOs, calculate how related they are **Format:** Library and CLI **Bonus:** Given an xpub, calculate relatedness between all UTXOs belonging to xpub.

#### Timelock refresher

**Outline:** To ensure your heirs can access your bitcoin after you pass away, all of your P2WSH addresses contain a second spending clause that after 1 year, a second key (held by your heir) can spend all of your outputs. With this program/script, you want to be able to quickly "refresh" all outputs that are coming close to being unlocked, e.g. within 3 months of the second spending path becoming viable. See https://bitcointalk.org/index.php?topic=5185907.0 for an example of the original setup. **Format:** Client application, short lived. **BTC/LN topics:** creating transaction, advanced scripting, timelocks **Bonus:** multisig instead of single sig; use taproot

### Lightning projects

1. Web store e.g. starblocks.acinq.co
2. Satoshi dice/game
3. Satoshi's place
4. getAlby hacking
5. Messaging app
6. Something related to social networking
7. paywall
8. LND -> Core Lightning (CLN) database migration tool
9. Exchange / remittance service Look around Galoy for more ideas Ask Galoy
10. Build your own lightning node with LDK and accompanying crates (Rust)
