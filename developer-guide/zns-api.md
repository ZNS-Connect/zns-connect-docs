---
description: All the endpoints return a JSON encoded object.
cover: ../.gitbook/assets/API Integration.png
coverY: 0
---

# ZNS API

### Base URL: `https://zns.bio/api`

## 1. Resolve Domain

Endpoint:

{% code title="GET" %}
```markup
/resolveDomain?chain=<CHAIN_ID>&domain=<YOUR_DOMAIN>
```
{% endcode %}

Query Parameters:

<table><thead><tr><th width="132">Name</th><th width="139">Type</th><th>Description</th></tr></thead><tbody><tr><td>chain</td><td>Number</td><td>Chain id</td></tr><tr><td>domain</td><td>String</td><td>Domain to look for</td></tr></tbody></table>

#### Request URL Example:

{% code title="GET" fullWidth="false" %}
```markup
zns.bio/api/resolveDomain?chain=137&domain=haodev007
```
{% endcode %}

Response:

```json
{
  "code": 200,
  "address": "0x181EB6D5D3fD8FbACcb422237197826c6ac70232"
}
```

## 2. Resolve Address

Endpoint:

{% code title="GET" %}
```markup
/resolveAddress?chain=<CHAIN_TLD>&address=<YOUR_ADDRESS>
```
{% endcode %}

Query Parameters:

<table><thead><tr><th width="132">Name</th><th width="139">Type</th><th>Description</th></tr></thead><tbody><tr><td>chain</td><td>Number</td><td>Chain id</td></tr><tr><td>address</td><td>String</td><td>Address to look for</td></tr></tbody></table>

#### Request URL Example:

{% code title="GET" %}
```markup
zns.bio/api/resolveAddress?chain=137&address=0x181EB6D5D3fD8FbACcb422237197826c6ac70232
```
{% endcode %}

Response:

```json
{
  "code": 200,
  "primaryDomain": "cyberstorm",
  "userOwnedDomains": [
    "cyberstorm",
    "dontneedhelp",
    "enemymaycry",
    "residentevil"
  ]
}
```

**Here is an example of partner** [**integration**](https://app.kiloex.io/trade?sCode=zns\&utm_source=referral\&utm_medium=zns)&#x20;

## <mark style="color:orange;">**KiloEx Platform from Binance Labs**</mark>

{% embed url="https://app.kiloex.io/" %}
KiloEx integration of ZNS API
{% endembed %}



<figure><img src="../.gitbook/assets/Screenshot 2024-06-19 at 08.59.08.png" alt=""><figcaption><p>KiloEx integration of ZNS Rest API</p></figcaption></figure>

## <mark style="color:orange;">The Trailblazers platform from Taiko Team</mark>&#x20;

{% embed url="https://trailblazers.taiko.xyz/" %}
API integration of ZNS Taiko to Trailblazers portal
{% endembed %}



<figure><img src="../.gitbook/assets/Screenshot 2024-07-22 at 17.44.42.png" alt=""><figcaption><p>Link your wallet to the Trailblazers website to update your profile with your new domain names</p></figcaption></figure>
