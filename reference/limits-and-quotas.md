[Home](../README.md) > [Reference](../README.md#reference) > Limits & Quotas

# Limits & Quotas

Defo Ads usage limits are determined by your subscription plan. Limits are **dynamic and configured per plan** -- they may vary based on your subscription tier and can change over time. This page explains how quotas work.

---

## Plan Limits

Limits are configured per plan and can be adjusted at any time by admins. The resources governed by plan limits include:

| Resource | Description |
|----------|-------------|
| **Campaigns** | Maximum active campaigns |
| **Daily AI tokens** | Daily allowance for AI text generation |
| **Daily image generations** | Daily AI-generated images |
| **Image upload size** | Maximum file size per upload |
| **Storage quota** | Total cloud storage allocation |
| **Platform accounts** | Google Ads / Microsoft Ads accounts |
| **Scheduler slots** | Number of automated sync schedules |

> **Note:** Exact limits vary by plan and can change. Check your [User Profile](../premium/user-profile.md) for your current plan details and usage.

---

## AI Token Limits

AI tokens are the unit of measurement for AI usage. Different actions consume different amounts of tokens:

| Action | Approximate Tokens |
|--------|-------------------|
| Generate a single headline | 50-100 |
| Generate a full ad (headlines + descriptions) | 200-500 |
| Generate a full campaign (ad groups + keywords + ads) | 2,000-10,000 |
| AI chat message | 100-500 |

These are estimates -- actual usage depends on the complexity of your request and the length of the AI response.

### Image Generation Limits

Plans include a daily limit on AI-generated images. This applies to image generation features within the app, not to uploading your own images.

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

### Campaign Limit on Lower Plans

If your plan has a campaign limit:

- You can create campaigns up to the limit
- To create more, you must delete an existing campaign or upgrade your plan
- The campaign count includes all campaigns regardless of status (enabled or paused)

### Unlimited Campaigns

Paid plans typically include unlimited campaigns. Check your plan details to confirm.

---

## Storage

- Data stored in cloud (Redis)
- Storage quota depends on your plan
- Data is backed up and accessible from any device
- Local cache may also be used for performance

---

## Tips for Managing Quotas

1. **Plan your AI usage.** Generating a full campaign at once is more token-efficient than generating components one by one.
2. **Edit manually when possible.** Small tweaks to headlines or descriptions do not require AI -- save your tokens for larger generation tasks.
3. **Monitor your usage.** Check the User Profile page to see how much of your daily quota remains before starting a large generation task.

---

**Related:**
- [Plans](../getting-started/plans.md) -- Plan details and features
- [Subscription & Billing](../premium/subscription.md) -- Plans, pricing, and upgrades
- [User Profile](../premium/user-profile.md) -- View your usage statistics
- [AI Features](../guides/ai-features.md) -- Understanding AI token consumption
