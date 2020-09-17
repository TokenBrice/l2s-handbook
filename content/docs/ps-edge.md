---
title: "ParaSwap's Edge"
weight: 3
description: >
  Why using ParaSwap can be more effective than interacting directly with DeFi services  
---

This page summarizes the main benefits you can draw from using ParaSwap's over interacting with the decentralised finance services directly or using another middleware.

### Efficient Decentralized Exchanges Aggregation

{{< notice note >}}
ParaSwap scours dozens of decentralised exchanges to secure the best rates. Thanks to a refined pathing analysis logic, all options are explored, including splitting your order into several exchanges or looking for alternative swapping routes. 
{{< /notice >}}

{{< block "grid-2" >}}
{{< column >}}
#### Find the Best Rate
ParaSwap connects to most major decentralised exchanges, such as Uniswap, Kyber, Curve or the 0x network. 

When you input a trading pair on ParaSwap, such as ETH to DAI, for instance, ParaSwap compares the prices of each exchange (accounting for your transaction's volume).

{{< /column >}}
{{< column >}}

![compare-rates-with-Paraswap](/images/rate-compare.png)

{{< /column >}}
{{< /block >}}

_ParaSwap examines at the rate for the given pair on all supported exchanges and displays the effective rate (accounting for slippage) for each._

---

{{< block "grid-2" >}}
{{< column >}}

![Paraswap-order-split](/images/order-split.png)

{{< /column >}}

{{< column >}}
#### Optimise Orders' Execution
ParaSwap does whatever it takes to find the best rate - including splitting your order across several decentralized exchanges.

Splitting orders is particularly effective for large transactions, such as the one presented here: a swap of 500 ETH to DAI, routed on three supports: 
1. 40% ParaSwapPool, 
2. 40% Uniswap V2, 
3. 20% Kyber

{{< /column >}}
{{< /block >}}

---

{{< block "grid-2" >}}
{{< column >}}

#### MultiPath (1/2): No Stones Left Unturned
**ParaSwap routing algorithm explore every relevant route**, including the ones involving extra hops. 

For instance, to buy ETH from USDT, a direct USDT -> ETH swap might not be the way. Getting the best rate might involve going USDT -> USDC -> ETH for instance.

No need to compute all this complexity (across all DEXes) by yourself - ParaSwap does it for you!

{{< /column >}}
{{< column >}}

![Paraswap-multipath](/images/paraswap-multipath.png)
_A large USDT -> ETH swap routed through MultiPath to beat the direct-pair price._

{{< /column >}}
{{< /block >}}

---

{{< block "grid-2" >}}
{{< column >}}

![Paraswap-aSNX-multipath](/images/multipath-aSNX.png)
_A swap from ETH to aSNX facilitated by ParaSwap_

{{< /column >}}

{{< column >}}
#### MultiPath (2/2) - Interactions Aggregation
MultiPath will also help you **interacting with several services with one gas-efficient transaction**. For instance, if you'd like to swap ETH to SNX and then deposit the SNX into Aave for aSNX, ParaSwap can do this for you in one step.

ParaSwap will interact with each contract - so in this case your ETH are swapped to SNX and then deposited into Aave (aSNX) in one transaction for a better gas efficiency.

{{< /column >}}
{{< /block >}}



---

### Gas Optimisations

{{< notice note >}}
ParaSwap implements several solutions to reduce gas usage across the platform, such implementing the GST2 gas token.
{{< /notice >}}

{{< block "grid-2" >}}
{{< column >}}

![etherscan-gas-tracker](/images/etherscan-gas-tracker.png)
_Check the current status of the gas market with **[⛽ EtherScan Gas Tracker](https://etherscan.io/gastracker)**._

{{< /column >}}

{{< column >}}
**Every trade made on ParaSwap is settled on the Ethereum network and incurs a gas cost paid to the miners** to verify and broadcast the transaction. The gas price (chosen by the person submitting the transaction) influences the time required for the transaction to be validated.

**If the gas price is too low, a transaction might never be incorporated into a block.**

The Gas Token (GST2) enables the tokenisation of gas when prices are low. The GST2 previously minted are then harnessed to reduce the effective gas costs when the Ethereum Network is most busy.
{{< /column >}}
{{< /block >}}

{{< notice tip >}}
The gas costs estimations displayed on ParaSwap.io are **a worst-case scenario**. Often, the effective price will be lower. While GST2 can be harnessed to optimize your trade, ParaSwap will refund you the gas cost saved.
{{< /notice >}}

---

### ParaSwapPool

{{< notice note >}}
On top of all major DEXes, ParaSwap has its private Market Maker pool. ParaSwapPool provides further opportunities to optimise the transactions, sometimes enabling our users to **beat the market rate**.
{{< /notice >}}

ParaSwap pools the liquidity provided by professional liquidity providers in the ParaSwapPool. This pool is included in any relevant trade, just like another decentralized exchange.

---

### Streamlined Allow Transactions

{{< notice note >}}
**With ParaSwap, one `Allow` rules them all!** Once you've allowed a given token on ParaSwap, you can exchange it on any DEX (through ParaSwap) - no further allow required!
{{< /notice >}}

#### Not familiar with `Allow` transactions? Read this 👇

When interacting with a DeFi service never used on a given wallet before, a specific transaction is required to enable tokens to be spent or moved around: `Allow`. The transaction must be repeated for each token spent/traded, and on each new service.

{{< notice info >}}
Since ETH is the base asset of the Ethereum network, it is the only asset that does not require an `Allow` transaction to be spent or utilized.
{{< /notice >}}

#### With ParaSwap `Allow` once and for all

With ParaSwap, you still need to perform the `Allow` for any new token you interact with. However, once you've allowed the ParaSwap contract, you'll be able to trade your tokens on any DEX - including potentially new DEXes added after your first trade.

---

### Understanding Risk & Hedging It

{{< notice note >}}
ParaSwap follows a strict procedure to reduce operational risk. ParaSwap never holds custody of your assets. For further insurance, you can also contract a cover on Nexus Mutual.
{{< /notice >}}

Since ParaSwap is a middleware, your funds are only exposed while a transaction is being processed. **ParaSwap never hold custody of your assets - you stay in full control**.

![ParaSwap-on-Nexus-Mutual](/images/nexus-mutual.png)

_As of Friday, Sep 04, a total of $8M (51.222 NXM) were staked on ParaSwap's contract. **[Source: NexusTracker](https://nexustracker.io/staking)**_

While being a middleware reduce the scope of risk, it doesn't eliminate it. The main operational risk lies in the failure of one of ParaSwap's contracts. We implement several solutions to hedge for this risk:
1. ParaSwap's contracts are audited. New versions go through a thorough audit process before being released.
2. Any user can subscribe to insurance covering the risk of a technical failure of ParaSwap's contract using Nexus Mutual.
3. To minimize the risk exposure, ParaSwap only integrates with services following thorough security practices.