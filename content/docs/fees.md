---
title: "Fees & Business Model"
weight: 7
description: >
  An overview of ParaSwap's revenue streams
---

This page provides an overview of the revenue streams flowing in and out of ParaSwap. It provides clarity on the revenue structure for integrators and helps our users better understand the business model.

ParaSwap can either be used directly, through our website paraswap.io or accessed through a third party integrating with the service:
1. On [ParaSwap.io](https://paraswap.io), there is no extra markup.
2. It's up to the services integrating with ParaSwap to decide if they want to charge a commission on the swaps facilitated. The ParaSwap API streamlines the collection of a fee, if desired, thanks to the Revenue Sharing contract.

---

### 💸 ParaSwap's Fee = 0

ParaSwap currently operates with no fee: **there is no additional markup taken on swaps while interacting directly with the service**. Users exchanging tokens on paraswap.io only face the cost of broadcasting a transaction on the Ethereum network (gas costs).

### ♻ Revenue Sharing (Integrators)

Third-party services, such as wallets, can easily integrate with ParaSwap using to the API. They can control the fee structure of their integration with the revenue sharing smart contract. 

If they chose so, they can charge a commission on the swaps they facilitate. When an integrating service uses this feature, 20% of the revenues collected (by default) are shared with ParaSwap.