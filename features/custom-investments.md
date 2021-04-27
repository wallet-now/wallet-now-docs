# Custom Investments

Isn't it frustrating when you want to make an investment but your favorite aggregator does not support that protocol? You now have a dilema: Make the investment and keep track of it offline \(typically in a spreadsheet\) or skip the investment just because you want to have a consolidated vision of your crypto.

With **Wallet Now**, you don't need to worry about that! Just register a custom investment describing which token you are investing and how much of it, and Wallet Now will include that information consolidated in a single vision! Any BEP20 token is supported \(even LP Tokens\)!

If you make an investment which does not have a corresponding BEP20 token \(for example if that is on another chain\), you can always register your investment in USD to have some level of visibility about the external investment. Sometimes it is better to have a slightly outdated exchange rate and see that consolidated with all your other crypto than not having anything at all!

To register a custom investment, just open your Account Settings and add them there.

### Limitations

There are some important limitations with custom investments:

1. We don't know how much the investment is yielding \(or losing\), so the reported data is based exclusively on the amount of tokens invested and the current price of the token.
2. We support only BEP20 tokens \(all Binance Smart Chain tokens\). If there is no corresponding token in the BSC, you will need to register with a similar token or in Dollars.

## Configuring using the Telegram bot

You can also configure custom investments using the following commands:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Command</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">/custom add <b>&lt;token&gt; &lt;qty&gt; &lt;name&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Adds a custom investment</p>
        <p><b>&lt;token&gt;</b>: Token address on BSC</p>
        <p><b>&lt;qty&gt;</b>: Token amount</p>
        <p><b>&lt;name&gt;</b>: Name of the investment</p>
        <p></p>
        <p>You can also send &apos;USD&apos; and &apos;BNB&apos; as &lt;token&gt;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">/custom delete <b>&lt;number&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Removes a custom investment</p>
        <p><b>&lt;number&gt;</b>: Investment number as listed by /custom</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">/custom edit <b>&lt;number&gt; &lt;token&gt; &lt;qty&gt; &lt;name&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Edits a custom investment
          <br /><b>&lt;number&gt;</b>: Investment number as listed by /custom</p>
        <p><b>&lt;token&gt;</b>: Token address on BSC</p>
        <p><b>&lt;qty&gt;</b>: Token amount</p>
        <p><b>&lt;name&gt;</b>: Name of the investment</p>
      </td>
    </tr>
  </tbody>
</table>

Example configuration session with the bot:

```text
🙍‍♂️ You:
/custom

🤖 Wallet Now Bot:
You don't have any custom investments yet.

To add a custom investment, send the following command:
/custom add

If you have any questions, check the documentation

🙍‍♂️ You:
/custom add USD 100 $100 on STC

🤖 Wallet Now Bot:
Custom investment added with success

🙍‍♂️ You:
/custom

🤖 Wallet Now Bot:
Your custom investments are:

  1) $100 on STC: 100 USDT (0x55d398326f99059ff775485246999027b3197955)

Valid commands are:
 - /custom
 - /custom add
 - /custom delete
 - /custom edit

If you have any questions, check the documentation

🙍‍♂️ You:
/custom edit 1 BNB 10 Lots of money on STC

🤖 Wallet Now Bot:
Custom investment updated with success

🙍‍♂️ You:
/custom

🤖 Wallet Now Bot:
Your custom investments are:

  1) Lots of money on STC: 10 WBNB (0xbb4cdb9cbd36b01bd1cbaebf2de08d9173bc095c)

Valid commands are:
 - /custom
 - /custom add
 - /custom delete
 - /custom edit

If you have any questions, check the documentation
```

