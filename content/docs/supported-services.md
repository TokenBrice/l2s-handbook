---
title: "Supported Services"
weight: 4
description: >
  An overview of all the services supported on ParaSwap and their main features.
---

As a middleware, ParaSwap connects and harnesses many services to facilitate its users' interactions with DeFi. The main driver of the prices provided are obviously the exchanges supported - so this is where we start at with the [`💱 Exchanges`](#-exchanges) section.

ParaSwap also implements various services and tools to streamline the experience, such as a price oracle. You'll find them detailed in the [`🧰 Infrastructure`](#-infrastructure) section.

## 💱 Exchanges

All major decentralised exchanges are supported on ParaSwap. When a new exchange is made available - its trading volume is analysed to determine the integration's priority.

### Uniswap

![uniswap-logo](/images/DEX/uniswap.png) 

Uniswap is the leading decentralised exchange. Uniswap pioneered the concept of an Automated Market Maker. Thanks to its AMM, Uniswap always find a price for a given trade - at the cost of potentially high slippage if the pool is undersized.

Uniswap's design is minimal and elegant. Since Uniswap's is also the decentralized exchange with the most volume processed to date, (parts of) Uniswap's model are frequently re-used to create new AMMs.

- **[Official Website](https://uniswap.exchange/)**
- **[Stats & Infos](https://uniswap.info/)**

---

### Curve Finance

Curve improved on Uniswap's Automated Market Maker model to optimise it for the exchanges of assets following the same peg, such as stablecoins (USDC, USDT, DAI, TUSD) or the different representations of Bitcoin on the Ethereum chain (wBTC, renBTC, sBTC).

- **[Official Website](https://www.curve.fi/)**
- **[Stats & Infos](https://www.curve.fi/combinedstats)**

---

### Balancer

![balancer-logo](/images/DEX/balancer.png)

Balancer built on the Uniswap's AMM model and improve it to reduce the risk of impermanent losses making it more attractive for liquidity providers. Unlike Uniswap which defaults to equally weighted pairs (ex: 50% ETH / 50% DAI), Balancer can support up to 8 tokens in a pool with custom weights.

- **[Official Website](https://balancer.exchange/)**

---

### 0x Network

0x is technically not a decentralized exchange per-se, but more like a network of order books (0xMesh). 0x provides an easy infrastructure for decentralized exchanges to mutualize their order book on the Mesh, helping to solve the chicken & egg liquidity dilemma. 

- **[Official Website](https://0x.org/)**
- **[Stats & Infos](https://0xtracker.com/)**

---

### Kyber Network

![kyber-logo](/images/DEX/kyber.png)

Unlike most DEX, Kyber does not implement an AMM and use instead of an order book logic. While it provides more control to the liquidity providers, it's also more restrictive than an AMM-based model. 

- **[Official Website](https://kyber.network/)**
- **[Stats & Infos](https://tracker.kyber.network/#/)**

---

### Bancor

![bancor-logo](/images/DEX/bancor.png)

Bancor was a pioneer when it comes to decentralized exchanges, yet adoption was mostly driven by Uniswap. With the upcoming Bancor V2 release, the team promises the elimination of impermanent losses for liquidity providers as well as a liquidity amplification mechanism to reduce slippage. 

- **[Official Website](https://www.bancor.network/)**
- **[Stats & Infos](https://bancor-network.info/)**

---

### Oasis

![maker-oasis-logo](/images/DEX/maker.jpg)

Oasis is a decentralized exchange provided by Maker. While it offers fewer pairs than other DEXes, it can provide another potential source of pricing for arbitrages mostly on ETH/DAI pairs.

- **[Official Website](https://oasis.app/)**
- **[Stats & Infos](https://bloxy.info/dexes/0x14fbca95be7e99c15cc2996c6c9d841e54b79425)**

---

## 🧰 Infrastructure

On top of the decentralized exchanges ParaSwap integrates with, several other tools are required to provide or improve the service. You'll find the main ones below:

### ChainLink

ParaSwap implements ChainLink's price feeds to quickly fetch actionable and accurate prices on most pairs.

### Nexus Mutual

ParaSwap's main contracts are covered on Nexus Mutual - the insurance service. Any user can contract an insurance to hedge oneself against a risk of failure of ParaSwap's contract.