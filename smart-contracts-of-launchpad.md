---
description: Official smart contracts used by the ZNS Launchpad infrastructure.
icon: water-arrow-up
cover: .gitbook/assets/Smart Contracts.png
coverY: 0
---

# Smart Contracts of Launchpad

## Smart Contracts of Launchpad

The ZNS Launchpad is built entirely on immutable smart contracts running on Uniswap v4.

Every launch follows the same architecture across all supported networks, providing deterministic deployment, immediate liquidity, and fully on-chain execution.

***

### Architecture

Each launch consists of several independent components working together:

* ERC-20 Token
* Uniswap v4 Pool
* Launch Hook
* LP Locker
* Fee Locker
* Creator Vault

Each component has a dedicated responsibility and operates without upgrade permissions.

***

### Launch Hook

The Launch Hook extends the native Uniswap v4 pool lifecycle.

Responsibilities include:

* Launch validation
* Fee distribution
* Creator rewards
* Protocol fee accounting
* Trading rules

The hook is immutable.

It contains:

* No proxy
* No upgradeability
* No owner-gated swap logic

Applications may submit empty `hookData`.

All swaps execute through the canonical **Uniswap Universal Router**.

***

### Liquidity Pool

Every token launches directly into a live **Uniswap v4 liquidity pool**.

Pool parameters include:

* Pool ID
* Hook Address
* Token Address
* Quote Asset (WETH)
* Tick Spacing
* Dynamic Fee

Liquidity becomes available immediately after deployment.

There is no migration stage.

***

### Security

The protocol follows several security principles:

* Immutable contracts
* No proxy contracts
* No upgrade permissions
* No migration contracts
* No owner-controlled liquidity
* Native Uniswap v4 execution

This minimizes trust assumptions while maintaining full compatibility with the Uniswap ecosystem.

***

### Integration

Projects integrating with ZNS Launchpad typically require only:

* Pool ID
* Hook Address
* Token Address
* Universal Router
* Chain ID

All production contract addresses are available on the **Contract Addresses** page.
