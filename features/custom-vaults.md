# Custom vaults

Isn't it frustrating when you want to make an investment in that brand new farm but your favorite portfolio monitoring solution does not support that protocol yet? You now have a dilemma: Make the investment and keep track of it offline (typically in a spreadsheet) or skip the investment just because you want to have a consolidated vision of your crypto.

With **WalletNow**, you don't need to worry about that! Just find your transaction on BSCScan, get the address of the vault, and register it as a **custom vault**! WalletNow will automatically attempt to extract the most possible data from that vault for you.

### Video Tutorial

{% embed url="https://www.youtube.com/watch?v=BaGImYiAoOE" %}

If the vault follows a standard ABI (Application Binary Interface) which is similar to PancakeSwap's "MasterChef" contract, we can extract additional information such as the exact balance you have, including any earnings. But, even if the vault uses a custom ABI, we can still report some basic information for it.

The following information is currently reported for custom vaults:

| Name            | Description                                                                                                                                                                                                                                                                                                   |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Deposits        | All token deposits                                                                                                                                                                                                                                                                                            |
| Withdraws       | All token withdraws                                                                                                                                                                                                                                                                                           |
| Balance         | <p>We will attempt to extract the exact balance from the vault contract.</p><p>If the vault contract is not supported, the balance will be reported as: "Deposits - Withdraws" <em>(notice that this may not reflect the reality if the vault gives yields in the same token as the deposited token)</em></p> |
| Harvests        | For tokens withdraws which are not the same as the deposit token                                                                                                                                                                                                                                              |
| Pending rewards | **ADVANCED: **Only available if you configure the optional settings for the "Reward token" and "Pending reward API"                                                                                                                                                                                           |

To register a custom vault, just open your Account Settings and add it there.



![](<../.gitbook/assets/image (46).png>)

![](<../.gitbook/assets/image (34).png>)

### Determining the configuration values

The most important information you need is the "Vault address", which is the address of the Smart Contract of that vault. To find that information, you can open your deposit transaction on BSCScan and copy the address of "**Interacted With (To)**":

![Finding the vault address](<../.gitbook/assets/image (22).png>)

You can also optionally set additional fields to help WalletNow extract more information from the vault. These are more advanced configurations, which you can skip if you only want the basic information.

The following sections describe the advanced configuration fields if you want to have more details:

#### **Reward token (address or API name)**

This setting defines what token the vault gives as a reward for your investment. On this field you can either set the "API name" from the vault which gives the token address, or you can set the token address directly (0x....).\
Each vault will have a different API to tell the reward token, so you need to figure out which it by examining the available APIs on BSCScan's "Read Contract". For example:

![Example API which returns the reward token address ("spcx")](<../.gitbook/assets/image (26).png>)

For the example above you would set the reward token to either "**spcx**" (with that exact case) or to "**0x79e6e581003d49929fd065ce8ea5d8794ca6b9d8**"

#### API Name for Pending Reward

This setting defines the name of the contract API responsible to indicate how much pending reward you have. Each vault will have a different API for that, so you need to figure out which it by examining the available APIs on BSCScan's "Read Contract". They are usually called "**pending**" or "**pendingXXX**" (where XXX is the reward token), but this is just a mere convention. For example:

![Example API which returns the pending rewards](<../.gitbook/assets/image (27).png>)

For the example above you would set the API name to "**pendingSPCX**" (with that exact case).

## Configuring using the Telegram bot

You can also configure custom vaults using the following commands:

| Command                                                  | Description                                                                                                                                                                                                                                                                         |
| -------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| /vault                                                   | List custom vaults                                                                                                                                                                                                                                                                  |
| /vault add **\<address> \<name>**                        | <p>Adds a custom vault</p><p><strong>&#x3C;address></strong>: Vault contract address on BSC</p><p><strong>&#x3C;name></strong>: Name of the vault (for your reference only)</p>                                                                                                     |
| /vault delete **\<number>**                              | <p>Removes a custom vault</p><p><strong>&#x3C;number></strong>: Vault number as listed by /vault</p>                                                                                                                                                                                |
| /vault set_reward **\<number> ** **\<reward_token>**     | <p>Sets the "reward token" of a custom vault</p><p><strong>&#x3C;number></strong>: Vault number as listed by /vault</p><p><strong>&#x3C;reward_token></strong>: Either the reward token address or the name of the API which retrieves the reward token from the vault contract</p> |
| /vault set_pending_api **\<number> ** **\<pending_api>** | <p>Sets the "pending reward" API name of a custom vault</p><p><strong>&#x3C;number></strong>: Vault number as listed by /vault</p><p><strong>&#x3C;pending_api></strong>: The name of the API which retrieves the pending reward from the vault contract</p>                        |

## Limitations

Custom vaults will try to extract as much information as possible from unknown contracts in a "best effort" way. There is no way to guarantee that it will work with any particular vault.

If you added a custom vault, and it is not showing up in your portfolio, it probably means that we failed to extract any useful information from it. You can send us the address of the vault and we will try to add support for it, but some vaults may not be technically viable.
