# Ad Platforms

Defo Ads connects to major advertising platforms so you can manage all your campaigns from a single interface. The **Ad Platforms** page is a standalone view accessible from the sidebar under the **Platforms** section. This guide covers how to connect, manage, and troubleshoot your platform connections.

![Integrations Overview](../images/integrations-multi-platform.png)

## Supported Platforms

| Platform | Authentication | Networks |
|----------|---------------|----------|
| **Google Ads** | Google OAuth | Google Search, YouTube, Display Network, Shopping, Maps |
| **Microsoft Advertising** | Azure Entra ID (OAuth) | Bing, Yahoo, DuckDuckGo, AOL |

> **Note:** Microsoft Advertising integration is available on Premium plans.

---

## Connecting Google Ads

### Step 1: Initiate the Connection

1. Navigate to **Ad Platforms**.
2. Find the **Google Ads** card and click **Connect**.

### Step 2: Authorize with Google

1. A Google OAuth window will open.
2. Sign in with the Google account associated with your Google Ads account.
3. Review the requested permissions and click **Allow**.

### Step 3: Select Your Account

1. After authorization, Defo Ads will retrieve your available Google Ads accounts.
2. Select the account you want to connect from the dropdown list.
3. If you manage multiple accounts through a Manager (MCC) account, choose the specific sub-account you want to work with.
4. Click **Confirm** to complete the connection.

![Google Ads Connected](../images/integrations-google-card-connected.png)

---

## Connecting Microsoft Advertising

### Step 1: Initiate the Connection

1. Navigate to **Ad Platforms**.
2. Find the **Microsoft Advertising** card and click **Connect**.

### Step 2: Authorize with Azure Entra ID

1. A Microsoft OAuth window will open, powered by Azure Entra ID.
2. Sign in with the Microsoft account linked to your Microsoft Advertising account.
3. Review the requested permissions and click **Accept**.

### Step 3: Select Your Account

1. After authorization, Defo Ads will retrieve your available Microsoft Advertising accounts.
2. Select the account you want to connect.
3. Click **Confirm** to complete the connection.

### Microsoft Advertising Networks

When you connect Microsoft Advertising, your campaigns can reach users across multiple search networks:

- **Bing** — Microsoft's primary search engine
- **Yahoo** — Syndicated search results
- **DuckDuckGo** — Privacy-focused search engine
- **AOL** — Syndicated search results

![Microsoft Advertising Card](../images/integrations-microsoft-ads-card.png)

---

## Managing Connections

### Viewing Connection Status

Each connected platform displays a status indicator on the **Ad Platforms** page:

| Status | Indicator | Meaning |
|--------|-----------|---------|
| **Connected** | Green | The platform is connected and functioning normally |
| **Requires Attention** | Yellow | The connection needs re-authorization or has a minor issue |
| **Disconnected** | Gray | The platform is not connected |
| **Error** | Red | The connection has failed and needs troubleshooting |

### Disconnecting a Platform

1. Navigate to **Ad Platforms**.
2. Find the connected platform card.
3. Click the **Disconnect** button.
4. Confirm the disconnection in the dialog.

> **Important:** Disconnecting a platform does not delete any campaigns you have already imported. It only stops synchronization with that platform.

### Reconnecting a Platform

If your connection expires or encounters an error:

1. Navigate to **Ad Platforms**.
2. Click **Reconnect** on the affected platform card.
3. Complete the authorization flow again.
4. Your previous account selection will be restored if available.

![Disconnect Confirmation](../images/integrations-disconnect-confirm.png)

---

## Troubleshooting

### "Authorization Failed" Error

- Verify you are signing in with the correct account.
- Check that your ad platform account is active and in good standing.
- Clear your browser cookies and try again.
- For Google Ads, ensure third-party access is not blocked in your Google Account security settings.

### "Account Not Found" Error

- Confirm that the account you are trying to connect has active campaigns or is otherwise in good standing.
- For Google Ads Manager (MCC) accounts, make sure the sub-account you want to connect is not suspended.
- For Microsoft Advertising, verify your account has been fully set up in the Microsoft Advertising portal.

### Connection Drops Frequently

- OAuth tokens expire periodically. If your connection drops regularly, reconnect and ensure you grant all requested permissions.
- Check that your ad platform account has not been suspended or placed under review.
- Verify that no other third-party application has revoked Defo Ads' access.

### Platform-Specific Limitations

- **Google Ads:** Some account types (e.g., accounts under certain compliance reviews) may have restricted API access.
- **Microsoft Advertising:** Accounts must be fully verified with Microsoft before they can be connected.
