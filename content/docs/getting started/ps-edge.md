---
title: "ParaSwap's Edge"
weight: 3
description: >
  Why using ParaSwap can be more effective than interacting directy with DeFi services  
---

This page summarizes the main benefits you can draw from using ParaSwap's over interacting with the decentralised finance services directly, or using another middleware.

### Decentralized Exchanges Aggregation

{{< notice note >}}
ParaSwap scours dozens of decentralised exchanges to secure the best rates. Thanks to a refine pathing analysis logic, all options are explored, including splitting your order on several exchanges or looking for alternative swapping routes. 
{{< /notice >}}

{{< block "grid-2" >}}
{{< column >}}
#### Find the Best Rate

ParaSwap connect to most major decentralised exchanges, such as Uniswap, Kyber, Curve or the 0x network. 

When you input a trading pair on ParaSwap, such as ETH to DAI for instance, ParaSwap compare the prices of each exchange (accounting for your transaction's volume).

> ParaSwap can execute a given order on both Uniswap and Kyber for instance, at the same time and in one transaction.
{{< /column >}}
{{< column >}}

![compare-rates-with-Paraswap](/images/rate-compare.png)
_ParaSwap examines at the rate for the given pair on all supported exchanges and displays the effective rate (accounting for slippage) for each._

{{< /column >}}
{{< /block >}}

{{< block "grid-2" >}}
{{< column >}}

![Paraswap-order-split](/images/order-split.png)

{{< /column >}}

{{< column >}}

#### Optimise the Order's Execution

Whatever gets you the best rate, ParaSwap does - including splitting your order accross several decentralized exchanges.

Splitting orders is particularly effective for large transactions, such as the one presented here: a swap of 500 ETH to DAI, routed on three supports: 
1. 40% ParaSwapPool, 
2. 40% Uniswap V2, 
3. 20% Kyber

{{< /column >}}
{{< /block >}}

---

### ParaSwap's Pool

{{< notice note >}}
On top of all major DEXes, ParaSwap has its own private Market Maker pool. ParaSwap's pool provides further opportunities to optimisatise the transactions, sometimes enabling our users to **beat the market rate**.
{{< /notice >}}

Something

---

### Gas Optimisations

{{< notice note >}}
ParaSwap implements several solutions to reduce gas usage accross the platform, such as the GST2 gas token.
{{< /notice >}}

Something

{{< notice tip >}}
Please note that the gas costs estimations featured on ParaSwap.io are **a worst case scenario**. Often, the effective price will be lower. While GST2 can be harnessed to optimize your trade, ParaSwap will refund you the gas cost saved.
{{< /notice >}}

---

### Streamlined Allow Transactions

{{< notice note >}}
**With ParaSwap, one allow rules them all!** Once you've allowed a given token on ParaSwap, you can exchange it on any DEX (through ParaSwap) - no further allow required!
{{< /notice >}}

#### Not familiar with `Allow` transactions? Read this 👇

When interacting with a DeFi service never used on a given wallet before, a specific transaction is required to enable tokens to be spent or moved around: `Allow`. The transaction must be repeated for each tokens spent/traded, and on each new service.

{{< notice info >}}
Since ETH is the base asset of the Ethereum network, it does not require an `Allow` transaction to be spent or utilized.
{{< /notice >}}

#### With ParaSwap `Allow` once and for all

With ParaSwap, you still need to perform the `Allow` for any new token you interact with. However, once you've allowed the ParaSwap contract, you'll be able to trade your tokens on any DEX - including potentially new DEXes added after your first trade.

---

### Nexus Mutual Insurance

{{< notice note >}}
2 line explainer
{{< /notice >}}

zomg