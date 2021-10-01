# Export data to CSV \(Excel\)

Exporting data to CSV allows you to open all your portfolio data in Excel or any other spreadsheet application.

![](../.gitbook/assets/image%20%2868%29.png)

To use this feature, it is very simple: Just click on the "three dots" right next to the plan details, and select "Export data to CSV \(Excel\)":

![](../.gitbook/assets/image%20%2870%29.png)

Just open the downloaded file on your favorite spreadsheet manager and start processing it! Oh, and it even works with the "Time Machine" so you can export data from the past as well.

The following columns are exported:

* **wallet**: The address of the wallet
* **chain**: Blockchain identification \(bsc, eth, poly, ftm, etc…\)
* **protocol**: Name of the protocol \(PCS, Wault, AutoFarm, etc…\)
* **investment**: Name of the investment as you see on WalletNow \(for example, the name of the pool where you invested\)
* **tokenAddress**: Address of the token
* **tokenSymbol**: Symbol of the token
* **type**: One of the following: hold, balance, deposited, withdrawn, pending, earned, harvested, debt, fee \(see below for the descriptions\)
* **quantity**: Quantity \(amount\) of tokens \(called "quantity" here to avoid confusion with the fiat amount\)
* **amountUSD**: Amount in US Dollars
* **amountLocalCurrency**: If your selected currency is different than USD, this will be the amount in your local currency

And the **types** are:

* **hold**: \(HODL\) This amount is simply being held by the user, on his wallet — not locked anywhere
* **balance**: Token balance on this investment
* **deposited**: Total amount deposited by the user \(depending on the pool, it may have interest/yield included\). If you did multiple deposits, they will all be summed.
* **withdrawn**: Total amount withdrawn by the user \(depending on the pool, it may have interest/yield included\). If you did multiple withdraws, they will all be summed.
* **pending**: Yield amount available for the user to harvest
* **earned**: Yield amount earned but that the user does not need to harvest \(for example when it is auto-compounded, or it was airdropped\)
* **harvested**: Yield amount already harvested by the user
* **debt**: This amount is owned by the user to a lending protocol
* **fee**: Total gas fee spent on this investment

This feature is exclusive to our **Diamond Tier** 💎. But if you are not yet a diamond member, you can test it by clicking on "**DEMO ACCOUNT**" in the landing page:

![](../.gitbook/assets/image%20%2869%29.png)



