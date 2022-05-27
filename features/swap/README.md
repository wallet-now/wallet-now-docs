# WalletNow Swap

WalletNow has a builtin multi-chain liquidity aggregator to find the **best deal to swap your tokens**!

_**Safety is our top priority!** Our swap contracts perform several security checks to ensure that you will never receive less tokens than expected. This means you can safely swap using "untrusted" DEX routers to get you the best available deal._

When you use WalletNow Swap, you will interact exclusively with our custom-built liquidity aggregation router, which was designed with security as the top priority. You don't need to trust the underlying liquidity source because, even if it has any malicious code, WalletNow Swap will detect the diverging amounts and revert the transaction. This also increases the convenience since you only need to authorize WalletNow Swap for swapping your tokens instead of having to autorize individual distributed exchanges.

## Using WalletNow Swap

Head over to [https://walletnow.net/swap](https://walletnow.net/swap)

![](<../../.gitbook/assets/image (79) (1).png>)

Then select the tokens you want to swap, or paste a contract address to import:

![](<../../.gitbook/assets/image (81) (1) (1) (1).png>)

Once you click on "Review Swap", WalletNow will search several liquidity sources to find the best deal for your swap:

![](<../../.gitbook/assets/image (76).png>)![](<../../.gitbook/assets/image (80) (1) (1).png>)

The first time you swap a token, you may need to enable the token for swapping on WalletNow:

![](<../../.gitbook/assets/image (78) (1).png>)

Once you submit the swap transaction, you can choose to wait for the confirmation or continue the transaction in the background:

![](<../../.gitbook/assets/image (82) (1) (1).png>)

Once the transaction is confirmed, you have successfully swapped your tokens!

This feature is currently in BETA. Please report on our Telegram ([@WalletNow](https://t.me/WalletNow)) if you find any issues.

### Swapping directly from your WalletNow account

If you are using WalletNow and would like to swap tokens directly from the main interface, just click on any token that you want to swap and then click on the Swap button:

![](<../../.gitbook/assets/image (77).png>)

![Swap button on token dialog](<../../.gitbook/assets/image (81) (1) (1) (1) (1).png>)

This will open the token Swap dialog, where you can select the output token. It is that simple!

### Feature availability

WalletNow Swap is available on the following chains / networks:

| Chain               | Supported?  |
| ------------------- | ----------- |
| Binance Smart Chain | ✅ Yes       |
| Polygon             | ✅ Yes       |
| Fantom Opera        | ✅ Yes       |
| HECO                | ✅ Yes       |
| Ethereum            | Coming soon |
