[Home](../README.md) > [Premium](README.md) > Subscription & Billing

> **Premium Feature** — This feature requires a Defo Ads Premium subscription. [Compare plans](../getting-started/free-vs-premium.md)

# Subscription & Billing

Defo Ads Premium offers flexible subscription plans to match your needs. Plans are dynamically configured and may include options such as Free Trial, Pro, and Business tiers. This guide covers everything about choosing a plan, managing your subscription, and handling billing.

---

## Available Plans

Defo Ads offers multiple subscription tiers. Plans are configured dynamically, so the exact offerings may vary. Here is what a typical plan lineup looks like:

### Free Trial

Every new account starts with a free trial that gives you access to premium features for a limited period. The trial activates automatically when you sign up — no credit card required.

- **Duration:** Configured per deployment (typically 7-14 days)
- **AI tokens:** Limited daily allocation
- **Image generation:** Limited daily allocation
- **Campaigns:** Restricted campaign count
- **Purpose:** Explore all premium features before committing

### Pro Plan

The standard premium tier for individual advertisers and small businesses.

- **AI tokens:** Higher daily limit for text generation
- **Image generation:** More daily image generations
- **Campaigns:** Increased campaign limit
- **AI models:** Access to additional AI model options
- **Google Ads sync:** Full bidirectional sync capabilities

### Business Plan

For teams and agencies managing multiple accounts.

- **AI tokens:** Highest daily allocation
- **Image generation:** Maximum daily image limit
- **Campaigns:** Highest or unlimited campaign count
- **AI models:** Full selection of AI models
- **Team features:** Collaboration and shared workspaces
- **Priority support:** Faster response times

![Plan comparison](../images/subscription-plan-comparison.png)

---

## What Each Plan Includes

Every premium plan provides access to these core features, with limits that scale by tier:

### Daily AI Token Limit

Each plan includes a daily allowance of AI tokens for generating ad copy, headlines, descriptions, and chat interactions. The token counter resets every 24 hours. You can monitor your current usage on the [User Profile](user-profile.md) page.

### Daily Image Generation Limit

Plans include a daily quota for AI-generated images. This is used by Display and Performance Max campaigns that require visual assets. Unused image generations do not roll over to the next day.

### Campaign Limit

Each plan defines how many active campaigns you can manage simultaneously. Paused and completed campaigns may or may not count toward this limit depending on configuration.

### AI Model Selection

Higher-tier plans unlock access to more capable AI models. The available models may include options for speed-optimized generation, quality-optimized generation, or specialized advertising models.

![Plan features breakdown](../images/subscription-features-breakdown.png)

---

## Free Trial

### How It Works

1. **Automatic activation** — When you create a Defo Ads account, a free trial is activated immediately
2. **No credit card needed** — You can explore all premium features without entering payment information
3. **Full feature access** — The trial includes access to all premium features with reduced quotas
4. **Countdown visible** — Your trial expiration date is shown on the [User Profile](user-profile.md) page

### During Your Trial

While the trial is active, you can:

- Connect Google Ads accounts and sync campaigns
- Use managed AI for ad copy generation
- Access the performance dashboard
- Try the AI assistant
- Upload assets to the library
- Invite team members

### When Your Trial Expires

After the trial period ends:

- **Premium features pause** — Sync, managed AI, and analytics become unavailable
- **Your data is preserved** — Campaigns and settings remain in your account
- **Two paths forward:**
  1. **Subscribe to a plan** to restore full premium access
  2. **Use your own OpenAI API key** to continue with AI features in the free tier

![Trial expiration notice](../images/subscription-trial-expiring.png)

---

## Subscribing to a Plan

### Step-by-Step

1. **Navigate to plans** — Go to your User Profile or click any "Upgrade" prompt in the app
2. **Compare plans** — Review the available tiers and their included quotas
3. **Select a plan** — Click the "Subscribe" button on your chosen tier
4. **Stripe checkout** — You are redirected to a secure Stripe checkout page
5. **Enter payment details** — Provide your credit card information
6. **Confirm payment** — Complete the checkout process
7. **Instant activation** — Your subscription is active immediately upon successful payment

