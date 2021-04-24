# Telegram Bot

Our Telegram Bot \([@WalletNow\_Bot](https://t.me/WalletNow_Bot)\) provides a convenient way to quickly check summarized information of your investments, any time, anywhere! With our bot you can:

* Request a quick snapshot of all your wallets with summarized information
* Check the prices of all your tokens \(tokens you currently hold or have invested\)
* Configure most account settings, such as: Additional wallets, custom investments, preferred currency, and the Binance Exchange integration
* Receive proactive warnings about abnormal fluctuation in any any of your tokens \(tokens you currently hold or have invested\). Read more about this [**here**](active-monitoring.md).

## Linking your account

To link your Telegram account to your wallet:

1. Open your walled on Wallet Now.
2. Click on Account Settings and make sure your are logged in. You MUST login to connect your telegram account.
3. Click on "Link Telegram Bot" and copy the provided key
4. Go to Telegram and start a conversation with [@WalletNow\_Bot](https://t.me/WalletNow_Bot)
5. Send the following command: `/link <wallet> <key>`

**Example:**

```text
You:
/link 0x9f8ccdafcc39f3c7d6ebf637c9151673cbc36b88 2f54b02a4b23c456fda6

🤖 Wallet Now Bot:
Congratulations! Your account has been successfully linked 👏🏻👏🏻
```

## Snapshot

To take a quick snapshot of your investments, just send the command `/snapshot`

**Example:**

```text
You:
/snapshot

🤖 Wallet Now Bot:
Processing. Please wait...

Snapshot: 2021-04-24 22:45 UTC
Investment          | Total amount
------------------- | ------------
$AUTO               |       $21.08
$AUTOx              |       $28.18
$BNB                |       $26.68
$BNBx               |       $27.47
$BNB on Binance     |        $1.31
$BUSD on Binance    |        $0.01
$BTCB               |    $7,481.19
$BUNNY              |       $77.12
$BUSD               |    $5,771.08
$Cake               |       $46.88
$ETH                |    $4,410.83
$FAIR               |        $7.08
$UST                |       $19.20
$VAI                |    $6,148.10
$WATCH              |      $461.12
BUNNY Boost Vault   |      $412.74
Cake                |        $0.04
Moo Swampy SWAMP    |       $70.06
Student Coin (STC)  |    $6,353.00
USDT lending market |        $0.35
iBUSD               |   $23,392.93
iUSDT               |   $14,978.51
xBLZD Cave          |        $1.83
------------------- | ------------
Trezor 1            |   $57,328.01
Trezor 2            |   $11,947.68
Ledger 1            |      $461.13
Grand total         |   $69,736.82
```

## Prices

You can quickly check the prices of all your tokens with the `/prices` command:

```text
You:
/prices

🤖 Wallet Now Bot:
Processing. Please wait...

== Token Prices == 
 - AUTO: $2,147.99
 - BNB: $507.15
 - BTCB: $50,819.54
 - BUNNY: $356.25
 - BUSD: $1.00
 - Cake: $29.51
 - ETH: $2,267.08
 - FAIR: $0.00
 - SWAMP: $49.11
 - USDT: $1.00
 - UST: $1.00
 - VAI: $0.98
 - WATCH: $1.22
 - iBUSD: $1.01
 - iUSDT: $1.01
 - xBLZD: $10.40
```

## Other commands

There are many other commands in the bot which you can use to configure your preferences, manage extra wallets and register custom investments. Just send the `/start` command to see them all:

```text
You:
/start

🤖 Wallet Now Bot:
Hello. Welcome to Wallet Now! (https://walletnow.net)
The list of available commands are:
/start
/link
/snapshot
/prices
/currency
/locale
/monitor
/custom
/wallet
/binance
/unlink
/help

If you have not linked your account yet, you should start with:
/link
```

## Feature availability

| Free | Bronze | Silver | Gold |
| :--- | :--- | :--- | :--- |
| 🚫 | 🚫 | ✅ | ✅ |

