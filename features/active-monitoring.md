# Active Monitoring

Your [Telegram Bot](telegram-bot.md) comes with another super-useful feature: Active Monitoring of all your tokens!

When you enable active monitoring, you will be automatically notified if there is any abnormal volatility in any of your investments \(any tokens you are currently holding or are locked in an investment\).

```text
🤖 WalletNow Bot:
WalletNow Active Monitoring
Relevant changes in the last hour:
Symbol | Change | Price now    
------ | ------ | -------------
BNB    | +7.3%  |    US$ 530,38
BTCB   | +6.9%  | US$ 52.151,66
------ | ------ | -------------
SWAMP  | -8.1%  |     US$ 53,18
```

You can configure the following settings for this feature:

| Setting | Description |
| :--- | :--- |
| Time window | Number of hours in the past that Wallet Now will look to check for price differences. The default is 1 hour, which means that alerts are generated for price changes on that period. |
| Drop threshold | Only notify about price drops higher than the given percentage \(E.g.: Alert if any price drops more than 6% in one hour\) |
| Increase threshold | Only notify about price increases higher than the given percentage \(E.g.: Alert if any price increases more than 6% in one hour\) |

## Configuring via Telegram commands

You can configure this functionality using the following telegram commands:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Commmand</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">/monitor enable</td>
      <td style="text-align:left">Enables active monitoring</td>
    </tr>
    <tr>
      <td style="text-align:left">/monitor disable</td>
      <td style="text-align:left">Disables active monitoring</td>
    </tr>
    <tr>
      <td style="text-align:left">/monitor increase <b>&lt;percentage&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Sets the <b>Increase threshold</b> to the given percentage</p>
        <p>Example to set the threshold to 7%:</p>
        <p><code>/monitor price increase 7</code>
        </p>
        <p>You can also set this to 0 (zero) to disable Price Increase checks</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">/monitor drop <b>&lt;percentage&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Sets the <b>Drop threshold</b> to the given percentage</p>
        <p>Example to set the threshold to 7%:</p>
        <p><code>/monitor price drop 7</code>
        </p>
        <p>You can also set this to 0 (zero) to disable Price Drop checks</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">/monitor hours <b>&lt;hours&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Sets the <b>Time window</b> to the given number of hours</p>
        <p>Example to set the time window to 2 hours:</p>
        <p><code>/monitor hours 2</code>
        </p>
      </td>
    </tr>
  </tbody>
</table>

Example configuration session with the bot:

```text
🙍‍♂️ You:
/monitor

🤖 WalletNow Bot:
Active monitoring is currently: DISABLED
 - Time window: 1 hour
 - Price drop alert: (disabled)
 - Price increase alert: (disabled)

Available commands:
 - /monitor enable 
 - /monitor disable
 - /monitor drop <percentage>
 - /monitor increase <percentage>
  Where <percentage> is either a percentage number or 0 (zero) to disable that alert
 - /monitor hours <hours>

If you have any questions, check the documentation

🙍‍♂️ You:
/monitor enable

🤖 WalletNow Bot:
Active monitoring ENABLED

🙍‍♂️ You:
/monitor increase 5

🤖 WalletNow Bot:
Price increase alert set to: 5%

🙍‍♂️ You:
/monitor drop 6%

🤖 WalletNow Bot:
Price drop alert set to: 6%

🙍‍♂️ You:
/monitor hours 2

🤖 WalletNow Bot:
Time window set to: 2 hours
```

