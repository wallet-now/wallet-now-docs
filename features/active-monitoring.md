# Active Monitoring

Your [Telegram Bot](telegram-bot.md) comes with another super-useful feature: Active Monitoring of all your tokens!

When you enable active monitoring, you will be automatically notified if there is any abnormal volatility in any of your investments \(any tokens you are currently holding or are locked in an investment\).

```text
🤖 Wallet Now Bot:
== Active Monitoring ==
 - Good news: Detected a price increase of 6.0% for token BNB.
   The current price is $507.15
 - Detected a price drop of 9.2% for token SWAMP. The current price is $52.45
```

You can configure the following settings for this feature:

| Setting | Description |
| :--- | :--- |
| Time window | Number of hours in the past that Wallet Now will look to check for price differences. The default is 1 hour, which means that alerts are generated for price changes on that period. |
| Drop threshold | Only notify about price drops higher than the given percentage \(E.g.: Alert if any price drops more than 6% in one hour\) |
| Increase threshold | Only notify about price increases higher than the given percentage \(E.g.: Alert if any price increases more than 6% in one hour\) |



## Feature availability

| Free | Bronze | Silver | Gold |
| :--- | :--- | :--- | :--- |
| 🚫 | 🚫 | 🚫 | ✅ |

