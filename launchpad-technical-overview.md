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

## Launchpad Technical Overview

Welcome to the technical documentation for the ZNS Launchpad.

This documentation provides the information most frequently requested by launchpads, wallets, DEX aggregators, explorers, analytics platforms, exchanges, and ecosystem partners integrating with ZNS Launchpad.

***

### Overview

ZNS Launchpad is a decentralized token launch platform built entirely on **Uniswap v4**.

Unlike traditional launchpads, ZNS Launchpad launches tokens directly into live Uniswap v4 liquidity pools.

The platform does **not** use:

* Bonding Curves
* Presales
* Fair Launch Auctions
* Migration Contracts
* Secondary DEX Deployments

Liquidity is available immediately after deployment.

***

### Core Principles

Every launch follows the same architecture:

* Native Uniswap v4 deployment
* Immutable smart contracts
* Immutable Launch Hook
* Dynamic fee pools
* Permanent LP locking
* Canonical Universal Router compatibility
* Fully on-chain execution

No proxy contracts are used.

No owner-controlled swap logic exists.

***

### Launch Flow

Each launch is completed within a single deployment flow:

1. Deploy ERC-20 token
2. Create a Uniswap v4 liquidity pool
3. Initialize liquidity
4. Lock LP position
5. Activate Launch Hook
6. Enable trading

After deployment, the token becomes immediately tradable.

***

### Supported Networks

Current production deployments:

| Network         | Chain ID |
| --------------- | -------: |
| Base Mainnet    |     8453 |
| Robinhood Chain |      466 |

Additional EVM-compatible networks may be supported in future releases.

***

### Quote Asset

All launch pools use **WETH** as the quote asset.

Other quote assets such as USDC or USDT are not supported.

***

### Documentation

This documentation consists of three sections:

* Launchpad Technical Overview
* Smart Contracts
* Contract Addresses

For technical questions or integration requests, please contact the ZNS team.
