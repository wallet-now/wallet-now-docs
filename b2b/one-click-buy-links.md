# One-click buy links

**WalletNow Swap** allows you to create direct links to buy any token in a super-easy way, across multiple chains! You can control all aspects of the token directly on the URL. This is a great way to create "one-click buy buttons" for your token to put on your website, telegram, and everywhere else.

![](<../.gitbook/assets/image (81).png>)

For example, here is the link to buy BUSD on BSC:

[https://walletnow.net/swap/?outputToken=0xe9e7cea3dedca5984780bafc599bd69add087d56\&slippage=0.5\&chain=56\&allowedChains\[\]=56\&embed=true](https://walletnow.net/swap/?outputToken=0xe9e7cea3dedca5984780bafc599bd69add087d56\&slippage=0.5\&chain=56\&allowedChains\[]=56\&embed=true)

To create a custom link, all you need to do is add the "query string" parameters to the end of this URL: **`https://walletnow.net/swap/?`**

Each query string parameter is formatted like this: `<name>=<value>` and they are separated by an ampersand (`&`);

The following parameters are accepted:

* **chain** - Chain number. If specified, the chain will be selected by default in the chain selector. If chain parameter is not specified, or the chain parameter is not a valid chain for swap, we will default to the first chain available.
* **inputToken** - Address of the input token. To select the native coin of the chain, use the address of the wrapped coin (WBNB, WETH, WFTM, WHT, etc).
* **outputToken** - Address of the output token. To select the native coin of the chain, use the address of the wrapped coin (WBNB, WETH, WFTM, WHT, etc).
* **slippage** - Slippage value as a decimal number. If not specified, it will default to 2 (2%).
* **fixedOutput** - Token symbol to be used as output. This is only allowed for our whitelisted tokens (the ones which show by default on the list). If specified, it will be selected as default output token even if the user switches to a different chain. If you would like to have your token whitelisted contact us at [contact@walletnow.net](mailto:contact@walletnow.net)
* **allowedChains\[]** - List of chain numbers that should be displayed in the chain selector. Add this parameter multiple times to list multiple values. If not specified, all the chains supporting WalletNow swap's contract will be displayed. Chains specified in this parameter must be supported by WalletNow, otherwise they will be ignored. If the resulting list after applying the filter is empty, all supported chains will be displayed.
* **embed** - Set this to **true** to make WalletNow display in embedded mode, which hides all advertisements.

### Examples

1. Select Polygon by default\
   `chain=137`
2. Allow only Fantom and HECO and select HECO by default.\
   `chain=128&allowedChains[]=128&allowedChains[]=250`
3. Select HECO by default, set input token to HT with slippage of 3%\
   `chain=128&inputToken=0x5545153ccfca01fbd7dd11c0b23ba694d9509a6f&slippage=3`

### Benefits for token owners

1. **100% permission-less** - You don't need to be whitelisted in order to use this feature
2. **Token logo listings are free** - We detect automatically all logos listed on TrustWallet, but you can submit your token logo for free by opening a Pull-request here, in the same format expected by  Trust Wallet: [https://github.com/wallet-now/assets](https://github.com/wallet-now/assets)
3. **Automatically find the best deal to buy your token** - Our liquidity aggregator will find the best deal for your buyers, with zero effort.
