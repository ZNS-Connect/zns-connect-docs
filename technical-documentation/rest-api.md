---
description: All the endpoints return a JSON encoded object.
cover: ../.gitbook/assets/1990-480 API.png
coverY: 0
---

# Rest API

### Base URL: `https://v3.znsconnect.io/api`

## 1. Resolve Domain

Endpoint:

{% code title="GET" %}
```markup
/resolveDomain?tld=<CHAIN_TLD>&domain=<YOUR_DOMAIN>
```
{% endcode %}

Query Parameters:

<table><thead><tr><th width="132">Name</th><th width="139">Type</th><th>Description</th></tr></thead><tbody><tr><td>tld</td><td>String</td><td>tld of the domain</td></tr><tr><td>chain</td><td>String</td><td>Base part of domain without the tld</td></tr></tbody></table>

#### Request URL Example:

{% code title="GET" fullWidth="false" %}
```markup
v3.znsconnect.io/api/resolveDomain?tld=honey&domain=tonystark
```
{% endcode %}

Response:

```json
{
  "code": 200,
  "address": "0x9DaA27Ba25B1fa267Fe46D9C9F8b3676A5bc7D1c"
}
```

## 2. Resolve Address

Endpoint:

{% code title="GET" %}
```markup
/resolveAddress?tld=<CHAIN_TLD>&address=<YOUR_ADDRESS>
```
{% endcode %}

Query Parameters:

<table><thead><tr><th width="132">Name</th><th width="139">Type</th><th>Description</th></tr></thead><tbody><tr><td>tld</td><td>String</td><td>tld of the domain</td></tr><tr><td>address</td><td>String</td><td>Address to look for</td></tr></tbody></table>

#### Request URL Example:

{% code title="GET" %}
```markup
v3.znsconnect.io/api/resolveAddress?tld=honey&address=0x9DaA27Ba25B1fa267Fe46D9C9F8b3676A5bc7D1c
```
{% endcode %}

Response:

```json
{
  "code": 200,
  "primaryDomain": "tonystark",
  "userOwnedDomains": [
    "tonystark",
    "nickfury",
    "thorodinsson"
  ]
}
```

**Here is an example of partner** [**integration**](https://app.kiloex.io/trade?sCode=zns\&utm\_source=referral\&utm\_medium=zns)&#x20;

{% embed url="https://app.kiloex.io/" %}
KiloEx integration of ZNS API
{% endembed %}



<figure><img src="../.gitbook/assets/Screenshot 2024-06-19 at 08.59.08.png" alt=""><figcaption><p>KiloEx integration of ZNS Rest API</p></figcaption></figure>
