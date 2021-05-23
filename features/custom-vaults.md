# Custom vaults

Isn't it frustrating when you want to make an investment in that brand new farm but your favorite portfolio monitoring solution does not support that protocol yet? You now have a dilemma: Make the investment and keep track of it offline \(typically in a spreadsheet\) or skip the investment just because you want to have a consolidated vision of your crypto.

With **WalletNow**, you don't need to worry about that! Just find your transaction on BSCScan, get the address of the vault, and register it as a **custom vault**! WalletNow will automatically attempt to extract the most possible data from that vault for you.

If the vault follows a standard ABI \(Application Binary Interface\) which is similar to PancakeSwap's "MasterChef" contract, we can extract additional information such as the exact balance you have, including any earnings. But, even if the vault uses a custom ABI, we can still report some basic information for it.

The following information is currently reported for custom vaults:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Deposits</td>
      <td style="text-align:left">All token deposits</td>
    </tr>
    <tr>
      <td style="text-align:left">Withdraws</td>
      <td style="text-align:left">All token withdraws</td>
    </tr>
    <tr>
      <td style="text-align:left">Balance</td>
      <td style="text-align:left">
        <p>We will attempt to extract the exact balance from the vault contract.</p>
        <p>If the vault contract is not supported, the balance will be reported as:
          &quot;Deposits - Withdraws&quot; <em>(notice that this may not reflect the reality if the vault gives yields in the same token as the deposited token)</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Harvests</td>
      <td style="text-align:left">For tokens withdraws which are not the same as the deposit token</td>
    </tr>
    <tr>
      <td style="text-align:left">Pending rewards</td>
      <td style="text-align:left"><b>ADVANCED: </b>Only available if you configure the optional settings
        for the &quot;Reward token&quot; and &quot;Pending reward API&quot;</td>
    </tr>
  </tbody>
</table>

To register a custom vault, just open your Account Settings and add it there.



![Custom vaults](../.gitbook/assets/image%20%2815%29.png)

![Adding a custom vault](../.gitbook/assets/image%20%2824%29.png)

### Determining the configuration values

The most important information you need is the "Vault address", which is the address of the Smart Contract of that vault. To find that information, you can open your deposit transaction on BSCScan and copy the address of "**Interacted With \(To\)**":

![Finding the vault address](../.gitbook/assets/image%20%2822%29.png)

You can also optionally set additional fields to help WalletNow extract more information from the vault. These are more advanced configurations, which you can skip if you only want the basic information.

The following sections describe the advanced configuration fields if you want to have more details:

#### **Reward token \(address or API name\)**

This setting defines what token the vault gives as a reward for your investment. On this field you can either set the "API name" from the vault which gives the token address, or you can set the token address directly \(0x....\).  
Each vault will have a different API to tell the reward token, so you need to figure out which it by examining the available APIs on BSCScan's "Read Contract". For example:

![Example API which returns the reward token address \(&quot;spcx&quot;\)](../.gitbook/assets/image%20%2826%29.png)

For the example above you would set the reward token to either "**spcx**" \(with that exact case\) or to "**0x79e6e581003d49929fd065ce8ea5d8794ca6b9d8**"

#### API Name for Pending Reward

This setting defines the name of the contract API responsible to indicate how much pending reward you have. Each vault will have a different API for that, so you need to figure out which it by examining the available APIs on BSCScan's "Read Contract". They are usually called "**pending**" or "**pendingXXX**" \(where XXX is the reward token\), but this is just a mere convention. For example:

![Example API which returns the pending rewards](../.gitbook/assets/image%20%2827%29.png)

For the example above you would set the API name to "**pendingSPCX**" \(with that exact case\).

## Configuring using the Telegram bot

You can also configure custom vaults using the following commands:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Command</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">/vault</td>
      <td style="text-align:left">List custom vaults</td>
    </tr>
    <tr>
      <td style="text-align:left">/vault add <b>&lt;address&gt; &lt;name&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Adds a custom vault</p>
        <p><b>&lt;address&gt;</b>: Vault contract address on BSC</p>
        <p><b>&lt;name&gt;</b>: Name of the vault (for your reference only)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">/vault delete <b>&lt;number&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Removes a custom vault</p>
        <p><b>&lt;number&gt;</b>: Vault number as listed by /vault</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">/vault set_reward <b>&lt;number&gt; </b>  <b>&lt;reward_token&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Sets the &quot;reward token&quot; of a custom vault</p>
        <p><b>&lt;number&gt;</b>: Vault number as listed by /vault</p>
        <p><b>&lt;reward_token&gt;</b>: Either the reward token address or the name
          of the API which retrieves the reward token from the vault contract</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">/vault set_pending_api <b>&lt;number&gt; </b>  <b>&lt;pending_api&gt;</b>
      </td>
      <td style="text-align:left">
        <p>Sets the &quot;pending reward&quot; API name of a custom vault</p>
        <p><b>&lt;number&gt;</b>: Vault number as listed by /vault</p>
        <p><b>&lt;pending_api&gt;</b>: The name of the API which retrieves the pending
          reward from the vault contract</p>
      </td>
    </tr>
  </tbody>
</table>

## Limitations

Custom vaults will try to extract as much information as possible from unknown contracts in a "best effort" way. There is no way to guarantee that it will work with any particular vault.

If you added a custom vault, and it is not showing up in your portfolio, it probably means that we failed to extract any useful information from it. You can send us the address of the vault and we will try to add support for it, but some vaults may not be technically viable.

