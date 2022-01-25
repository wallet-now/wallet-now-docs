# Swap as a service

Would you like to offer a built-in swap service which leverages our advanced multi-chain liquidity aggregator, and receive a commission of 0.3% from all swaps at the same time?

With WalletNow you can do that with just a couple lines of code on your website, or even with zero changes at all (with a custom referral link).

## Benefits for project owners

1. Receive fees in real time for any swap performed via your website or referral link
2. Offer a multi-chain liquidity aggregator to your users with minimal effort! Your users will swap tokens using the best available deal across 40+ liquidity sources (and more being added every week)!
3. Fully customizable! You choose which chains to display, the default slippage, and tokens to pre-select.
4. Zero maintenance. Once you integrate, we take care of maintaining and improving it constantly for you!

## Fees distribution

Fees are taken on every swap transaction following our regular [WalletNow Swap Terms Of Service](../features/swap/terms-of-service.md). **You receive 0.3% from all swaps (40% of the total fee taken).**

As mentioned in the terms of service above, WalletNow reserves the right to adjust the fees according to the market conditions, given the proper communication and advance notice.

## Integration via JS Library

With this integration option, you can embed our swap widget directly on your website.

WalletNow offers a JavaScript API to render the WalletNow swap widget into a DOM element on a hosting page. The widget will seamlessly integrate with your page and it won't require to set a specific height on the container element, it will automatically adjust its height as necessary. Also, customer feedback like dialog boxes will be adequately displayed based on page resolution.

### Step 1 - Add our swap library

Just add this code to your html head:

`<script src="https://walletnow.net/swap_bundle.js"></script>`

### Step 2 - Define the location of the widget on your page

Define an element that will be used as container for the swap widget, like this:

`<div id="swap_container"></div>`

### **Step 3 - Call our API to display the widget**

`WalletNow.renderSwap(domElement: Element, options: SwapOptions)`

Usage example:&#x20;

{% embed url="https://gist.github.com/wallet-now/d9aa1c0089fdfa3af76348b7a26cd86b" %}

**SwapOptions documentation:**

{% embed url="https://gist.github.com/wallet-now/8381fbf4657b8c8e60464a978769c6c8" %}

## Integration **via referral link**

If you don't want to add our widget you can still earn fees by linking to our swap with your referral code!

To create a custom link, all you need to do is add the "query string" parameters to the end of this URL: **`https://walletnow.net/swap/?`**

Each query string parameter is formatted like this: `<name>=<value>` and they are separated by an ampersand (`&`);

The following parameters are accepted:

* **referrer** - Your referrer wallet address (where you will receive the fees)
* **chain** - Chain number. If specified, the chain will be selected by default in the chain selector. If chain parameter is not specified, or the chain parameter is not a valid chain for swap, we will default to the first chain available.
* **inputToken** - Address of the input token. To select the native coin of the chain, use the address of the wrapped coin (WBNB, WETH, WFTM, WHT, etc).
* **outputToken** - Address of the output token. To select the native coin of the chain, use the address of the wrapped coin (WBNB, WETH, WFTM, WHT, etc).
* **slippage** - Slippage value as a decimal number. If not specified, it will default to 2 (2%).
* **fixedOutput** - Token symbol to be used as output. This is only allowed for our whitelisted tokens (the ones which show by default on the list). If specified, it will be selected as default output token even if the user switches to a different chain. If you would like to have your token whitelisted contact us at [contact@walletnow.net](mailto:contact@walletnow.net)
* **allowedChains\[]** - List of chain numbers that should be displayed in the chain selector. Add this parameter multiple times to list multiple values. If not specified, all the chains supporting WalletNow swap's contract will be displayed. Chains specified in this parameter must be supported by WalletNow, otherwise they will be ignored. If the resulting list after applying the filter is empty, all supported chains will be displayed.
* **embed** - Set this to **true** to make WalletNow display in embedded mode, which hides all advertisements.

