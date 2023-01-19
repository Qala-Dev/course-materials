---
description: Building on lightning
---

# Week 3

## Prerequisites

We assumed that you have the following setups from Week 1 in place:
* LND installed
* [Polar](https://lightningpolar.com) installed and functional (essential)! It requires [Docker](https://www.docker.com/products/docker-desktop/) to be installed.

## Goals

This week, we will be studying Lightning Network and how it works using [Mastering Lightning](https://github.com/lnbook/lnbook) book covering a chapter per day. Discussions will be in small groups as you answer discussion questions. 

A web-reader-friendly hosted version of the book can be found at [lnbook.256k1.dev](https://lnbook.256k1.dev), which can be accessed for educational purposes using username and password `qala:lightning`.

At the end of the week, we hope that you will:

* Understand how the lightning network operates
  * Why it is thought of as a bitcoin "layer 2"
  * Where the trust in the system lies
  * What security assumptions it makes
  * How the various "layers" of the network fit together
  * Risks and benefits of using Lightning transactions
* Be familiar with sending and receiving lightning payments



Assigned groups and discussion questions will be shared in the Cohorts' Channel and the book should be read in the following order:

| Day       | Chapters |
| --------- | -------- |
| Monday    | 1        |
| Tuesday   | 2        |
| Wednesday | 3        |
| Thursday  | 4        |
| Friday    | 6        |

If you finish your chapter for the day early, feel free to move on to the next day's chapter, as repetition is key when it comes to absorbing so much knowledge.


Deliverables for the week are:

* Run LND from source
* Run the LND test suite (if a few tests fail this is OK, they fail on GitHub too -- don't worry!)
* Open a lightning channel on signet
* Request an invoice and make a payment
* BONUS: Repeat previous exercise programmatically (RPC)
* Have a go at [making a lightning app](https://medium.com/@wbobeirne/making-a-lightning-web-app-part-1-4a13c82f3f78) using LND on signet
