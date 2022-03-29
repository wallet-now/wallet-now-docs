# Price Charts

WalletNow has a built-in multi-chain DEX price charts. This means you can see price charts for all tokens, as long as they have liquidity in any of our ever-growing list of supported Distributed Exchanges: [https://walletnow.net/chart/](https://walletnow.net/chart/)

![](<../.gitbook/assets/image (80).png>)

![](<../.gitbook/assets/image (81).png>)![](<../.gitbook/assets/image (82).png>)

Our price charts leverage the impressive "Trading View" charts for best-in-class chart analytics. All historical price data is indexed directly from the blockchain liquidity sources for maximum reliability.

Once you select a token, or enter its address manually, the price chart for the highest liquidity source will be displayed. You can also manually select other liquidity sources to view their charts.

![](<../.gitbook/assets/image (79).png>)

By default, all prices will be converted to USD (US Dollars), but you can also switch to view the price in the liquidity pair token.

![](<../.gitbook/assets/image (83).png>)

Once a given token is selected, the browser URL is updated so you can quickly share a link to that chart. For example, this is the link to the ETH price on the Ethereum network: [https://walletnow.net/chart/eth/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2](https://walletnow.net/chart/eth/0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2)

## Accessing from the WalletNow Interface <a href="#2f80" id="2f80"></a>

You can access WalletNow Charts by clicking on the "Candle Sticks" icon (in the top-right corner, or inside the menu for small screens):

![](https://miro.medium.com/max/564/1\*i44bD-oZxdXV-BFFxaHBkg.png)

You can also open the chart for a specific token by clicking on the "Candle Sticks" icon in the token information dialog:

![](https://miro.medium.com/max/680/1\*LwGsWT0c4Tv9nYTGqHFtIw.png)

## Background indexing <a href="#0d38" id="0d38"></a>

At the moment, WalletNow Charts works by indexing the blockchain data in a "lazy" manner. This means that the first time a token chart is accessed, you may see an indexing status like this:

![](https://miro.medium.com/max/1400/1\*vUqg\_Bmd6R6HR6pUpuH\_Pg.png)

Don't worry, this should happen only once per token, and shouldn't take long. Just come back later and the chart should be loaded normally.

If the demand increases, we may choose to migrate to a real-time active indexing in the future, which will eliminate that one-time load.

## Charting APIs <a href="#266a" id="266a"></a>

Are you a project owner and would like to include charting capabilities into your website? Let's have a chat about it: contact@walletnow.net

All the backend data for the charts have been developed by the awesome WalletNow team in a super-scalable way, and we may be able to help you with that!
