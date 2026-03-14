[Home](../README.md) > [Reference](../README.md#reference) > Limits & Quotas

# Limits & Quotas

Defo Ads has different usage limits depending on whether you use the free open-source version or a Premium subscription. This page explains what those limits are and how they work.

---

## Free (Open Source) Version

The free version runs entirely in your browser with no backend server. Because there is no cloud service involved, most limits are determined by your browser and your own API key.

| Resource | Limit |
|----------|-------|
| **Campaigns** | Unlimited |
| **Ad groups per campaign** | Unlimited |
| **Ads per ad group** | Unlimited |
| **Keywords per ad group** | Unlimited |
| **AI usage** | Unlimited (you pay OpenAI directly) |
| **Storage** | Browser localStorage (typically 5-10 MB) |
| **Image uploads** | Not available |
| **Cloud sync** | Not available |
| **Google Ads connection** | Not available |

### Storage Considerations

The free version stores all data in your browser's localStorage. Typical limits:

- **Most browsers:** 5-10 MB of localStorage per domain
- **What fits in 5 MB:** Roughly 50-100 campaigns with full ad groups, ads, and keywords
- **When you run out:** The app will show an error when saving. Export your data to JSON to free up space or clear old campaigns.

> **Important:** Browser storage can be cleared by clearing your browser cache, using incognito mode, or switching browsers. Always keep a backup by [exporting your data](../guides/import-export.md) regularly.

### AI Usage (Free Version)

In the free version, AI requests go directly from your browser to OpenAI using your own API key. Your usage limits are determined by your OpenAI account:

- **Rate limits:** Set by OpenAI based on your account tier
- **Costs:** Billed directly to your OpenAI account
- **No daily cap from Defo Ads:** The app does not impose any additional limits

---

## Premium Version

Premium plans include cloud storage, managed AI, and additional features. Limits are **dynamic and configured per plan** -- they may vary based on your subscription tier and can change over time.

### Typical Plan Limits

The following table shows example limits. Your actual limits depend on your specific plan. Check your [User Profile](../premium/user-profile.md) for your current plan details.

| Resource | Free Trial (Example) | Pro Plan (Example) |
|----------|---------------------|-------------------|
| **Campaigns** | 3 | Unlimited |
| **Daily AI tokens** | 10,000 | 300,000 |
| **Daily image generations** | 5 | 50 |
| **Image upload size** | 5 MB per file | 5 MB per file |
| **Storage quota** | Per plan | Per plan |
| **Google Ads accounts** | 1 | Multiple |

> **Note:** These are examples only. Exact limits vary by plan and can be updated. Always check your plan details in the app for current limits.

### AI Token Limits

AI tokens are the unit of measurement for AI usage. Different actions consume different amounts of tokens:

| Action | Approximate Tokens |
|--------|-------------------|
| Generate a single headline | 50-100 |
| Generate a full ad (headlines + descriptions) | 200-500 |
| Generate a full campaign (ad groups + keywords + ads) | 2,000-10,000 |
| AI chat message | 100-500 |

These are estimates -- actual usage depends on the complexity of your request and the length of the AI response.

### Image Generation Limits

Premium plans include a daily limit on AI-generated images. This applies to image generation features within the app, not to uploading your own images.

---

## How Quotas Work

### Daily Reset

- Daily limits (AI tokens, image generations) **reset every 24 hours**
- The reset time is based on when your current usage period started
- A countdown to the next reset is shown in your [User Profile](../premium/user-profile.md)

### Checking Your Usage

You can check your current usage in two places:

#### User Profile Page

Navigate to your **User Profile** to see a usage summary:

- Current AI tokens used vs. daily limit
- Image generations used vs. daily limit
- Campaign count vs. plan limit
- Time until next daily reset

![Usage stats in User Profile](../images/ref-usage-stats-profile.png)

#### Response Headers

For technical users, API responses include usage information in HTTP headers. This is primarily useful for debugging or building integrations.

### When You Hit a Limit

When you reach a daily limit, the following happens:

1. **AI requests return a 429 error** -- "Rate limit exceeded" or "Quota exceeded"
2. **The app shows a notification** explaining which limit was reached
3. **You can still use non-AI features** -- editing, organizing, exporting, etc.
4. **Options to continue:**
   - Wait for the daily reset (countdown shown in Profile)
   - Upgrade to a higher plan for increased limits

![Quota exceeded notification](../images/ref-quota-exceeded.png)

---

## Campaign Limits

### Free Trial Campaign Limit

If your Premium plan has a campaign limit (e.g., 3 campaigns on a free trial):

- You can create campaigns up to the limit
- To create more, you must delete an existing campaign or upgrade your plan
- The campaign count includes all campaigns regardless of status (enabled or paused)

### Unlimited Campaigns

Paid Premium plans typically include unlimited campaigns. Check your plan details to confirm.

---

## Storage Limits

### Free Version

- All data in browser localStorage
- Typically 5-10 MB depending on browser
- No cloud backup -- data is only on your device
- Export to JSON regularly as a backup

### Premium Version

- Data stored in cloud (Redis)
- Storage quota depends on your plan
- Data is backed up and accessible from any device
- Local cache may also be used for performance

---

## Comparing Free vs. Premium Limits

| Feature | Free (Open Source) | Premium |
|---------|-------------------|---------|
| **Campaigns** | Unlimited | Per plan (often unlimited on paid plans) |
| **AI provider** | Your own OpenAI key | Managed (included in subscription) |
| **AI daily limit** | None from Defo Ads | Per plan |
| **Image uploads** | Not available | Per plan |
| **Storage** | Browser only (5-10 MB) | Cloud (per plan) |
| **Data backup** | Manual JSON export | Automatic cloud storage |
| **Google Ads sync** | Not available | Included |
| **Multi-device access** | No (browser-specific) | Yes |

For a full comparison of features, see [Free vs. Premium](../getting-started/free-vs-premium.md).

---

## Tips for Managing Quotas

1. **Plan your AI usage.** Generating a full campaign at once is more token-efficient than generating components one by one.
2. **Edit manually when possible.** Small tweaks to headlines or descriptions do not require AI -- save your tokens for larger generation tasks.
4. **Export regularly (free version).** Browser storage is volatile. A JSON export protects your work.
5. **Monitor your usage.** Check the User Profile page to see how much of your daily quota remains before starting a large generation task.

---

**Related:**
- [Free vs. Premium](../getting-started/free-vs-premium.md) -- Full feature comparison
- [Subscription & Billing](../premium/subscription.md) -- Plans, pricing, and upgrades
- [User Profile](../premium/user-profile.md) -- View your usage statistics
- [AI Features](../guides/ai-features.md) -- Understanding AI token consumption
- [Import & Export](../guides/import-export.md) -- Backup your data
