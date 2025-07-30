---
description: ZNS Registration Integration guide
cover: ../.gitbook/assets/Registration.png
coverY: 0
---

# ZNS Registration Integration

### Registration Process with WalletConnect

This guide outlines how to integrate the domain registration process with WalletConnect, enabling users to authenticate and register domains using their cryptocurrency wallets.

#### Steps Overview

1. Initialize the WalletConnect client.
2. Prompt the user to connect their wallet using a QR code modal.
3. Authenticate the user based on the wallet address.
4. Register domains under a specific TLD to the authenticated wallet addresses.
5. Confirm the registration and provide feedback to the user.

#### Prerequisites



Before starting, ensure you have installed the necessary WalletConnect packages:

```javascript
npm install @walletconnect/client @walletconnect/qrcode-modal
```

#### Initializing WalletConnect Client



Create a new file named `WalletConnectInit.js` and add the following code to initialize the WalletConnect client:

```javascript
import WalletConnect from "@walletconnect/client";
import QRCodeModal from "@walletconnect/qrcode-modal";

const walletConnectInit = () => {
    const connector = new WalletConnect({
        bridge: "https://bridge.walletconnect.org",
        qrcodeModal: QRCodeModal,
    });

    if (!connector.connected) {
        connector.createSession();
    }

    connector.on("connect", (error, payload) => {
        if (error) {
            throw error;
        }
        const { accounts } = payload.params[0];
        console.log(`Connected to ${accounts[0]}`);
    });

    return connector;
};

export default walletConnectInit;
```

#### Connecting to a Wallet



Invoke `walletConnectInit` from your application to establish a connection with the user's wallet. This step will prompt the user with a QR code modal to connect their wallet.

#### Handling Wallet Responses



Upon successful connection, the wallet address obtained from the `connect` event can be used for user authentication. This authenticated wallet address is crucial for the domain registration process.

#### Domain Registration



After authenticating the user, proceed with the domain registration process. The `register` function allows registering a list of domains under a specific TLD to the authenticated owner addresses.

**`register` Function**



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

#### Confirmation and Feedback



After the registration process is complete, provide the user with confirmation and any relevant details about their new domain(s). This could include transaction IDs, links to view the domain on a blockchain explorer, or next steps for setting up their domain.

#### Security Considerations



* Always validate wallet addresses on the server side.
* Implement rate limiting to prevent abuse.

#### Troubleshooting



* **QR Code Modal Does Not Appear**: Ensure the WalletConnect library is correctly installed and initialized.
* **Connection Fails**: Check the bridge server status and ensure your internet connection is stable.
