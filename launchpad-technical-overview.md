---
description: >-
  Technical reference for the ZNS Launchpad architecture, smart contracts,
  security model and integration guidelines.
icon: compress
cover: .gitbook/assets/1800-360 zns.png
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

This section contains the information most frequently requested by launchpads, wallets, aggregators, exchanges, explorers and ecosystem partners integrating with ZNS Launchpad.

The documentation covers our launch architecture, smart contracts, APIs, security model, fee distribution and integration guidelines.

***

### Overview

ZNS Launchpad is a decentralized token launch platform built entirely on **Uniswap v4**.

Unlike traditional launchpads, ZNS does **not** use:

* Bonding Curves
* Presales
* Fair Launch Auctions
* Migration Contracts
* Temporary Liquidity

Every token launches directly into a live **Uniswap v4 liquidity pool**.

Liquidity exists immediately after deployment.

There is no migration stage.

There is no graduation process.

There is no secondary DEX deployment.

***

### Core Principles

Every launch follows the same architecture.

• Direct Uniswap v4 deployment

• Immutable smart contracts

• No upgradeable Hook

• No proxy contracts

• Permanent LP locking

• Dynamic fee pools

• Canonical Universal Router compatibility

• Fully on-chain launch process

***

### Launch Flow

Every token launch consists of a single on-chain transaction.

The transaction performs:

1. Deploy ERC-20 token
2. Initialize a new Uniswap v4 pool
3. Deploy liquidity
4. Lock LP position
5. Activate Hook
6. Enable trading

Once the transaction completes, the token is immediately tradable.

***

### Supported Networks

Current production networks:

| Network         | Chain ID |
| --------------- | -------: |
| Base            |     8453 |
| Robinhood Chain |     4663 |

Additional EVM networks may be supported in future releases.

***

### Quote Asset

All launchpad pools use **WETH**.

Other quote assets such as USDC or USDT are not supported.

The quote token is enforced at the contract level.

***

### Launch Architecture

Every launch uses:

* ERC-20 Token
* Uniswap v4 Pool
* Immutable Hook
* Dynamic Fee Pool
* LP Locker
* Fee Locker
* Creator Vault
* Anti-MEV Module

No proprietary AMM is used.

All swaps are executed through the standard **Uniswap v4 Universal Router**.

***

### Security

The launchpad has been designed with simplicity and transparency as primary goals.

Key security properties include:

* Immutable Hook contracts
* No owner-controlled swap logic
* No upgradeable proxies
* No hidden migration contracts
* Permanent LP locking
* Permissionless trading
* Standard Uniswap v4 architecture

***

### Documentation Structure

This section contains the following technical documentation:

* Smart Contract Addresses
* Launch Architecture
* Hook Documentation
* Fee Distribution
* Anti-Sniping Protection
* Launch Flow
* Public API
* GraphQL Subgraphs
* Integration Guide
* Frequently Asked Questions

Each page can be referenced independently by ecosystem partners during integrations.

***

For technical questions, integration requests or partnership inquiries, please contact the ZNS team.
