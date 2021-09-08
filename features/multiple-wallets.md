# Multiple Wallets

Would you like to split your investments across multiple wallets for extra security, but still monitor them all in a consolidated view? We too!

With WalletNow, you can register up to **15 wallets per account**, and see all of them in a consolidated view in both the website and the Telegram Bot! Gold members are limited to five wallets, while Diamond members can add up to fifteen!

To register additional wallets, open "Account Settings" and add them. You can also manage those using the [Telegram Bot](telegram-bot.md).

![Wallets configuration](../.gitbook/assets/image%20%2843%29.png)

![Wallet selection in the main screen](../.gitbook/assets/image%20%2848%29.png)

## Configuring via the Telegram bot

You can also configure your wallets via the Telegram bot using the following commands:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Commmand</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">/wallet add <b>&lt;address&gt;</b>  <b>&lt;alias&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Adds another wallet to your account</p>
        <p>&lt;address&gt; is the wallet address</p>
        <p>&lt;alias&gt; is an optional alias (short description)</p>
        <p></p>
        <p>Example:</p>
        <p><code>/wallet add 0x0... My secondary wallet</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">/wallet delete <b>&lt;number&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Removes an wallet from your account</p>
        <p>&lt;number&gt; is the wallet number as listed by <code>/wallet</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>

Example bot configuration session:

```text
🙍‍♂️ You:
/wallet

🤖 WalletNow Bot:
Your registered wallets are:
 - 1) 0x2ed2...9ce9 - Alias: Trezor 1

Valid commands are:
 - /wallet
 - /wallet add
 - /wallet delete

If you have any questions, check the documentation

🙍‍♂️ You:
/wallet add 0x4fd0e381c994b4173e4b452843b7b28c6a38acf6 Hot wallet MetaMask

🤖 WalletNow Bot:
Extra wallet registered with success

🙍‍♂️ You:
/wallet

🤖 WalletNow Bot:
Your registered wallets are:
 - 1) 0x2ed2...9ce9 - Alias: Trezor 1
 - 2) 0x4fd0...acf6 - Alias: Hot wallet MetaMask

Valid commands are:
 - /wallet
 - /wallet add
 - /wallet delete

If you have any questions, check the documentation

🙍‍♂️ You:
/wallet delete 2

🤖 WalletNow Bot:
Extra wallet unregistered with success
```

