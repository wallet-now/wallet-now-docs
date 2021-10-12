# Active Monitoring

Your [Telegram Bot](telegram-bot.md) comes with another cool feature: Active Monitoring of all your tokens and notifications about your investments!

When you enable active monitoring, you will be automatically notified if there is any abnormal volatility in any of your investments (any tokens you are currently holding or are locked in an investment).

That's right! All your portfolio is automatically monitored out of the box. When you buy any new token, or invest on any new farm, pool, stake, etc, WalletNow will automatically detect it and start monitoring it — you don't need to move a finger for that.

Did you decide to stop investing in a given token and swapped it for other ones? No problem: Active Monitoring will automatically stop tracking the old token and start tracking all the new tokens you purchased.

```
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

To configure this feature, just open your Account Settings and select Telegram.

![](<../.gitbook/assets/image (33).png>)

You can configure the following settings for this feature:

| Setting        | Description                                                                                                                                                                                    |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Time window    | <p>Number of hours in the past that Wallet Now will look to check for price differences.<br>The default is 1 hour, which means that alerts are generated for price changes on that period.</p> |
| Price Increase | <p>Only notify about price increases higher than the given percentage<br>(E.g.: Alert if any price increases more than 6% in one hour)</p>                                                     |
| Price Drop     | <p>Only notify about price drops higher than the given percentage<br>(E.g.: Alert if any price drops more than 6% in one hour)</p>                                                             |

## Notifications about your investments

Some protocols may also include special notifications as part of our Active Monitoring. For example, RugZombie will notify once your NFTs have been crafted and are ready to be minted. Other protocols may notify you if they retire a pool where you are investing. Different protocols may have different types of notifications.

All you need to do to activate this feature is to ensure that you are on the "Diamond membership" ([see our plans](../pricing.md)). You also need to have Active Monitoring enabled, of course!

Each notification will be sent **only once** to your Telegram, but you can list all your notifications at any time using the **/notifications** command on the Telegram Bot.

## Configuring via Telegram commands

You can also configure this functionality using the following telegram commands:

| Commmand                            | Description                                                                                                                                                                                                                                                                                                                                            |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| /monitor enable                     | Enables active monitoring                                                                                                                                                                                                                                                                                                                              |
| /monitor disable                    | Disables active monitoring                                                                                                                                                                                                                                                                                                                             |
| /monitor increase **\<percentage>** | <p>Sets the <strong>Increase threshold</strong> to the given percentage</p><p>Example to set the threshold to 7%:</p><p><code>/monitor price increase 7%</code></p><p><em>(The '%' is optional, so the following also works):</em><br><code>/monitor price increase 7</code><br>You can also set this to 0 (zero) to disable Price Increase checks</p> |
| /monitor drop **\<percentage>**     | <p>Sets the <strong>Drop threshold</strong> to the given percentage</p><p>Example to set the threshold to 7%:</p><p><code>/monitor price drop 7%</code></p><p><em>(The '%' is optional, so the following also works):</em><br><code>/monitor price drop 7</code></p><p>You can also set this to 0 (zero) to disable Price Drop checks</p>              |
| /monitor hours **\<hours>**         | <p>Sets the <strong>Time window</strong> to the given number of hours</p><p>Example to set the time window to 2 hours:</p><p><code>/monitor hours 2</code></p>                                                                                                                                                                                         |

Example configuration session with the bot:

```
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
