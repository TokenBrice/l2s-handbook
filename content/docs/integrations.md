---
title: "Integrations"
weight: 6
description: >
  An overview of all the services ParaSwap connects too, the one used for the infrastructure, and third party services harnessing ParaSwap's API.
---

As a middleware, ParaSwap connects to many services to facilitate its users' interactions with DeFi. The main driver of the prices provided are the exchanges supported - displayed in the [`💱 Exchanges`](#-exchanges) section.

Third-party services such as wallet can also integrate with ParaSwap thanks to the API - [`💻 ParaSwap API`](#-paraswap-api)

Finally, ParaSwap also implements several services and tools to streamline the experience, such as a price oracle. You'll find them detailed in the [`🧰 Infrastructure`](#-infrastructure) section.

## 💱 Supported Exchanges

All major decentralized exchanges are supported on ParaSwap. When a new exchange is made available - its trading volume is analysed to determine the integration's priority.

### Uniswap

<div align="center">{{< figure src="/images/DEX/uniswap.png" >}}</div>

Uniswap is the leading decentralized exchange. Uniswap pioneered the concept of an Automated Market Maker. Thanks to its AMM, Uniswap always find a price for a given trade - at the cost of potentially high slippage if the pool is undersized.

Uniswap's design is minimal and elegant. Since Uniswap's is also the decentralized exchange with the most volume processed to date, (parts of) Uniswap's model are frequently re-used (forked) to create new AMMs.

_ParaSwap fetches both Uniswap V2 (current) and V1 prices (previous version, still used)._

- **[Official Website](https://uniswap.exchange/)**
- **[Stats & Infos](https://uniswap.info/)**

---

### SushiSwap

<div align="center">{{< figure src="/images/DEX/sushiswap.png" >}}</div>

SushiSwap is a Uniswap fork with updated tokonomics attempting to better align liquidity provider incentives with the protocol's best interest. Compared to Uniswap, the commission earned by liquidity providers is slightly lowered (0.30% -> 0.25%) in favor of a value accrual mechanism on the SUSHI token.

- **[Official Website](https://sushiswap.fi/)**
- **[SushiSwap Protocol Analytics](https://sushiswap.vision/home)**

---

### Curve Finance

<div align="center">{{< figure src="/images/DEX/curve.png" >}}</div>


Curve improved on Uniswap's Automated Market Maker model to optimise it for the exchanges of assets following the same peg, such as stablecoins (USDC, USDT, DAI, TUSD) or the different representations of Bitcoin on the Ethereum chain (wBTC, renBTC, sBTC).

Curve is very efficient to swap such assets with minimal slippage.

- **[Official Website](https://www.curve.fi/)**
- **[Stats & Infos](https://www.curve.fi/combinedstats)**

---

### Balancer

<div align="center">{{< figure src="/images/DEX/balancer.png" >}}</div>

Balancer built on the Uniswap's AMM model and improve it to reduce the risk of impermanent losses making it more attractive for liquidity providers. Unlike Uniswap which defaults to equally weighted pairs (ex: 50% ETH / 50% DAI), Balancer can support up to 8 tokens in a pool with custom weights.

- **[Official Website](https://balancer.exchange/)**

---

### 0x Network & 0x API

<div align="center">{{< figure src="/images/DEX/0x.png" >}}</div>

0x is technically not a decentralized exchange, but more like a network of order books (0xMesh). 0x provides an easy infrastructure for decentralized exchanges to mutualize their order book on the Mesh, helping to solve the chicken & egg liquidity dilemma. 

- **[Official Website](https://0x.org/)**
- **[Stats & Infos](https://0xtracker.com/)**

---

### Synthetix

<div align="center">{{< figure src="/images/integrations/synthetix.png" >}}</div>

Synthetix is one of the leading decentralised protocol for derivatives on Ethereum. All synths are supported on ParaSwap as well as Synthetix itself. It enables swapping from any token to sUSD (or sETH/sBTC). You can also swap any synth for another without slippage.

Paraswap is part of the [Synthetix Volume Program](https://blog.synthetix.io/paraswap-joins-the-synthetix-volume-program/)

- **[Official Website](https://synthetix.io/)**
- **[Stats & Infos](https://stats.synthetix.io/)**

---

### Kyber Network

<div align="center">{{< figure src="/images/DEX/kyber.png" >}}</div>

Unlike most DEX, Kyber does not implement an AMM and use instead of an order book logic. While it provides more control to the liquidity providers, it's also more restrictive than an AMM-based model. 

- **[Official Website](https://kyber.network/)**
- **[Stats & Infos](https://tracker.kyber.network/#/)**

---

### Bancor

<div align="center">{{< figure src="/images/DEX/bancor.png" >}}</div>

Bancor was a pioneer when it comes to decentralized exchanges, yet adoption was mostly driven by Uniswap. With the upcoming Bancor V2 release, the team promises the elimination of impermanent losses for liquidity providers as well as a liquidity amplification mechanism to reduce slippage. 

- **[Official Website](https://www.bancor.network/)**
- **[Stats & Infos](https://bancor-network.info/)**

---

### Oasis

<div align="center">{{< figure src="/images/DEX/maker.jpg" >}}</div>

Oasis is a decentralized exchange provided by Maker. While it offers fewer pairs than other DEXes, it can provide another potential source of pricing for arbitrages mostly on ETH/DAI pairs.

- **[Official Website](https://oasis.app/)**
- **[Stats & Infos](https://bloxy.info/dexes/0x14fbca95be7e99c15cc2996c6c9d841e54b79425)**

---

## 💻 ParaSwap API

DeFi services can integrate ParaSwap thanks to the API. Projects integrating our API can easily collect a commission on the trades they facilitate thanks to the [`Revenue Sharing Contract`]({{< relref path="/content/docs/fees.md#-revenue-sharing-integrators" >}}).

### MetaMask

<div align="center">{{< figure src="/images/integrations/metamask.jpg" >}}</div>

MetaMask is the leading Ethereum wallet, trused by over 1 million users worldwide. It's a browser-extension enabling easy access to web3 decentralized applications, such as ParaSwap. MetaMask users can now swap using ParaSwap directly from their wallet!

- **[Official Website](https://metamask.io)**
- **[Integration Announcement](https://www.coindesk.com/metamask-gets-into-the-decentralized-exchange-aggregation-business-with-tokenswaps)**

---

### Monolith

<div align="center">{{< figure src="/images/integrations/monolith.png" >}}</div>

Monolith is a non-custodial Ethereum wallet paired with a Visa debit card. ParaSwap is integrated into the mobile app to facilitate users' token swaps.

- **[Official Website](https://monolith.xyz)**
- **[Integration Announcement](https://medium.com/monolith/monolith-dex-the-defi-one-stop-shop-2ba1166197da)**

---

## 🧰 Infrastructure

On top of the decentralized exchanges ParaSwap integrates with, several other tools are required to provide or improve the service. You'll find the main ones below:

### ChainLink

ParaSwap implements ChainLink's price feeds to quickly fetch actionable and accurate prices on most pairs.

### Nexus Mutual

ParaSwap's main contracts are covered on Nexus Mutual - the insurance service. Any user can contract insurance to hedge oneself against the risk of failure of ParaSwap's contract.