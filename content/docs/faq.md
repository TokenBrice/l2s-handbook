---
title: "Frequently Asked Questions"
weight: 2
description: >
  Just discovered ParaSwap? This page answers recurring questions to get ready to swap.
---

### What is ParaSwap about?

ParaSwap is middleware aggregating many decentralized exchanges (DEX) and other services in one comprehensive interface. For any given trade, ParaSwap checks the rates on all supported DEX and implements further optimizations to get the best rate possible - sometimes even beating the markets!

---

### What do I need to use ParaSwap?

To get started with ParaSwap, the only thing you need is an Ethereum wallet: our website currently supports [MetaMask](https://metamask.io/). ParaSwap can also be accessed through third parties services integrating with our API.

---

### How does ParaSwap work?

1. The user inputs a token pair and amount, for instance: swapping 3000 DAI for ETH.
2. ParaSwap checks the rate on all the exchanges it supports where the pair is available.
3. It provides a comprehensive overview of the best trading route found to the user.
4. The user signs a first transaction ("Allow") to enable ParaSwap to interact with their DAI balance. (This step is not always required, see below)
5. The user can now click the "Swap Now" button to confirm his transaction and execute the swap.
6. The swapping contract executes the swap and delivers the purchased tokens to the user.

---

### What are the fees?

**ParaSwap is currently not charging any fee for the service provided.**

Yet since ParaSwap is a **decentralized service enabled by smart contracts running on the Ethereum blockchain.** Interacting with it incurs a gas cost (paid in ETH): this is the cost of the commons - a fee paid miners who secure the Ethereum blockchain.

---

### Why do I need to sign two transactions to swap ("Allow")?

**To interact with tokens stored in a user wallet, the ParaSwap contract needs the permission - that's the `allow` transaction.** All tokens on the Ethereum blockchain require this transaction, but for ETH, the native asset of the network.

When initiating a token exchange on ParaSwap, you'll be asked to allow the token being spent. You have two options:

1. **Exact Amount** ("Unlock XXX DAI"), where the allowance is granted for the exact amount of tokens being exchanged.
2. **Permanently Unlock**, where the allowance is granted without limits. This enables you to avoid further allow transaction (and their associated gas costs) if you interact with the same token again on ParaSwap.

---

### What does slippage mean?

Transactions on decentralized exchanges are facilitated thanks to third parties providing liquidity: they do so by committing a balanced amount of tokens to a liquidity pool. 

**When the available liquidity is too slim compared to the trade at play, slippage can occur**: the effective rate for the transaction is below the market because the trade is significantly depleting liquidity pools.

ParaSwap swapping contract is able to split trades onto several exchanges at once to better the rate. Several other strategies are implemented to reduce splippage and optimise the rate. They are explained in the next section:

<div align ="center">{{< button "/docs/ps-edge/" "ParaSwap Edge" >}}</div>