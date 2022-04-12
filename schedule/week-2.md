---
description: Building on lightning
---

# Week 2

## Prerequisites

* LND should be installed and ready
* Developer environment from week 1 should be available. Having [Polar](https://lightningpolar.com) installed and functional is essential! It requires [Docker](https://www.docker.com/products/docker-desktop/) to be installed.

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

The mornings will be split between reading 2 chapters of the [Mastering Lightning](https://github.com/lnbook/lnbook) book, and answering discussion questions in small groups.

A web-reader-friendly hosted version of Mastering Lightning can be found at [lnbook.256k1.dev](https://lnbook.256k1.dev), which can be accessed for educational purposes using username and password `qala:lightning`.

Assigned groups and discussion questions are [here](https://docs.google.com/spreadsheets/d/1xE9ZHMB-pd6LSWcBCRj2sfx5lDnvvnfzasarFHy2ugo) and the book should be read in the following order:

| Day       | Chapters |
| --------- | -------- |
| Monday    | 1, 2     |
| Tuesday   | 3        |
| Wednesday | 4, 6     |
| Thursday  | 7        |
| Friday    | 8        |

If you finish your chapter(s) for the day early, feel free to move on to the next day's chapter(s), as repetition is key when it comes to absorbing so much knowledge.

If you finish all the chapters from this week, you can get a head start on the chapters in [week 3](/week-3.md).

### Afternoons

The afternoons will be spent continuing your project-building, with focus shifting towards lightning-based programs and applications.

Choose a project from the [projects](../projects.md) page and get started on it, following the instructions on the project page.

We are looking for you to push your code to GitHub every day, even if it is only a work in progress, not working at all, or just a skeleton of libraries and project layout.
Getting in the habit of regular updates is going to be really useful when we come to show off our proof of work later.

Some of the goals for the week, in addition to the project work include:

* Run LND from source
* Run the LND test suite (if a few tests fail this is OK, they fail on GitHub too -- don't worry!)
* Open a lightning channel on signet
* Request an invoice and make a payment
* BONUS: Repeat previous exercise programmatically (RPC)
* Have a go at [making a lightning app](https://medium.com/@wbobeirne/making-a-lightning-web-app-part-1-4a13c82f3f78) using LND on signet
