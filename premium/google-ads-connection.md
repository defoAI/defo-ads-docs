[Home](../README.md) > [Premium](README.md) > Google Ads Connection

> **Premium Feature** — This feature requires a Defo Ads Premium subscription. [Compare plans](../getting-started/free-vs-premium.md)

# Google Ads Connection

Connect your Google Ads accounts to Defo Ads to import existing campaigns, export new ones, and track performance. This guide walks through the complete connection flow, account management, and troubleshooting.

---

## Prerequisites

Before connecting Google Ads to Defo Ads, make sure you have:

- **A Defo Ads Premium account** — Free trial or active subscription
- **A Google Ads account** — Either a standard advertiser account or a Manager (MCC) account
- **Google account access** — You must be able to sign in to the Google account associated with your Google Ads account

---

## Connecting Your Google Ads Account

### Step 1: Open the Ad Platforms Page

Click **Ad Platforms** in the sidebar (under the **Platforms** section). This page shows all available platform connections.

![Ad Platforms page](../images/google-ads-integrations-page.png)

### Step 2: Click Connect

Click the **Connect** button on the Google Ads card. This initiates the OAuth authorization flow.

### Step 3: Sign In to Google

A Google sign-in window appears. Select the Google account that is associated with your Google Ads account, or enter your credentials.

![Google sign-in](../images/google-ads-oauth-signin.png)
<!-- TODO: Add screenshot of the Google OAuth sign-in dialog -->

### Step 4: Authorize Defo Ads

Google displays the permissions that Defo Ads is requesting. These typically include:

- View your Google Ads accounts and campaigns
- Manage your Google Ads campaigns
- View performance reporting data

Review the permissions and click **Allow** to authorize Defo Ads.

### Step 5: Select Accounts

After authorization, Defo Ads retrieves the list of Google Ads accounts accessible with your credentials. If you have multiple accounts, you see a selection screen.

- **Standard accounts** are shown with their account name and ID
- **Manager (MCC) accounts** are shown with their sub-accounts

Select the accounts you want to connect and click **Confirm**.

![Account selection](../images/google-ads-account-selection.png)

### Step 6: Connection Complete

Once connected, the Ad Platforms page updates to show your connected account(s) with their details.

---

## Account Types

### Standard Accounts

A standard Google Ads account belongs to a single advertiser. When you connect a standard account, you see:

- Account name
- Account ID in the format `XXX-XXX-XXXX`
- A **Standard** type badge
- Campaign count (number of campaigns in that account)

### Manager (MCC) Accounts

A Manager account (also called My Client Center or MCC) manages multiple Google Ads accounts. When you connect a Manager account:

- The manager account itself is listed with a **Manager** type badge
- Sub-accounts under the manager are also accessible
- You can import from and export to any sub-account

![Account types](../images/google-ads-account-types.png)

---

## Multi-Account Support

Defo Ads supports connecting multiple Google Ads accounts simultaneously. This is useful if you:

- Manage ads for multiple businesses
- Have separate accounts for different brands or regions
- Use a Manager account alongside standalone accounts

### Connecting Additional Accounts

1. Go to **Ad Platforms** in the sidebar
2. Click **Connect Another Account** (or the connect button if adding a different Google account)
3. Complete the OAuth flow with the additional Google account
4. Select the accounts to add

### Switching Between Accounts

When performing syncs or viewing performance data, you can select which connected account to use. The account selector appears in:

- The Sync page (choose source/destination account)
- The Performance Dashboard (filter analytics by account)
- Campaign export (assign accounts to campaigns)

---

## Account Information

For each connected account, the Ad Platforms page displays:

| Field | Description |
|-------|-------------|
| **Account Name** | The name you set in Google Ads |
| **Account ID** | The unique identifier in `XXX-XXX-XXXX` format |
| **Type Badge** | Either "Manager" or "Standard" |
| **Campaign Count** | Number of campaigns found in the account |
| **Connection Status** | Connected, Expired, or Disconnected |
| **Last Synced** | Timestamp of the most recent sync operation |

![Connected account details](../images/google-ads-connected-account.png)

---

## Reconnecting

OAuth tokens have an expiration period. If your connection expires, you need to reconnect.

### Signs Your Connection Has Expired

- A warning banner appears on the Ad Platforms or Sync page
- The account status changes to "Expired" or "Requires Reconnection"
- Sync operations fail with an authentication error

### How to Reconnect

1. Go to **Ad Platforms** in the sidebar
2. Find the account with the expired connection
3. Click **Reconnect**
4. Complete the Google sign-in and authorization flow again
5. Your account is reconnected with a fresh token

Reconnecting preserves all your sync history and settings. You do not need to reconfigure anything.

![Reconnect prompt](../images/google-ads-reconnect-prompt.png)

---

## Disconnecting

To remove a Google Ads connection from Defo Ads:

1. Go to **Ad Platforms** in the sidebar
2. Find the account you want to disconnect
3. Click **Disconnect** (or the menu icon and select "Disconnect")
4. Confirm the disconnection in the dialog

### What Happens When You Disconnect

- The OAuth tokens are removed from Defo Ads
- Sync operations are no longer available for that account
- Previously imported campaigns remain in Defo Ads (they are not deleted)
- Performance data already fetched is preserved
- You can reconnect the same account at any time

---

## Troubleshooting

### "Access Denied" During OAuth

**Cause:** Your Google account does not have access to any Google Ads accounts.

**Solution:**
- Verify you are signing in with the correct Google account
- Check that your Google account has access to at least one Google Ads account
- If using a Manager account, ensure your Google account has admin access

### "Pop-up Blocked" Error

**Cause:** Your browser is blocking the Google sign-in popup window.

**Solution:**
- Allow pop-ups for the Defo Ads domain in your browser settings
- Try clicking the Connect button again after allowing pop-ups
- Disable any browser extensions that might block pop-ups

### No Accounts Appear After Authorization

**Cause:** The authorized Google account does not have any Google Ads accounts, or the accounts are suspended.

**Solution:**
- Sign in to [ads.google.com](https://ads.google.com) directly to verify your accounts are active
- If you recently created a Google Ads account, wait a few minutes and try again
- Try disconnecting and reconnecting with the correct Google account

### "Token Expired" Error During Sync

**Cause:** Your OAuth token has expired since you last connected.

**Solution:**
- Go to the Ad Platforms page and click **Reconnect** on the affected account
- Complete the sign-in flow to refresh the token

### Connection Works but No Campaigns Found

**Cause:** The connected account may have zero campaigns, or they may be in a state that is not importable.

**Solution:**
- Verify campaigns exist in your Google Ads account by checking [ads.google.com](https://ads.google.com)
- Ensure the campaigns are not in a "Removed" state
- Try refreshing the Sync page

### "Third-Party App Access" Blocked

**Cause:** Your Google Workspace admin has restricted third-party app access.

**Solution:**
- Contact your Google Workspace administrator to allow Defo Ads
- Alternatively, use a personal Google account that is linked to your Google Ads account

---

**Related:**
- [Ad Platforms](integrations.md) — Manage all platform connections
- [Bidirectional Sync](sync.md) — Import and export campaigns
- [Quick Sync](quick-sync.md) — One-click sync for returning users
- [Troubleshooting](../troubleshooting/) — More troubleshooting guides
