---
description: >-
  Interacts with blockchain domain names, resolving addresses, retrieving
  metadata
cover: ../.gitbook/assets/1990-480 web3.png
coverY: 0
---

# Web3 Name SDK ZNS Connect

### ZNS Connect SDK Overview

**Earn Revenue Sharing**

Integrate the ZNS Connect SDK into your third-party frontend and benefit from revenue sharing on all domain minting activities. Depending on your brand, name service platform, or integration, you can earn up to 30-40% of the revenue generated through the SDK.

**Key Functionalities**

The ZNS Connect SDK offers a robust set of functionalities to interact with blockchain domain names:

* **Resolve Addresses:** Fetch the blockchain address associated with a given domain.
* **Retrieve Metadata:** Access detailed information about a specific domain.
* **Check Domain Availability:** Determine whether a domain name is already registered or available.
* **Manage Domains:** Perform various operations such as registering new domains and resolving domain ownership.

Below is the detailed documentation for each function available in the SDK:

### Functions

#### `resolveAddress`

Resolves the blockchain address for a given top-level domain (TLD) and address.

| Parameter | Type     | Description                                             |
| --------- | -------- | ------------------------------------------------------- |
| `tld`     | `string` | The top-level domain (e.g., 'nft', 'xterio').           |
| `address` | `string` | The blockchain address to resolve (prefixed with `0x`). |

**Returns:** `Promise<any>` - The resolution result.

**Example:**

```javascript
const result = await ZNSConnectClass.resolveAddress('nft', '0x123...');
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
const owner = await ZNSConnectClass.resolveDomain('example.nft');
console.log(owner);
```

#### `getRegistry`

Gets the registry information for a given domain.

| Parameter | Type     | Description                 |
| --------- | -------- | --------------------------- |
| `domain`  | `string` | The domain to get info for. |

**Returns:** `Promise<any>` - The registry information.

**Example:**

```javascript
const registry = await ZNSConnectClass.getRegistry('example.nft');
console.log(registry);
```

#### `getMetadata`

Retrieves metadata for a given domain.

| Parameter | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| `domain`  | `string` | The domain to get metadata for. |

**Returns:** `Promise<any>` - The domain metadata.

**Example:**

```javascript
const metadata = await ZNSConnectClass.getMetadata('example.nft');
console.log(metadata);
```

#### `checkDomain`



Check if a domain is already registered.

| Parameter | Type     | Description          |
| --------- | -------- | -------------------- |
| `domain`  | `string` | The domain to check. |

**Returns:** `Promise<boolean>` - `true` if the domain is registered, otherwise `false`.

**Example:**

```javascript
const isRegistered = await ZNSConnectClass.checkDomain('example.nft');
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

```javascript
const price = await ZNSConnectClass.getPrice(['example1', 'example2'], 'nft');
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

```javascript
await ZNSConnectClass.register(walletClient, ['example1', 'example2'], ['0x123...', '0x456...'], 'nft');
```

### The Web3 Name SDK ZNS Connect

The Web3 Name SDK is designed to simplify domain name resolution and reverse resolution. It supports various top-level domains (TLDs) such as .cz on BNB Chain, .scroll on Scroll Network, .blast on Blast Chain, and .poly on Polygon. For a full list of supported TLDs, visit [here](https://docs.znsconnect.io/technical-documentation/contract-address).&#x20;

The SDK also supports verified domains launched through the ZNS ID Toolkit and dynamically integrates new TLDs as they are verified.

For more details and examples, visit the [ZNS Connect SDK Documentation](https://docs.znsconnect.io/technical-documentation/sdk).



```
```

<details>

<summary></summary>



</details>

\
