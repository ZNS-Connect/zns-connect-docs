---
description: Official smart contracts used by the ZNS Launchpad infrastructure.
---

# Smart Contracts of Launchpad

## Smart Contracts

This page contains the official smart contracts used by the ZNS Launchpad.

All launches are built directly on top of Uniswap v4. ZNS does not use upgradeable launch contracts, migration contracts, or owner-controlled liquidity contracts.

***

### Architecture

Every token launch follows the same architecture:

* Token Deployment
* Pool Creation
* Hook Initialization
* Liquidity Initialization
* Trading Activation

Liquidity becomes available immediately after deployment.

There is no migration stage.

***

### Pool Manager

The ZNS Launchpad uses the official Uniswap v4 PoolManager.

The PoolManager is responsible for:

* Pool creation
* Liquidity management
* Swap execution
* Fee accounting

***

### Hook Contracts

Each launch uses an immutable Hook contract.

Properties:

* Immutable
* No proxy
* No upgradeability
* No owner-gated functions
* hookData is optional

Applications can submit empty hookData without affecting swap execution.

All swaps execute through the canonical Uniswap Universal Router.

***

### Pool Structure

Every launch creates a standard Uniswap v4 liquidity pool.

Typical parameters include:

* Chain ID
* Pool ID
* Hook Address
* Token Address
* Quote Asset
* Tick Spacing
* Dynamic Fee

***

### Security

The ZNS Launchpad follows several security principles.

* Immutable smart contracts
* No proxy contracts
* No upgrade permissions
* No migration contracts
* No owner-controlled liquidity
* Standard Uniswap v4 execution

***

### Integration

Projects integrating with ZNS generally require only:

* Pool ID
* Hook Address
* Chain ID
* Token Address

These values are sufficient for wallets, explorers, analytics platforms, DEX aggregators, portfolio trackers and ecosystem integrations.
