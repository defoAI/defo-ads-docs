[Home](../README.md) > [Premium](README.md) > Conversions

> See [Plans](../getting-started/plans.md) for feature details.

# Conversions

Track and manage conversion actions across your connected advertising platforms. The **Conversions** page lets you create conversion actions, export them to your ad platforms, assign them to campaigns, and get tracking code snippets for your website.

---

## Accessing Conversions

Click **Conversions** in the sidebar (under the **Platforms** section). This opens the Conversions management page.

<!-- TODO: Replace with updated screenshot -->
![Conversions page](../images/conversions-overview.png)

---

## What Are Conversion Actions?

Conversion actions track valuable activities that users take after clicking your ads, such as:

- **Purchases** — Completed transactions on your website
- **Sign-ups** — Newsletter subscriptions or account registrations
- **Phone calls** — Calls made from your ads or from your website
- **Form submissions** — Contact forms, quote requests, etc.
- **Page views** — Visits to specific pages (e.g., a "Thank You" page)
- **Offline conversions** — Conversions tracked outside your website (e.g., in-store purchases linked to ad clicks)

Tracking conversions helps you understand which campaigns, ads, and keywords drive the most valuable results.

---

## Conversions Page Overview

### Summary Statistics

At the top of the page, summary cards display:

- **Total** — All conversion actions configured
- **Active** — Conversion actions with Active status
- **Assigned** — Actions assigned to at least one campaign
- **Unassigned** — Actions not yet linked to any campaign

### Conversions Table

| Column | Description |
|--------|-------------|
| **Name** | The conversion action name |
| **Type** | User-friendly label: Website Action, Phone Call (ad), Phone Call (website), Offline (click), Offline (call) |
| **Category** | Conversion category (e.g., Purchase, Lead, Sign-up, Page View) |
| **Status** | Active (green chip) or Paused |
| **Synced to** | Platform icons showing where this action has been exported |
| **Campaigns** | Count of campaigns this action is assigned to (clickable) |

### Filtering

- **Status filter** — Show All, Active, or Paused conversion actions

### Row Actions

For each conversion action, you can:

- **Export to Platform** — Push the action to a connected ad platform
- **Assign to Campaign** — Link the action to one or more campaigns
- **Get Tracking Code** — View installation instructions for your website
- **Pause/Resume** — Toggle the conversion action status
- **Delete** — Remove the conversion action

---

## Creating a Conversion Action

Click **"New"** at the top of the page to launch the conversion action wizard. The wizard guides you through 5 steps:

### Step 1: Select Your Goal

Choose from 5 goal categories:

| Goal | Description |
|------|-------------|
| **Sales & Revenue** | Track purchases, transactions, and revenue |
| **Leads & Sign-ups** | Track form submissions, sign-ups, and contact requests |
| **Phone Calls** | Track calls from ads or from your website |
| **Engagement** | Track page views, visit duration, and pages per visit |
| **Offline Conversions** | Track click-based or call-based offline conversions |

### Step 2: Select Sub-Type (if applicable)

For goals with multiple tracking methods, choose the specific type:

- **Phone Calls** → "Calls from ads" or "Calls from website"
- **Offline Conversions** → "Offline (click-based)" or "Offline (call-based)"

### Step 3: Name Your Conversion

Enter a descriptive name for the conversion action (e.g., "Purchase", "Newsletter Signup", "Contact Form Submit").

### Step 4: Choose Category

Select from standard conversion categories:

- PURCHASE, ADD_TO_CART, BEGIN_CHECKOUT, SUBSCRIBE_PAID
- SUBMIT_LEAD_FORM, SIGNUP, CONTACT, BOOK_APPOINTMENT, REQUEST_QUOTE
- GET_DIRECTIONS, PAGE_VIEW, DOWNLOAD, PHONE_CALL_LEAD
- ENGAGEMENT, DEFAULT

### Step 5: Counting & Value

Configure how conversions are counted and valued:

**Counting Type:**
- **One per click** — Counts only one conversion per ad click (best for leads and sign-ups)
- **Every** — Counts every conversion per ad click (best for sales and transactions)

**Value Settings:**
- **No value** — Don't assign a monetary value
- **Fixed value** — Set a fixed amount per conversion (e.g., $50 per purchase)
- **Variable value** — User specifies the value on each conversion, with a default fallback

Click **"Create"** to save the conversion action.

> **Note:** You can create conversion actions even without any platform connected. They are stored locally and can be exported to platforms later.

---

## Exporting Conversions to Platforms

To push your conversion actions to a connected ad platform:

1. Click the **Export** action on a conversion row (or use the bulk export button).
2. Select the target platform from the dropdown (with platform icons).
3. Choose the account (auto-selected if only one).
4. The export shows which actions will be **Created** (new) vs **Updated** (already linked).
5. Confirm to start the export.
6. Real-time feedback shows success/error counts.

Conversion actions can also be exported as part of a regular [Sync](sync.md) operation.

---

## Assigning Conversions to Campaigns

Link conversion actions to specific campaigns to track which campaigns drive conversions:

1. Click the **Assign** action on a conversion row.
2. A dialog shows checkboxes for all available campaigns.
3. Check the campaigns you want to link.
4. Optionally select a **primary** conversion action (radio button) — the main conversion the campaign optimizes for.
5. Click **Save**.

The **Campaigns** column in the table shows the count of linked campaigns.

---

## Tracking Code Installation

After creating a conversion action, you need to install tracking code on your website. Click the **code icon** on any conversion row to open the Tracking Code dialog.

### Google Ads Conversions

The dialog shows two code snippets to copy:

1. **Global Site Tag** — Add to the `<head>` section of every page on your website
2. **Event Snippet** — Add to the page where the conversion happens (e.g., your order confirmation page)

> **Tip:** Using Google Tag Manager? You can add the conversion tag there instead of editing your website code directly.

### Microsoft Advertising Conversions

For Microsoft Ads, the dialog shows a message explaining that your **UET tag** handles tracking. Make sure the UET tag is installed on your website.

### Phone Call Conversions (from ads)

Calls from ad extensions are tracked automatically. No code installation is required.

### Offline Conversions

The dialog explains how to capture the **Google Click ID (GCLID)** when users click your ad, then upload conversions later via the platform's offline conversion tools.

---

## Platform-Specific Wizard Fields

When creating conversion actions, some fields are specific to the target platform:

### Google Ads

- Standard conversion action fields
- Global Site Tag + Event Snippet for tracking code

### Microsoft Advertising

- UET tag-based tracking
- Microsoft-specific category mappings
- Numeric ID format for API compatibility

---

## Empty States

- **No platforms connected** — A prompt to connect a platform first. Click the link to go to the [Connections](integrations.md) page.
- **No conversion actions** — Click **"New"** to set up your first conversion action.

---

**Related:**
- [Connections](integrations.md) — Connect and manage advertising platforms
- [Sync](sync.md) — Synchronize campaigns and conversions with connected platforms
- [Performance Dashboard](performance-dashboard.md) — View conversion metrics in analytics
