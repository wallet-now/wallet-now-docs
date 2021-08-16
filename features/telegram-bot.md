# Telegram Bot

Our Telegram Bot \([@WalletNow\_Bot](https://t.me/WalletNow_Bot)\) provides a convenient way to quickly check summarized information of your investments, any time, anywhere!

With our bot you can:

* Request a quick snapshot of all your wallets with summarized information
* Check the prices of all your tokens \(tokens you currently hold or have invested\)
* Configure most account settings, such as: Additional wallets, custom investments, preferred currency, and the Binance Exchange integration
* Receive proactive warnings about abnormal fluctuation in any any of your tokens \(tokens you currently hold or have invested\). Read more about this [**here**](active-monitoring.md).

## Linking your account

To link your Telegram account to your wallet:

1. Open your wallet on WalletNow.net
2. Click on Account Settings and make sure your are logged in. You MUST login to connect your telegram account. \(See how to login on [this page](login.md)\)
3. Click on "Telegram", then on "Get Key" and copy the provided key
4. Go to Telegram and start a conversation with [@WalletNow\_Bot](https://t.me/WalletNow_Bot)
5. Send the following command: `/link <wallet> <key>`

![](../.gitbook/assets/image%20%2857%29.png)

**Example command on Telegram:**

```text
🙍‍♂️ You:
/link 0x9f8ccdafcc39f3c7d6ebf637c9151673cbc36b88 2f54b02a4b23c456fda6

🤖 WalletNow Bot:
Congratulations! Your account has been successfully linked 👏🏻👏🏻
```

## Snapshot

To take a quick snapshot of your investments, just send the command `/snapshot`

**Example:**

```text
🙍‍♂️ You:
/snapshot

🤖 WalletNow Bot:
Processing. Please wait...

Snapshot: 2021-04-26 02:04 UTC
Investment          | Total amount
------------------- | -------------
$BNB on Binance     |      US$ 1,38
BTCB Vault          |  US$ 7.696,77
BUNNY Boost Vault   |    US$ 450,19
BUNNY Staking       |    US$ 177,18
Cake                |      US$ 0,04
ETH Vault           |  US$ 4.786,39
iBUSD               | US$ 23.419,45
iUSDT               | US$ 14.994,40
Moo Swampy SWAMP    |     US$ 76,98
Student Coin (STC)  |  US$ 6.353,35
VAI-BUSD LP Staking | US$ 11.900,85
xBLZD Cave          |      US$ 1,77
------------------- | -------------
Wallet 1 (3 tokens) |     US$ 35,34
 $BNB               |     US$ 23,21
 $FAIR              |      US$ 7,09
 $VAI               |      US$ 5,03
Wallet 2 (2 tokens) |     US$ 56,09
 $AUTO              |     US$ 29,23
 $BNB               |     US$ 26,86
Wallet 3 (1 token)  |    US$ 520,34
 $WATCH             |    US$ 520,34
------------------- | -------------
Wallet 1            | US$ 57.410,92
Wallet 2            | US$ 12.539,25
Wallet 3            |    US$ 520,35
Grand total         | US$ 70.470,52
```

## Prices

You can quickly check the prices of all your tokens with the `/prices` command:

```text
🙍‍♂️ You:
/prices

🤖 WalletNow Bot:
Processing. Please wait...

Symbol | Price        
------ | -------------
AUTO   |  US$ 2.230,03
BNB    |    US$ 530,38
BTCB   | US$ 52.151,66
BUNNY  |    US$ 386,98
BUSD   |      US$ 1,00
Cake   |     US$ 32,86
ETH    |  US$ 2.459,13
FAIR   |      US$ 0,00
SWAMP  |     US$ 53,18
USDT   |      US$ 1,00
VAI    |      US$ 0,98
WATCH  |      US$ 1,37
WBNB   |    US$ 532,34
iBUSD  |      US$ 1,01
iUSDT  |      US$ 1,01
xBLZD  |      US$ 9,96
```

## Pending Yields

You can check all your pending yields with the `/pending` command:

```text
🙍‍♂️ You:
/pending

🤖 WalletNow Bot:
Processing. Please wait...

Pending Yields:
Investment          | Pending
------------------- | -------
BNB-BUSD LP Staking |  $14.78
  $BUNNY            |   $7.96
  $Cake             |   $6.82
VAI-BUSD LP Staking |  $14.58
  $BUNNY            |   $7.85
  $Cake             |   $6.72
iBUSD Staking       |  $11.35
  $AUTO             |  $11.35
BUNNY Boost Vault   |   $8.89
  $BUNNY            |   $8.89
iUSDT Staking       |   $6.69
  $AUTO             |   $6.69
BUNNY Staking       |   $6.15
  $BNB              |   $6.15
BTCB Vault          |   $6.13
  $BTCB             |   $2.83
  $BUNNY            |   $3.30
ETH Vault           |   $3.50
  $BUNNY            |   $1.89
  $ETH              |   $1.62
xBLZD Cave          |   $0.18
  $xBLZD            |   $0.18
MDX-BUSD LP Staking |   $0.14
  $MDX              |   $0.14
------------------- | -------
Trezor 1            |  $47.96
Trezor 2            |  $24.41
Total Pending       |  $72.38
```

This is a great way to quickly check if it is time to do those manual compounds, or if you should wait a bit more!

## Other commands

There are many other commands in the bot which you can use to configure your preferences, manage extra wallets and register custom investments. Just send the `/start` command to see them all:

```text
You:
/start

🤖 WalletNow Bot:
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



