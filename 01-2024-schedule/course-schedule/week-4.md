---
description: Second-Layer Applications
---

# Week 4

This week, we'll mainly learn about Second-Layer Applications, specifically the Lightning Network. We'll explore how the network functions, its structure, and payment channels.&#x20;

Additionally, we'll delve into topics like path finding and how payments are delivered in the Lightning Network. Plus, we'll try to grasp the philosophy behind Bitcoin.

## Prerequisites

* LND should be installed and ready
* Developer environment from week 1 should be available. Having [Polar](https://lightningpolar.com) installed and functional is essential! It requires [Docker](https://www.docker.com/products/docker-desktop/) to be installed.

## Goals

* Understand how the lightning network operates
  * Why it is thought of as a bitcoin "layer 2"
  * Where the trust in the system lies
  * What security assumptions it makes
  * How the various "layers" of the network fit together
* Understand the architecture of Lightning Network
* Lightning Nodes and Wallets
* Be familiar with sending and receiving lightning payments
* Understand Payment Channels
  * Constructing a Payment Channel
  * Sending Payment accross the Channel
  * The Commitment Transaction
  * Advancing the Channel State
  * Closing the Channel
* Understand Routing on a network of Payment Channels
  * Routing a Payment
  * Routing vs pathfinding
  * Creating a network of Payment Channels
  * Fairness Protocol
  * Hash Time-Locked Contracts (HTLCs)
* Understand Channel Operation and Payment Forwarding
  * Managing HTLCs
  * Committing HTLCs to channel state
  * Channel balance
* Understand Path Finding and Payment Delivery
  * Finding Candidate Paths
  * Payment Delivery
  * Multiparts Payment (MPP)
* Understand Lightning Payments Requests
  * Payment Invoices
  * Payment Requests vs Bitcoin Addresses
  * Payment Requests Serialization and Interpretation

## Schedule


| Topic        | Goals               | Resources                                                         |
| ------------ | --------------------|------------------------------------------------------------------ |
| Lightning Network Basics     | Understand: <br/> Why Lightning is called Layer 2 <br/> Trust in Decentralised Network <br/> Security Assumptions <br/> The Lightning Network components |[Chapter 1: Introduction](https://lnbook.256k1.dev/#intro_what_is_the_lightning_network) <br/> [How Network Layers Fit Together](https://youtu.be/krux2v0jt4E?list=PLpLH33TRghT17_U3as2P3vHfAGL8pSOOY) |
| Lightning Network Architecture    | Understand the various components of the Lightning Network |[Chapter 6: Lightning Network Architecture](https://lnbook.256k1.dev/#_06_lightning_network_architecture)                                                                  |
| Lightning Nodes and Wallets   | Understand:  Lightning Nodes <br/> Wallets |[Lightning Nodes](https://lnbook.256k1.dev/#_lightning_nodes) <br/> [Lightning Wallets](https://lnbook.256k1.dev/#_lightning_wallets)                                     |
| Payment Channels | Understand: Payment Channel <br/>  Sending Payment accross the Channel <br/> The Commitment Transaction <br/> Advancing the Channel State <br/> Closing the Channel | [Chapter 7: Payment Channels](https://lnbook.256k1.dev/#payment_channels)      |
| Routing on a Network of Payment Channels  | Understand: Routing a Payment <br/> Routing vs pathfinding <br/> Creating a network of Payment Channels <br/>  Fairness Protocol <br/>  Hash Time-Locked Contracts (HTLCs) |[Chapter 8: Routing on a Network of Payment Channels)](https://lnbook.256k1.dev/#routing)  |
|Channel Operation and Payment Forwarding| Understand:  Managing HTLCs <br/> Committing HTLCs to channel state <br/>  Channel balance| [Channel Operation and Payment Forwarding](https://lnbook.256k1.dev/#channel_operation) |
| Pathfinding and Payment Delivery    | Understand: Pathfinding <br/> Payment Delivery |[Chapter 12: Pathfinding and Payment Delivery](https://lnbook.256k1.dev/#path_finding)         |
| Lightning Payments Requests  | Understand: Payment Invoices <br/>  Payment Requests Versus Bitcoin Addresses | [Lightning Payment Requests](https://lnbook.256k1.dev/#invoices) <br/> [Payment Invoices](https://lnbook.256k1.dev/#_invoices)                                     |


## Exercises

* Open a lightning channel on signet
* Request an invoice and make a payment
* BONUS: Repeat previous exercise programmatically (RPC)
* Have a go at [making a lightning app](https://medium.com/@wbobeirne/making-a-lightning-web-app-part-1-4a13c82f3f78) using LND on signet
* Follow along with Brian Mancini's "Building a Lightning Graph" workshop which can be found [here](https://github.com/bmancini55/building-lightning-graph). There is documentation for the workshop [here](https://github.com/bmancini55/building-lightning).
