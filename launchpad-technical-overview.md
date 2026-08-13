---
description: >-
  Technical reference for the ZNS Launchpad architecture, smart contracts,
  security model and integration guidelines.
icon: compress
cover: .gitbook/assets/ZNS LAUNCHPAD.png
coverY: 0
layout:
  width: default
  cover:
    visible: true
    size: full
    mask: none
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# Launchpad Technical Overview

***

## Launchpad Technical Overview

Welcome to the technical documentation for the ZNS Launchpad.

This section provides the information most frequently requested by launchpads, wallets, DEX aggregators, explorers, analytics platforms, exchanges and ecosystem partners integrating with ZNS Launchpad.

***

### Overview

ZNS Launchpad is a decentralized token launch platform supporting both **EVM** and **Solana** deployments.

On EVM networks, every launch is deployed directly into a **Uniswap v4 liquidity pool**.

On Solana, launches begin on **Meteora Dynamic Bonding Curve (DBC)** and automatically graduate into a **DAMM v2 liquidity pool**.

Unlike traditional launchpads, ZNS Launchpad does not use:

* Bonding Curves (EVM)
* Presales
* Fair Launch Auctions
* Migration Contracts
* Secondary DEX Deployments

Liquidity becomes available immediately after deployment.

***

### Core Principles

Every launch follows the same architecture:

* Native protocol deployment
* Immutable smart contracts / programs
* Immutable launch configuration
* Dynamic fee model
* Permanent liquidity
* Cross-chain architecture
* Fully on-chain execution

No proxy contracts are used.

No owner-controlled swap logic exists.

***

### Launch Flow

#### EVM

Each launch follows a single deployment flow:

1. Deploy ERC-20 token
2. Create a Uniswap v4 liquidity pool
3. Initialize liquidity
4. Lock LP position
5. Activate Launch Hook
6. Enable trading

#### Solana

Each launch follows the native Solana flow:

1. Create SPL token
2. Deploy Meteora DBC pool
3. Open bonding curve
4. Automatic graduation
5. Create DAMM v2 liquidity pool
6. Continue trading

After deployment, tokens become immediately tradable.

***

### Supported Networks

Current production deployments:

| Network         | Architecture          | Chain        |
| --------------- | --------------------- | ------------ |
| Base Mainnet    | Uniswap v4            | 8453         |
| Robinhood Chain | Uniswap v4            | 4663         |
| Solana Mainnet  | Meteora DBC → DAMM v2 | Mainnet-beta |

Additional EVM-compatible networks may be supported in future releases.

***

### Quote Assets

Supported quote assets:

* **Base:** WETH
* **Robinhood Chain:** WETH
* **Solana:** Wrapped SOL (wSOL)

Other quote assets such as USDC or USDT are not currently supported.

***

### Documentation

This documentation consists of three sections:

* Launchpad Technical Overview
* Smart Contracts
* Contract Addresses

For technical integration questions or launchpad integration requests, please contact the ZNS team.

***

