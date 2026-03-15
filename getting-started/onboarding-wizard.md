[Home](../README.md) > [Getting Started](../README.md#getting-started) > Onboarding Wizard

# Onboarding Wizard

When you first visit Defo Ads Premium, the onboarding wizard guides you through setting up your account in 6 steps. The wizard adapts based on whether you're a new user or returning to set up a new device.

A progress bar and step counter at the top show your current position (e.g., "Step 3 of 6").

---

## Step 1: Welcome

<!-- TODO: Add screenshot of welcome step -->

**What you see:**
- Defo Ads logo
- Heading: "Welcome to DefoAds"
- Subtitle: "Manage your ad campaigns with AI power"
- Language selector with three options: **English (EN)**, **Deutsch (DE)**, **Français (FR)**
- Three value propositions:
  - AI-powered campaign creation
  - Multi-platform ad management
  - Real-time performance insights
- **"Get Started"** button

**What to do:**
1. (Optional) Select your preferred language
2. Click **"Get Started"**

---

## Step 2: Account

<!-- TODO: Add screenshot of auth step -->

### New Users

**What you see:**
- Heading: "Create Your Free Account"
- Terms & Conditions checkbox with links to Terms and Privacy Policy
- Cloudflare Turnstile security verification (usually invisible)
- **"Continue with Google"** button
- Trust signals: "Your data is private and secure" and "No password needed with Google"

**What to do:**
1. Check the Terms & Conditions checkbox
2. Click **"Continue with Google"**
3. Complete the Google Sign-In popup
4. You're automatically advanced to the next step

### Returning Users

If you're already signed in (e.g., on a new device):

**What you see:**
- Success icon and "Welcome back!" message
- Your email address displayed
- Terms & Conditions checkbox (re-acceptance required)
- **"Accept & Continue"** button

**What to do:**
1. Check the Terms & Conditions checkbox
2. Click **"Accept & Continue"**

---

## Step 3: About You (Optional)

<!-- TODO: Add screenshot of organisation step -->

**What you see:**
- Heading: "Help us tailor your experience"
- Organization name input (e.g., "Acme Corp")
- Purpose selection chips (multi-select):
  - "Manage Google Ads campaigns"
  - "Manage Microsoft Ads campaigns"
  - "AI-powered ad creation"
  - "Multi-platform campaign management"
  - "Other"
- **"Skip"** link and **"Continue"** button

**What to do:**
1. (Optional) Enter your organization name
2. (Optional) Select one or more purpose tags — selected chips are highlighted in blue
3. Click **"Continue"** (or **"Skip"** to leave both blank)

This information helps personalize your experience and is saved to your profile.

---

## Step 4: Choose a Plan

<!-- TODO: Add screenshot of plan selection step -->

**What you see:**
- Up to 4 plan cards in a responsive grid:

**Free/Trial Plans:**
- Title and price (Free)
- Trial badge (e.g., "14 Day Trial")
- Features: daily token limits, image limits, campaign limit, cloud sync
- Button: **"Claim Free"** or **"Start Trial"** — claims the plan instantly

**Paid Plans (Pro, Business):**
- Title and monthly/annual price
- "Recommended" badge on highest-value plan
- Premium styling with gradient background
- Expandable feature list ("See All Features")
- Button: **"Select Plan"** — redirects to Stripe checkout

**What to do:**
1. Review the plan cards
2. Click the button on your chosen plan:
   - **Free/Trial:** Claimed immediately (requires Turnstile verification)
   - **Paid:** Redirects to Stripe for payment, then returns to the wizard
3. After plan selection, you're advanced to the next step

> **Note:** You can always change your plan later from the [Subscription](../premium/subscription.md) page.

---

## Step 5: Connect Platforms (Optional)

<!-- TODO: Add screenshot of platforms step -->

**What you see:**
- Heading: "Connect your ad platforms"
- Subtitle: "You can always do this later from Settings"
- Two platform cards:

**Google Ads:**
- Platform icon and description
- **"Connect"** button (or **"Connected"** badge with green checkmark if already linked)

**Microsoft Advertising:**
- Platform icon and description
- **"Connect"** button (or locked if plan doesn't support it)

- Footer: "You can always connect platforms later from Settings"
- **"Skip for now"** link and **"Continue"** button

**What to do:**
1. (Optional) Click **"Connect"** on any platform to start the OAuth flow
2. Complete the authorization popup for each platform
3. Click **"Continue"** (or **"Skip for now"**)

> **Tip:** Don't worry if you're not ready to connect. You can do this anytime from the [Connections](../premium/integrations.md) page.

---

## Step 6: You're All Set!

<!-- TODO: Add screenshot of completion step -->

**What you see:**
- Celebration heading: "You're all set!"
- Subtitle: "Your account is ready. Here's what we set up for you."
- **Setup summary checklist:**
  - ✅ Account created
  - ✅ [Plan name] activated (with trial end date if applicable)
  - ✅ or ⭕ Platform(s) connected (count or "No platforms connected yet")
- **Quick-start suggestions:**
  - "Create your first campaign" → navigates to campaign creation
  - "Explore the dashboard" → navigates to dashboard
  - "Connect an ad platform" (only shown if no platforms connected) → navigates to Connections
- **"Get Started"** button — closes the wizard

**What to do:**
1. Review the summary to confirm everything is set up
2. Click any quick-start suggestion to jump to that feature, or click **"Get Started"** to close the wizard

---

## Wizard Behavior

- The wizard appears automatically for new users and users without an active subscription
- It does **not** appear for users who have already completed it (tracked via browser storage)
- The wizard is responsive — full-screen on mobile, modal on desktop

---

**Related:**
- [Quick Start — Premium](quick-start-premium.md) — Step-by-step premium setup guide
- [Subscription & Billing](../premium/subscription.md) — Plan details and billing
- [Connections](../premium/integrations.md) — Connect ad platforms after setup
