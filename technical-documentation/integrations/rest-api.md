---
description: All the endpoints accept and return a JSON encoded object.
---

# Rest API

### Base URL: `https://v2.znsconnect.io/api`

## 1. Lookup

Endpoint:

<pre><code><strong>/lookup
</strong></code></pre>

Body:

```json
{
    "name": "example", // base part of the domain, without TLD
    "chain": 80001, // Chain ID, currently only Polygon Mumbai
    "tld": "zeta" // either zeta or zero
}
```

Response:

```json
{
    "success": true,
    "address": "0x...",
    "domain": "example",
    "expiration": 0329209332 // UNIX timestamp
}
```

## 2. Reverse Lookup

Endpoint:

```
/reverse-lookup
```

Body:

```json
{
    "address": "0x...", // address to look for
    "chain": 80001, // Chain ID, currently only Polygon Mumbai
    "tld": "zeta" // either zeta or zero
}
```

Response:

```json
{
    "success": true,
    "address": "0x...",
    "domains": [
        {
            "name": "example",
            "tokenId": 1
        },
        {
            "name": "another",
            "tokenId": 2
        }
    ],
    "primaryDomain": {
        "name": "example",
        "tokenId": 1
    }
}
```
