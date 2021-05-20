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
  </tbody>
</table>

To register a custom vault, just open your Account Settings and add it there.

![Custom vaults](../.gitbook/assets/image%20%2815%29.png)

![Adding a new custom vault](../.gitbook/assets/image%20%2816%29.png)

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
  </tbody>
</table>



