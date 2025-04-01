---
description: >-
  Yes — using ZNS domains to send assets is secure and simple. Here’s how
  resolution works:
---

# 🏫 Knowledge Base

How does ZNS resolve domain names to wallet addresses? Is it safe to send assets using a domain?

#### 🔗 Domain-to-Address Resolution Flow:

1. **Domain Registration**:\
   Users register a domain (e.g., `alice.defi`) on **ZNS Connect**, linking it to their wallet. This mapping is stored securely on-chain.
2. **Smart Contract Resolution**:\
   ZNS uses smart contracts to handle domain-to-address links. Everything is decentralized, permissionless, and tamper-proof.
3. **Lookup Request**:\
   When a user enters a ZNS domain (e.g., `nina.hvm`) in MetaMask or another integrated wallet, the Snap queries the blockchain for the linked address.
4. **Address Returned**:\
   The wallet retrieves and uses the correct address from the domain, enabling smooth and secure transactions — no more copying and pasting long addresses.

ZNS ensures a **trustless and decentralized resolution** process across supported EVM chains.

***

### Do I need to set a primary name for ZNS Snap to work?

No — setting a primary name is **not required** to use the ZNS Snap for **domain → address resolution**.

However, if you’d like to enable **reverse resolution** (resolving an address back to your domain for display in apps or profiles), setting a primary domain is recommended on each chain.

***

### What happens if my domain expires?

If your ZNS domain expires:

* It **will no longer resolve** to your wallet address.
* If someone else registers the domain later, it will resolve to **their address**, not yours.

ZNS provides a **grace period** (e.g., 90 days) after expiration, where the domain is **reserved for the original owner** to renew. After the grace period, the domain becomes available to the public again.

**Tip:** Always renew on time to keep your domain active and avoid misdirected transactions.

***

### How can I renew my ZNS domain?

You can renew anytime:

* **During the active registration period**
* Or within the **90-day grace period** after expiry

To renew:

1. Visit your domain’s page on [zns.bio](https://zns.bio/)
2. Click **“Extend”** or **“Renew”**
3. Confirm the transaction in your wallet

Quick, easy, and you're good to go! 🔄

***

### Does ZNS Snap work on non-EVM chains?

At the moment, ZNS Snap supports **EVM-compatible chains only**.\
We’re exploring future support for non-EVM ecosystems, but domains like `.sei` or `.inj` (if supported) are not yet resolvable within MetaMask Snap due to current technical limitations.

Stay tuned for future updates as ZNS expands cross-chain functionality 🌐
