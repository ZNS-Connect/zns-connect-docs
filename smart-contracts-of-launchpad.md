---
description: Official smart contracts used by the ZNS Launchpad infrastructure.
icon: water-arrow-up
cover: .gitbook/assets/Smart Contracts.png
coverY: 0
---

# Smart Contracts of Launchpad

***

## Smart Contracts of Launchpad

Official smart contracts and native programs powering the ZNS Launchpad.&#x20;

The ZNS Launchpad supports both **EVM (Uniswap v4)** and **Solana (Meteora DBC / DAMM v2)** deployments.

Every launch follows deterministic deployment with immutable on-chain execution.

***

### Architecture

#### EVM

Each deployment consists of:

* ERC-20 Token
* Uniswap v4 Pool
* Launch Hook
* LP Locker
* Fee Locker
* Creator Vault

Each component has a dedicated responsibility and operates without upgrade permissions.

***

#### Solana

Each deployment consists of:

* SPL Token
* Meteora Dynamic Bonding Curve (DBC)
* DAMM v2 Liquidity Pool
* Creator Fee Vault
* Treasury Accounts

Trading automatically continues after graduation from the bonding curve into DAMM v2 liquidity.

***

### Launch Hook (EVM)

The Launch Hook extends the native Uniswap v4 lifecycle.

Responsibilities include:

* Launch validation
* Fee distribution
* Creator rewards
* Protocol fee accounting
* Trading rules

Properties:

* Immutable
* No proxy
* No upgradeability
* No owner-gated swap logic

Applications may submit empty `hookData`.

All swaps execute through the canonical **Uniswap Universal Router**.

***

### Solana Programs

Solana deployments use native programs instead of Uniswap Hooks.

Responsibilities include:

* Token launch
* Dynamic Bonding Curve
* Automatic graduation
* DAMM v2 liquidity creation
* Creator fee accounting

All programs execute natively on Solana without migration contracts.

***

### Liquidity

#### EVM

Every token launches directly into a live **Uniswap v4 liquidity pool**.

Pool parameters include:

* Pool ID
* Hook Address
* Token Address
* Quote Asset (WETH)
* Tick Spacing
* Dynamic Fee

Liquidity becomes available immediately after deployment.

***

#### Solana

Every token launches through a **Meteora Dynamic Bonding Curve**.

After the graduation threshold is reached:

* Liquidity migrates automatically to DAMM v2.
* Trading continues without interruption.
* No manual migration is required.

***

### Security

The protocol follows several security principles:

* Immutable smart contracts (EVM)
* Immutable programs (Solana)
* No proxy contracts
* No upgrade permissions
* Native execution
* Fully on-chain settlement

This minimizes trust assumptions while maintaining compatibility with both ecosystems.

***

### Integration

Projects integrating with ZNS Launchpad typically require only:

#### EVM

* Pool ID
* Hook Address
* Token Address
* Universal Router
* Chain ID

#### Solana

* Token Mint
* Meteora DBC Pool
* DAMM v2 Pool
* Program IDs

All production addresses are available on the **Contract Addresses** page.

***
