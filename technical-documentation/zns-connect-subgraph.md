---
description: ZNS Connect Subgraph on Blockscout Explorer
cover: ../.gitbook/assets/1990-480 Subgraph.png
coverY: 0
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# ZNS Connect Subgraph

Developing a subgraph for the ZNS protocol, which is based on ENS contracts, requires providing specific additional information.

The ZNS protocol has a constant variable called `identifier` that uniquely describes the protocol across multiple chains. This value is crucial for the calculation of the namehash, and therefore, the subgraph should be aware of it.

Blockscout now supports Name Services for various chains, including ZNS for **Polygon and Blast.** Users can search by name in the search bar or use the dedicated Name Services lookup page accessible from the Blockscout Explorer:&#x20;

[Polygon Blockscout Name Domains](https://polygon.blockscout.com/name-domains)

Blast Blockscout Name Domains

For more details, visit: [ZNS Subgraph on GitHub](https://github.com/blockscout/blockscout-rs/tree/main/blockscout-ens/graph-node/subgraphs/zns-subgraph)



<figure><img src="../.gitbook/assets/Screenshot 2024-06-12 at 10.05.43.png" alt=""><figcaption><p>ZNS Connect Subgraph on Blockscout Explorer menu</p></figcaption></figure>

