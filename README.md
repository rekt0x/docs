---
description: THORChain, THORNodes, Wallets and the ecosystem.
---

# Introduction

## About

THORChain is a decentralised cross-chain liquidity protocol which uses the [Tendermint](https://tendermint.com/) consensus engine, [Cosmos-SDK](https://cosmos.network/) state machine and GG20 [Threshold Signature Scheme](https://eprint.iacr.org/2019/114.pdf) (TSS). It does not peg or wrap assets, it manages funds directly in on-chain vaults, and secures those funds using economic security. It could be described as a "cross-chain automated market maker (AMM), like Uniswap".&#x20;

## Innovations

There a numerous innovations in the THORChain Protocol that were built with first principles to be decentralised, resistant to capture and sustainable as possible:

1. **Capped Proof Of Bond** validator selection keeps the network decentralised and Nakamoto Coefficient high.&#x20;
2. **3-Day Validator Churning** stops validator stagnation, proves spendability of funds and upgrades the network with minimal governance.&#x20;
3. **Asynchronous Network Upgrades** allows validators to upgrade to a new protocol version in their own time, with the network upgrading without ever breaking consensus.&#x20;
4. **Chain-agnostic Bifrost Protocol** handles UTXO, EVM, BFT and Cryptonote chain connections with minimal core-logic nuances.&#x20;
5. **Incentive Pendulum** streams rewards to Validators and Liquidity Providers to target a Network Security ratio that always keeps funds secured.&#x20;
6. **Continuous Liquidity Pools** that allows single-sided liquidity provision and uses liquidity-sensitive fees to resist price attacks.
7. **Swap Queue** that orders swaps based on price impact in each block, which stops sandwich attacks and most other forms of Miner Extractable Value (MEV).&#x20;
8. **Liquidity Synths** to enable fast low-fee swaps across L1 pools and power single-sided Savers. Synths are a hybrid collaterised-pegged asset design that contribute to liquidity.&#x20;
9. **Derived Asset Collateral** to enable L1 lending, using the RUNE asset to underwrite the liability. This enables no interest, no liquidation, no expiry loans.&#x20;

## 3-Pillars of THORChain: Security, Liquidity, Volume

THORChain contributors work to three goals:

1. Improve the **Security** of the network, via either **Functional** (Solvency Checker, Node Pause, TxOut Throttler), **Procedural** (THORSec, Stagenet testing, PR reviews) or **Economic** (RUNE in the bond, or value of the $RUNE in the bond) Security.&#x20;
2. Improve the **Liquidity** of the network, via Total Value Locked (TVL), or better UX around providing liquidity (Savers).&#x20;
3. Improve the **Volume** of the network, via Swap UX (Synths, Order Books), or wallet Integrations (Quotes Endpoint, Dev UX, Business Development)

You can learn how THORChain works here:

{% content-ref url="how-it-works/" %}
[how-it-works](how-it-works/)
{% endcontent-ref %}

## THORChain Finance

Building on the foundation of liquidity pools, THORChain pursues three important financial primitives:

1. Allow a user to **Swap** {_Asset X on Chain A_}, to {_Asset Y on Chain B_}.&#x20;
2. Allow a user to **Save** {_Asset X on Chain A_}.
3. Allow a user to **Lend** {_Asset X on Chain A_}, to **Borrow** {_Asset Y on Chain B_}.&#x20;

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

## THORNodes

THORNodes service the THORChain network, of which there is intended to be initially 100, but can scale to 250+. The design goal of THORChain is such that anyone can join the network with the required funds (permissionless) and be anonymous, yet still be secure. THORChain takes this a step further by having a high churn schedule, kicking out nodes continuously. This high-churn network ensures that it is censorship-resistant, evades capture and resists centralisation.

Each THORNode is comprised of several independent servers in a cluster, which run full-nodes for each connected chain.&#x20;

{% content-ref url="roles/node-operators.md" %}
[node-operators.md](roles/node-operators.md)
{% endcontent-ref %}

## Developers

Developers build products that integrate with THORChain, such as wallets, exchanges and other services. Developers simply need to connect to Midgard, but they should also consider running their own nodes.

The order of integration is as follows:

1. Connect to THORChain via Midgard or THORNode.
2. Use data provided to display pools, assets, users, as well as get quotes for swaps/savers/lending.
3. Use existing wallet infrastructure to send L1 transactions
4. Use `xchainjs` packages to sign transactions and broadcast.

Learn more at the [`Dedicated Dev Site`](https://dev.thorchain.org/thorchain-dev/).

## CONTRIBUTING

THORChain is a public project. If you want to join the community or work on THORChain Core join the [Dev Discord](https://discord.gg/kvZhpEtHAw).
