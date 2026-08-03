---
description: >-
  Official contract addresses used by the ZNS Launchpad across supported
  networks.
cover: .gitbook/assets/1800-360 zns-2.png
coverY: 0
---

# Contract Addresses of Lauchpad

## Contract Addresses

Official smart contract deployments for the ZNS Launchpad.

Every supported network has its own independent deployment while preserving the same launch architecture.

***

## Base Mainnet

Chain ID

8453

Explorer

https://basescan.org

Native Currency

ETH

Quote Asset

WETH 0x4200000000000000000000000000000000000006

***

### ZNS Factory

Responsible for deploying every new token.

0xAD6f6a5e5D37870D7325CA663644020fE67a042F

***

### Launch Hook

Custom Uniswap v4 Hook powering every launch.

0xAcf358b129423f0107B0bF892B3eFF6C770128Cc

***

### LP Locker

Holds every LP NFT permanently.

0xa70FACF8ddD62Fc14d62EF1500cc359eB1eAfb68

***

### Fee Locker

Stores creator and protocol trading fees.

0x21e0e33370bDe6F6ed0cf46bBE74BA19fEDE4961

***

### Anti-MEV Module

Protects launches during the first minute.

0x04a6E9093532b912B0C96744E720F7d01cd17223

***

### Creator Vault

Time-locked creator allocation.

0xC49aF77c896F9dA8FdbE7Cd023A3F8cfCDD25A44

***

### Dev Buy Extension

Optional developer buy module.

0x4Fba7F8aaEa4A02Ca509A1c7F588091D3624AcF2

***

### Treasury

Platform fee recipient.

0xDB38F82cc039B97996362D2a63E9C2a55A31833b

***

### Uniswap v4 PoolManager

0x498581fF718922c3f8e6A244956aF099B2652b2b

***

### Uniswap v4 PositionManager

0x7C5f5A4bBd8fD63184577525326123B519429bDc

***

### Uniswap v4 UniversalRouter

0x6fF5693b99212Da76ad316178A184AB56D299b43

***

### Uniswap v4 StateView

0xA3c0c9b65baD0b08107Aa264b0f3dB444b867A71

***

### Permit2

0x000000000022D473030F116dDEE9F6B43aC78BA3

***

## Robinhood Chain

Chain ID

4663

Explorer

https://robinhoodchain.blockscout.com

Native Currency

ETH

Quote Asset

WETH 0x0Bd7D308f8E1639FAb988df18A8011f41EAcAD73

***

### ZNS Factory

0x960d2d412ed19DaD39037D2334891AeBd660a32e

***

### Launch Hook

0x0b1DAAD7084ACA64e2C21cF1b16374b8a26968cc

***

### LP Locker

0xbcf8Da3827345BC3325bAAE2DC91b6b7AD324Bf9

***

### Fee Locker

0x4d9E8a416576Fd56C723eff6C9200e3330c5d3d4

***

### Anti-MEV Module

0xddDA09C81290558e5e06b6adA17363F91Adc27F7

***

### Creator Vault

0x76e3C27B4f39e1a9589Ff6CAba3755aA066DAf12

***

### Dev Buy Extension

0x31A6A66093b63b6dA724F6d4C858a9B4157d7e1E

***

### Treasury

0xDB38F82cc039B97996362D2a63E9C2a55A31833b

***

### Uniswap v4 PoolManager

0x8366a39CC670B4001A1121B8F6A443A643e40951

***

### Uniswap v4 PositionManager

0x58daec3116aae6D93017bAAea7749052E8a04fA7

***

### Uniswap v4 UniversalRouter

0x8876789976dEcBfCbBbe364623C63652db8C0904

***

### Uniswap v4 StateView

0xF3334192D15450CdD385c8B70e03f9A6bD9E673b

***

### Uniswap v4 Quoter

0x8Dc178eFB8111BB0973Dd9d722ebeFF267c98F94

***

### Permit2

0x000000000022D473030F116dDEE9F6B43aC78BA3

***

## Notes

* Every launch is deployed directly into a Uniswap v4 liquidity pool.
* No bonding curve contracts exist.
* No migration contracts exist.
* No presale contracts exist.
* Every network has its own independent deployment.
* All contracts listed above are production deployments.
