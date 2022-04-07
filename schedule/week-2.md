---
description: Building on lightning
---

# Week 2

## Prerequisites

* LND should be installed and ready
* Developer environment from week 1 should be available
* You should read chapters 1 & 2 of Mastering Lightning in your own time before the sessions begin.

## Goals

* Understand how the lightning network operates
    * Why it is thought of as a bitcoin "layer 2"
    * Where the trust in the system lies
    * What security assumptions it makes
    * How the various "layers" of the network fit together
    * Risks and benefits of using Lightning transactions
* Be familiar with sending and receiving lightning payments
* Understand how BOLT11 invoices work and what information they contain
* Understanding about BOLT12 offers, what the costs and benefits are, what alternatives are there?
* Thinking about how the bitcoin fee market can affect lightning channels
* Building an application on top of the lightning network

## Exercises

### Mornings

Monday morning presentation: "Introduction to Lightning".

The mornings will be split between reading 3 chapters of the [Mastering Lightning](https://github.com/lnbook/lnbook) book, and answering discussion questions in small groups.

A web-reader-friendly hosted version of Mastering Lightning can be found at [lnbook.256k1.dev](https://lnbook.256k1.dev/), which can be accessed for educational purposes using username and password `qala:lightning`.

The book should be read in the following order:

| Day | Chapters |
| --- | --- |
| Monday | 1, 2 |
| Tuesday | 3, 4 |
| Wednesday | 6, 7 |
| Thursday | 8, 9 |
| Friday | 12, 15 |

If you finish your chapters for the day early, feel free to move on to the next day's chapters, as repetition is key when it comes to absorbing so much knowledge.

If you finish all the chapters, you should read the remaining chapters in the following order:

11 -> 17 -> 5 -> 10 -> 13 -> 14 -> 16

### Afternoons

The afternoons will be spent continuing your project-building from week 1, with focus shifting towards lightning-based programs and applications.

Some of the goals for the week, in addition to the project work include:

* Run LND from source
* Run the LND test suite
* Open a lightning channel on signet
* Request an invoice and make a payment
* BONUS: Repeat previous exercise programmatically (RPC)
* Have a go at [making a lightning app](https://medium.com/@wbobeirne/making-a-lightning-web-app-part-1-4a13c82f3f78) using LND on signet

Choose a project from the [projects](projects.md) page and get started on it.

