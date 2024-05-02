# Typescript SDK

## Installation

### Using NPM

{% hint style="warning" %}
NPM Package not published yet; Stay tuned.
{% endhint %}

### Pull using Git

```
npm install git+https://github.com/ZNS-Connect/sdk
```

### Usage

#### Creating a client

```ts
import { http } from 'viem';
import { createZnsPublicClient, Chain } from '@znsconnect/sdk';

const client = createZnsPublicClient({
  chain: Chain.PolygonMumbai,
  transport: http(),
});
```

#### Lookup a domain

```ts
const result = client.lookup({
  name: 'syed',
  tld: 'zeta',
});

console.log(result.owner); //= 0x137645BC5f1A8efB2BAB22FAb6829DF8f12847BA
```

#### Reverse Lookup a domain

```ts
const result = client.reverseLookup({
  address: '0x137645BC5f1A8efB2BAB22FAb6829DF8f12847BA',
  tld: 'zeta',
});

console.log(result.primaryDomain); //= { name: "syed', tokenId: 1 }
```
