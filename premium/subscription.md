[Home](../README.md) > [Premium](README.md) > Subscription & Billing

> **Premium Feature** — This feature requires a Defo Ads Premium subscription. [Compare plans](../getting-started/free-vs-premium.md)

# Subscription & Billing

Defo Ads Premium offers flexible subscription plans to match your needs. Plans are dynamically configured and managed by admins — the available tiers, prices, and limits may change. This guide covers choosing a plan, managing your subscription, and handling billing.

---

## Available Plans

Defo Ads offers multiple subscription tiers. Plans are **configured dynamically** by admins, so the exact offerings, prices, and limits may change. View the current plans in the app at any time.

### Free Trial

Every new account starts with a free trial that gives you access to premium features for a limited period. The trial activates automatically when you sign up — no credit card required.

- **Duration:** Configured per deployment
- **Full feature access:** All premium features with reduced quotas
- **No credit card:** Explore everything before committing

### Paid Plans

Paid plans scale by usage limits and feature access. Higher tiers typically include:

- Higher daily AI token and image generation limits
- More platform accounts (Google Ads, Microsoft Ads)
- Access to more capable AI models
- Team collaboration features
- More scheduler slots for automated syncs

The exact plans, prices, and features are displayed on the plan selection page in the app and may be updated at any time.

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
4. **Countdown visible** — Your trial expiration date is shown on the [User Profile](user-profile.md) page and in the **Plan Status Indicator** in the top navigation bar

### Plan Status Indicator

The top navigation bar displays your current plan status at all times:

- **Free Plan** — Gray icon with "Free Plan" label
- **Trial (7+ days remaining)** — Green indicator with days remaining
- **Trial (3-7 days)** — Amber/warning color
- **Trial (< 3 days)** — Red with pulsing dot animation and countdown
- **Trial Expired** — Red warning icon with "Trial Expired · Upgrade" link
- **Active Paid Plan** — Green indicator with plan name and renewal date

Click the plan status indicator at any time to navigate to the plan selection page.

<!-- TODO: Add screenshot of plan status indicator in nav bar -->

### During Your Trial

While the trial is active, you can:

- Connect Google Ads and Microsoft Advertising accounts and sync campaigns
- Use managed AI for ad copy generation
- Access the performance dashboard
- Try the AI assistant
- Upload assets to the library
- Invite team members

### When Your Trial Expires

After the trial period ends, your account enters **read-only mode**:

- **Your data is safe** — All campaigns, ad groups, ads, and keywords are preserved and visible
- **Read-only access** — You can view all your data but cannot create, edit, delete, or sync
- **AI features paused** — AI generation and chat are unavailable until you upgrade
- **Upgrade prompt** — A gate screen shows exactly what you've built and offers a direct path to upgrade
- **Persistent banner** — A reminder banner stays visible across all views

You will receive email notifications as your trial approaches expiry (3 days before, 1 day before, and on the day of expiry) so there are no surprises.

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

When your trial ends, your account enters read-only mode. You have two options:

### Option 1: Upgrade to a Paid Plan

The recommended path. Choose any paid plan to restore full access immediately. Your campaigns, ads, and keywords are exactly where you left them.

1. Click "Upgrade Now" from the gate screen or the persistent banner
2. Select a plan from the available options
3. Complete checkout via Stripe
4. Full access is restored instantly

See [Subscribing to a Plan](#subscribing-to-a-plan) above for details.

### Option 2: Stay in Read-Only Mode

You can continue to view all your data in read-only mode indefinitely. Your data is preserved — nothing is deleted. You can upgrade at any time to resume full access.

---

## Frequently Asked Questions

**Can I switch plans at any time?**
Yes. Upgrades take effect immediately. Downgrades take effect at the end of your current billing period.

**What happens to my data if I cancel?**
Your data is preserved in your account. If you resubscribe later, everything is still there.

**Do unused AI tokens roll over?**
No. Daily token and image generation limits reset every 24 hours.

**What happens when my trial expires?**
Your account enters read-only mode. All your data is preserved and visible — you just cannot create, edit, or sync until you upgrade.

**Is there a yearly billing option?**
This depends on the currently configured plans. Check the plan selection page for available billing cycles.

---

**Related:**
- [User Profile](user-profile.md) — View your subscription and usage
- [Free vs Premium Comparison](../getting-started/free-vs-premium.md) — Feature comparison
- [Premium Features Overview](README.md) — All premium features
