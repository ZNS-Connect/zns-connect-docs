---
description: >-
  Official contract addresses used by the ZNS Launchpad across supported
  networks.
icon: xmark-to-slot
cover: .gitbook/assets/CONTRACT ADDRESSESontracts.png
coverY: 0
---

# Contract Addresses of Lauchpad

## Contract Addresses of Launchpad

Production contract addresses used by the ZNS Launchpad across supported networks.

These addresses are intended for wallets, explorers, exchanges, aggregators, analytics platforms and ecosystem partners integrating with ZNS Launchpad.

***

## Base Mainnet

#### Network Information

* Network: Base Mainnet
* Chain ID: 8453
* Native Currency: ETH
* Quote Asset: WETH

WETH

```
0x4200000000000000000000000000000000000006
```

#### ZNS Token Factory

```
0xAD6f6a5e5D37870D7325CA663644020fE67a042F
```

Responsible for deploying ZNS Launchpad tokens.

***

#### Launch Hook

```
0xAcf358b129423f0107B0bF892B3eFF6C770128Cc
```

Immutable Uniswap v4 Hook.

***

#### LP Locker

```
0xa70FACF8ddD62Fc14d62EF1500cc359eB1eAfb68
```

Permanent liquidity position locker.

***

#### Fee Locker

```
0x21e0e33370bDe6F6ed0cf46bBE74BA19fEDE4961
```

Fee distribution contract.

***

#### Anti-MEV Module

```
0x04a6E9093532b912B0C96744E720F7d01cd17223
```

Dynamic launch protection.

***

#### Creator Vault

```
0xC49aF77c896F9dA8FdbE7Cd023A3F8cfCDD25A44
```

Creator token vesting.

***

#### Dev Buy Extension

```
0x4Fba7F8aaEa4A02Ca509A1c7F588091D3624AcF2
```

Optional developer purchase extension.

***

#### Treasury

```
0xDB38F82cc039B97996362D2a63E9C2a55A31833b
```

Protocol treasury.

***

#### Uniswap v4

PoolManager

```
0x498581fF718922c3f8e6A244956aF099B2652b2b
```

PositionManager

```
0x7C5f5A4bBd8fD63184577525326123B519429bDc
```

UniversalRouter

```
0x6fF5693b99212Da76ad316178A184AB56D299b43
```

StateView

```
0xA3c0c9b65baD0b08107Aa264b0f3dB444b867A71
```

Permit2

```
0x000000000022D473030F116dDEE9F6B43aC78BA3
```

***

## Robinhood Chain

#### Network Information

* Network: Robinhood Chain Mainnet
* Chain ID: 4663
* Native Currency: ETH
* Quote Asset: WETH

RPC

```
https://rpc.mainnet.chain.robinhood.com
```

Explorer

```
https://robinhoodchain.blockscout.com
```

WETH

```
0x0Bd7D308f8E1639FAb988df18A8011f41EAcAD73
```

***

#### ZNS Token Factory

```
0x960d2d412ed19DaD39037D2334891AeBd660a32e
```

***

#### Launch Hook

```
0x0b1DAAD7084ACA64e2C21cF1b16374b8a26968cc
```

***

#### LP Locker

```
0xbcf8Da3827345BC3325bAAE2DC91b6b7AD324Bf9
```

***

#### Fee Locker

```
0x4d9E8a416576Fd56C723eff6C9200e3330c5d3d4
```

***

#### Anti-MEV Module

```
0xddDA09C81290558e5e06b6adA17363F91Adc27F7
```

***

#### Creator Vault

```
0x76e3C27B4f39e1a9589Ff6CAba3755aA066DAf12
```

***

#### Dev Buy Extension

```
0x31A6A66093b63b6dA724F6d4C858a9B4157d7e1E
```

***

#### Treasury

```
0xDB38F82cc039B97996362D2a63E9C2a55A31833b
```

***

#### Uniswap v4

PoolManager

```
0x8366a39CC670B4001A1121B8F6A443A643e40951
```

PositionManager

```
0x58daec3116aae6D93017bAAea7749052E8a04fA7
```

UniversalRouter

```
0x8876789976dEcBfCbBbe364623C63652db8C0904
```

StateView

```
0xF3334192D15450CdD385c8B70e03f9A6bD9E673b
```

Quoter

```
0x8Dc178eFB8111BB0973Dd9d722ebeFF267c98F94
```

Permit2

```
0x000000000022D473030F116dDEE9F6B43aC78BA3
```

***

## Solana Mainnet

#### Network Information

* Network: Solana Mainnet Beta
* Native Currency: SOL
* Quote Asset: Wrapped SOL (wSOL)

wSOL Mint

```
So11111111111111111111111111111111111111112
```

***

#### Core Programs

Dynamic Bonding Curve

```
dbcij3LWUppWqq96dh6gJWwBifmcGfLSB5D4DuSMaqN
```

Meteora DAMM v2

```
cpamdpZCGKUy5JxQXB4dcpGPiikHawvSWAd6mEn1sGG
```

ZNS Splitter

```
8iPFG3f2Y8oGLN6g48NpRQiL3Eu4RzcdNku7qpnNNcbw
```

***

#### Launch Configurations

Standard

```
Ag218y7qLGf3gmLRzPZMaLu3ghnGUZstpjeiUi6GGPz9
```

Safe

```
DEKVtkTtGf14fiVY2pa1WykHJpm4XzTA745SfGrSH7mv
```

Certified

```
9qYwiLdfvKtCEQA5M1YgTYSXjZdLQ5XobE7vW3E1tePb
```

***

## Integration Notes

* Every supported network has an independent production deployment.
* Base and Robinhood launch directly into Uniswap v4 liquidity pools.
* Solana launches use Meteora Dynamic Bonding Curve followed by Meteora DAMM v2.
* WETH is the quote asset on EVM networks.
* Wrapped SOL (wSOL) is the quote asset on Solana.
* No bonding-curve contracts are used on EVM deployments.
* All Launch Hooks are immutable.
* No proxy contracts are used.
* No upgrade permissions exist.
* Third-party wallets, explorers, aggregators and analytics platforms may safely integrate using the public addresses listed above.