![Stripe checkout](../images/subscription-stripe-checkout.png)
<!-- TODO: Add screenshot of the Stripe checkout page -->

### After Subscribing

- Your plan name and tier appear on the User Profile page
- Daily quotas update to reflect your new plan
- All premium features become available
- A confirmation email is sent to your registered email address

---

## Managing Your Subscription

### Viewing Your Subscription

Your current subscription details are displayed on the [User Profile](user-profile.md) page:

- Plan name and tier
- Subscription status (active, trialing, canceled)
- Current period end date
- Daily usage statistics

### Upgrading Your Plan

To move to a higher tier:

1. Go to User Profile
2. Click "Manage Subscription" or "Upgrade"
3. Select the new plan
4. Confirm the change via Stripe
5. The upgrade takes effect immediately with prorated billing

### Downgrading Your Plan

To move to a lower tier:

1. Go to User Profile
2. Click "Manage Subscription"
3. Select the lower plan
4. The downgrade takes effect at the end of your current billing period

Note: If your current usage exceeds the lower plan's limits (for example, more campaigns than allowed), you may need to reduce usage before the downgrade activates.

### Canceling Your Subscription

1. Go to User Profile
2. Click "Manage Subscription"
3. Click "Cancel Subscription"
4. Confirm the cancellation
5. Your subscription remains active until the end of the current billing period
6. After cancellation, your account reverts to free-tier access

![Subscription management](../images/subscription-management-page.png)

---

## Billing

### How Billing Works

- **Payment processor:** All payments are handled securely by Stripe
- **Payment method:** Credit card (Visa, Mastercard, American Express, and other cards supported by Stripe)
- **Billing cycle:** Monthly or annual (depending on available plan configurations)
- **Receipts:** Sent via email after each payment

### Accessing Billing History

1. Go to User Profile
2. Click "Manage Subscription" — this opens the Stripe Customer Portal
3. View past invoices, update payment methods, and download receipts

### Failed Payments

If a payment fails:

- Stripe automatically retries the charge over several days
- You receive email notifications about the failed payment
- Your subscription remains active during the retry period
- If all retries fail, your subscription may be suspended

### Refunds

Refund policies are determined by the Defo Ads terms of service. Contact support for refund requests.

---

## After Your Trial Expires

If you choose not to subscribe after your trial ends, you still have options:

### Option 1: Subscribe to a Plan

The most straightforward path. Choose any plan to restore full premium access. See [Subscribing to a Plan](#subscribing-to-a-plan) above.

### Option 2: Use Your Own OpenAI API Key

You can continue using Defo Ads in free mode by providing your own OpenAI API key:

1. Go to Settings
2. Enter your OpenAI API key
3. AI features work directly against your OpenAI account
4. You pay OpenAI directly for usage

This option gives you AI-powered ad copy generation but does not include cloud sync, Google Ads integration, analytics, or team features.

### Option 3: Use Without AI

You can continue using Defo Ads as a manual campaign management tool without any AI features. Create and organize campaigns using the editor, and export them manually.

---

## Frequently Asked Questions

**Can I switch plans at any time?**
Yes. Upgrades take effect immediately. Downgrades take effect at the end of your current billing period.

**What happens to my data if I cancel?**
Your data is preserved in your account. If you resubscribe later, everything is still there.

**Do unused AI tokens roll over?**
No. Daily token and image generation limits reset every 24 hours.

**Can I use my own OpenAI API key with a premium subscription?**
Yes. You can choose between managed AI and your own API key regardless of your subscription tier.

**Is there a yearly billing option?**
This depends on the currently configured plans. Check the plan selection page for available billing cycles.

---

**Related:**
- [User Profile](user-profile.md) — View your subscription and usage
- [Free vs Premium Comparison](../getting-started/free-vs-premium.md) — Feature comparison
- [Premium Features Overview](README.md) — All premium features
