---
layout: page
title: Crypto Tracking
description: Bitcoin, Ethereum and Cardano against the spot crypto ETFs — premiums, fee drag and return statistics, updated daily
img: assets/img/crypto-tracking.svg
importance: 8
category: fun
github: https://github.com/dmhenke/Crypto_Tracking_Fun
redirect: https://dmhenke.github.io/Crypto_Tracking_Fun/
---

Crypto Tracking is a daily-updated, interactive dashboard comparing Bitcoin, Ethereum and Cardano on Coinbase with the Grayscale (GBTC, ETHE) and iShares (IBIT, ETHA) spot funds. An R pipeline in GitHub Actions pulls the data each night; every statistic is recomputed in the browser and validated against R.

## Features

- Each Grayscale fund's estimated premium or discount to its holdings, checked against issuer figures
- Fee drag of GBTC vs IBIT and ETHE vs ETHA, measured with Newey-West intervals
- Return relationships with normal-theory, Newey-West or block-bootstrap intervals, and lead-lag at matched closing times
- Price-range forecasts scored by a rolling-origin backtest, and a Cardano epoch tracker
