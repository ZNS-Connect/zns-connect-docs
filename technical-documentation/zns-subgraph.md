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

# ➡️ ZNS Subgraph

Developing a subgraph for the ZNS protocol, which is based on ENS contracts, requires providing specific additional information.

The ZNS protocol has a constant variable called **`identifier`** that uniquely describes the protocol across multiple chains. This value is crucial for calculating the namehash, and therefore, the subgraph should be aware of it.

<div>

<figure><img src="../.gitbook/assets/Screenshot 2024-07-05 at 19.59.04.png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../.gitbook/assets/Screenshot 2024-07-05 at 19.58.42.png" alt=""><figcaption></figcaption></figure>

</div>

Blockscout and ZNS are excited to announce their collaboration, aimed at enhancing flexibility and features in name service implementations. This partnership leverages the strengths of both platforms to provide a seamless user experience for discovering and managing decentralized applications (DApps) and name services.

<figure><img src="../.gitbook/assets/Screenshot 2024-07-05 at 19.05.45.png" alt=""><figcaption><p>How's ZNS Connect Subgreah works</p></figcaption></figure>

Blockscout now supports Name Services for various chains, including ZNS for <mark style="color:purple;">**Polygon and Blast.**</mark> Users can search by name in the search bar or use the dedicated Name Services lookup page accessible from the Blockscout Explorer:&#x20;

* [**Polygon Blockscout Name Domains**](https://polygon.blockscout.com/name-domains)

<figure><img src="../.gitbook/assets/Screenshot 2024-06-12 at 10.05.43.png" alt=""><figcaption><p>ZNS Connect Subgraph on Blockscout Explorer menu Polygon</p></figcaption></figure>



* [**Blast Blockscout Name Domains**](https://blast.blockscout.com/name-domains)

<figure><img src="../.gitbook/assets/Screenshot 2024-07-05 at 19.05.31.png" alt=""><figcaption><p>ZNS Connect Subgraph on Blockscout Explorer menu on Blast</p></figcaption></figure>

#### For more technical details and to explore the ZNS Subgraph, visit: [<mark style="color:purple;">ZNS Subgraph on GitHub</mark>](https://github.com/blockscout/blockscout-rs/tree/main/blockscout-ens/graph-node/subgraphs/zns-subgraph)

#### Developing a Subgraph for ZNS

Creating a subgraph for the ZNS protocol, which is based on ENS contracts, involves providing specific additional information. The ZNS protocol includes a constant variable called "**identifier**" that uniquely describes the protocol across multiple chains.

#### Conclusion

The partnership between Blockscout and ZNS marks a significant step forward in enhancing the user experience for name service implementations. By integrating ZNS into Blockscout Explorer and developing a robust subgraph for the ZNS protocol, we are making it easier for users to navigate and utilize decentralized applications and services.

&#x20;[Stay tuned for more updates as we continue to innovate and improve the blockchain ecosystem.](#user-content-fn-1)[^1]





[^1]: 
