---
description: >-
  Interacts with blockchain domain names, resolving addresses, retrieving
  metadata
cover: ../.gitbook/assets/SDK.png
coverY: 0
---

# ZNS SDK

### ZNS Connect SDK Overview

**Earn Revenue Sharing**

Integrate the ZNS Connect SDK into your third-party frontend and benefit from revenue sharing on all domain minting activities. Depending on your brand, name service platform, or integration, you can earn up to 30-40% of the revenue generated through the SDK.

**Key Functionalities**

The ZNS Connect SDK offers a robust set of functionalities to interact with blockchain domain names:

* **Resolve Addresses:** Fetch the blockchain address associated with a given domain.
* **Retrieve Metadata:** Access detailed information about a specific domain.
* **Check Domain Availability:** Determine whether a domain name is already registered or available.
* **Manage Domains:** Perform various operations such as registering new domains and resolving domain ownership.

<mark style="color:orange;">**Link to NPM**</mark>**&#x20;:** [https://www.npmjs.com/package/zns-sdk](https://www.npmjs.com/package/zns-sdk)

<mark style="color:blue;">**Link to GitHub**</mark><mark style="color:blue;">:</mark> [https://github.com/ZNS-Connect/zns-sdk-v3](https://github.com/ZNS-Connect/zns-sdk-v3)

Below is the detailed documentation for each function available in the SDK:

### Functions

The ZNSConnect SDK provides a set of functionalities to interact with blockchain domain names, including resolving addresses, getting metadata, checking domain availability, and more. Below is the documentation for each function available in the SDK.

### Functions



#### `resolveAddress`



Resolves the blockchain address for a given top-level domain (TLD) and address.

| Parameter | Type     | Description                                             |
| --------- | -------- | ------------------------------------------------------- |
| `tld`     | `string` | The top-level domain (e.g., 'ink', 'future').           |
| `address` | `string` | The blockchain address to resolve (prefixed with `0x`). |

**Returns:** `Promise<any>` - The resolution result.

**Example:**

```
const result = await ZNSConnect.resolveAddress('ink', '0x123...');
console.log(result);
```

#### `resolveDomain`



Resolves the owner of a given domain.

| Parameter | Type     | Description                 |
| --------- | -------- | --------------------------- |
| `domain`  | `string` | The domain name to resolve. |

**Returns:** `Promise<string>` - The owner's address.

**Example:**

```
const owner = await ZNSConnect.resolveDomain('example.ink');
console.log(owner);
```

#### `getRegistry`



Gets the registry information for a given domain.

| Parameter | Type     | Description                 |
| --------- | -------- | --------------------------- |
| `domain`  | `string` | The domain to get info for. |

**Returns:** `Promise<any>` - The registry information.

**Example:**

```
const registry = await ZNSConnect.getRegistry('example.ink');
console.log(registry);
```

#### `getMetadata`



Retrieves metadata for a given domain.

| Parameter | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| `domain`  | `string` | The domain to get metadata for. |

**Returns:** `Promise<any>` - The domain metadata.

**Example:**

```
const metadata = await ZNSConnect.getMetadata('example.ink');
console.log(metadata);
```

#### `checkDomain`



Checks if a domain is already registered.

| Parameter | Type     | Description          |
| --------- | -------- | -------------------- |
| `domain`  | `string` | The domain to check. |

**Returns:** `Promise<boolean>` - `true` if the domain is registered, otherwise `false`.

**Example:**

```
const isRegistered = await ZNSConnect.checkDomain('example.ink');
console.log(isRegistered ? 'Registered' : 'Available');
```

#### `getPrice`



Gets the total price for registering a list of domains under a specific TLD.

| Parameter     | Type       | Description                                 |
| ------------- | ---------- | ------------------------------------------- |
| `domainArray` | `string[]` | The list of domains to check the price for. |
| `tld`         | `string`   | The top-level domain.                       |

**Returns:** `Promise<any>` - The total price.

**Example:**

```
const price = await ZNSConnect.getPrice(['example1', 'example2'], 'ink');
console.log(price);
```

#### `register`



Registers a list of domains under a specific TLD to specified owner addresses.

| Parameter        | Type           | Description                                  |
| ---------------- | -------------- | -------------------------------------------- |
| `walletClient`   | `WalletClient` | The wallet client instance.                  |
| `domainNames`    | `string[]`     | The list of domains to register.             |
| `ownerAddresses` | `string[]`     | The list of owner addresses for the domains. |
| `tld`            | `string`       | The top-level domain.                        |

**Returns:** `Promise<any>` - The registration result.

**Example:**

```
await ZNSConnect.register(
  walletClient,
  ['example1', 'example2'],
  ['0x123...', '0x456...'],
  'ink'
);
```

This documentation provides a comprehensive guide to using the ZNSConnect SDK for interacting with blockchain domains.

### The Web3 Name SDK ZNS Connect

The Web3 Name SDK is designed to simplify domain name resolution and reverse resolution. It supports various top-level domains (TLDs) such as .cz on BNB Chain, .scroll on Scroll Network, .blast on Blast Chain, and .poly on Polygon. For a full list of supported TLDs, visit [here](https://docs.znsconnect.io/developer-guide/contract-address).&#x20;

The SDK also supports verified domains launched through the ZNS ID Toolkit and dynamically integrates new TLDs as they are verified.



```
```

<details>

<summary></summary>



</details>

<br>
