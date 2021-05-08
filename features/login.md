# Login

To modify any settings on your account, you will need to **Login** using your wallet.

![](../.gitbook/assets/image%20%2811%29.png)

The login process is very simple: We will request a message signature which you need to accept with your wallet application. This message signature happens completely offline, so **there is no cost for that**.

Once the message is successfully signed, we will store that information on your browser and use it to sign all the requests. This will enable you to modify your settings.

We currently support the following wallet applications: **MetaMask**, **Trust Wallet, Math Wallet, SafePal and WalletConnect**. WalletConnect can be used to enable a large variety of other wallet applications and uses-cases.

![](../.gitbook/assets/image%20%2813%29.png)

If you wish to logout, you can do so in the same page:

![](../.gitbook/assets/image%20%2812%29.png)

You can also configure your account to be visible only when logged-in. Read more about it [**here**](privacy-lock.md).

### Security considerations

Signing messages with your wallet \(even offline messages\) has been used as an attack vector multiple times already, so it is important to understand WHAT is being signed.

WalletNow login messages are created using a combination of a server-side generated secret and the account address, and they look like this: `0uKt9xd7eor738EtFjTPI+oacQIPahMIBwoWQA+3j95=`

**Notice that the message will always end with an equals sign \(=\)**. This is a Base64-encoded message of a SHA256, and it will always have the exact length of 44 characters. Base64-encoded data cannot be used to perform any operations in the blockchain, so it is perfectly safe to sign this for the purposes of logins. 

**You should take extra care when signing messages which appear to be HEX-encoded** like this one: `bb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c` as they may expose you to security threats. The biggest problem with this is **WalletConnect**, since most wallet applications will display WalletConnect signature requests as HEX-encoded regardless of the message itself. On this situation, the only thing you can validate is the message length, as it **must be exactly 90 characters if it is coming from WalletNow \(0x followed by 88 characters\)**.

