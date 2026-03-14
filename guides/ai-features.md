[Home](../README.md) > [Guides](../README.md#guides) > AI Features

# AI Features

Defo Ads uses AI to help you generate headlines, descriptions, keywords, and complete campaign structures. AI is woven throughout the app to save you time and produce better ad content.

---

## How AI Works

Defo Ads offers two AI modes depending on your version:

### Free Version: Bring Your Own Key

In the free version, you provide your own **OpenAI API key**:

- Your key is stored **locally in your browser** and is never sent to Defo Ads servers
- AI requests go **directly from your browser to OpenAI** (no middleman)
- You pay OpenAI directly for usage based on their pricing
- You can add or change your key anytime in **Settings > General**

To get an API key, visit [platform.openai.com](https://platform.openai.com) and create one. See [Settings](settings.md) for setup instructions.

### Premium Version: Managed AI

> **Premium Feature** -- This requires a Defo Ads Premium subscription.

With Premium, AI is fully managed:

- **No API key needed** — AI works out of the box
- **Multi-provider support** — Requests are routed through EdenAI to the best available provider (OpenAI, Anthropic, Google, and more)
- **Usage quotas** — Each plan includes a monthly AI usage allowance
- **Better reliability** — If one provider is down, requests are automatically routed to another

---

## AI in Campaign Creation

The campaign creation wizard uses AI to generate a complete campaign structure from your goals.

### How It Works

1. Start a new campaign and select your campaign type and site
2. Set your target locations
3. Describe your **campaign goals** in plain language (e.g., "Sell running shoes to fitness enthusiasts in the US")
4. Choose what AI should generate:
   - Ad groups only
   - Keywords only
   - Ads only
   - **All three** (recommended)
5. AI generates a complete structure: themed ad groups, relevant keywords with match types, and compelling ad copy

![AI campaign generation](../images/ai-campaign-generation.png)

6. Review the generated content and make any adjustments
7. Finalize and create the campaign

> **Tip:** The more specific your goals, the better the AI output. Instead of "sell shoes," try "sell premium leather dress shoes to professionals aged 30-50 who value craftsmanship."

---

## AI in Sites

When you add a site (website), AI can analyze it to extract useful information automatically.

### Website Analysis

1. Enter your website URL on the **Sites** page
2. Click **"Analyze with AI"**
3. AI visits your site and extracts:
   - **Business description** — What your company does
   - **Keywords** — Relevant search terms from your site content
   - **Sitelinks** — Internal pages suitable for ad sitelink extensions
4. Review and edit the extracted data before saving

![AI site analysis](../images/ai-site-analysis.png)

This data is then used as context whenever AI generates content for campaigns linked to this site.

---

## AI in Ads

AI can help with multiple aspects of ad creation and optimization.

### Generate Ads with AI

You can generate ads from two places:

- **From the ad group list:** Select an ad group and click **"Generate Ads with AI"** to create ads for that group
- **From the entity list:** Select multiple ad groups and batch-generate ads for all of them

AI uses the campaign goals, site data, ad group theme, and keywords to create relevant responsive search ads with multiple headlines and descriptions.

![Generate ads with AI](../images/ai-generate-ads.png)

### Ad Review

Already have an ad? AI can review it and suggest improvements.

1. Open an ad in the ad editor
2. Click **"Review with AI"**
3. AI analyzes your ad and provides:
   - An overall quality **rating**
   - Specific **suggestions** for improving headlines and descriptions
   - **One-click apply** — Click a suggestion to apply it instantly

![AI ad review](../images/ai-ad-review.png)

### Ad Translation

Translate your ads into another language while respecting Google Ads character limits.

1. Open an ad in the ad editor
2. Click **"Translate with AI"**
3. Select the target language
4. AI translates all headlines and descriptions, keeping each within its character limit
5. Review and apply the translations

This is especially useful for multi-market campaigns where you need the same message in different languages.

### Sitelink Generation

AI can generate sitelink extensions for your ads based on your site data.

1. Open the sitelinks section of an ad or campaign
2. Click **"Generate with AI"**
3. AI suggests sitelinks with titles and descriptions based on your website pages
4. Select which sitelinks to add

### Landing Page Suggestions

When creating or editing ads, AI can suggest the best landing page URL from your site's pages based on the ad group theme and keywords.

---

## AI in Keywords

AI generates keyword suggestions based on your campaign context.

1. Navigate to a campaign's keyword section
2. Click **"Generate Keywords with AI"**
3. AI considers:
   - Your campaign goals
   - The ad group theme
   - Your site content and description
   - Existing keywords (to avoid duplicates)
4. Review suggested keywords and their recommended match types
5. Select and add the ones you want

![AI keyword generation](../images/ai-generate-keywords.png)

> **Tip:** AI suggests a mix of broad, phrase, and exact match keywords. See [Keyword Match Types](../reference/keyword-match-types.md) to understand the differences.

---

## Custom Instructions

Before any AI generation, Defo Ads can show you a text field to provide **custom instructions**. This lets you guide the AI for each specific generation.

### Examples of Custom Instructions

- "Focus on luxury and premium positioning"
- "Use casual, friendly language"
- "Emphasize free shipping and 30-day returns"
- "Target small business owners, not enterprise"
- "Include pricing in the headlines"

### Disabling Custom Instructions

If you prefer a faster workflow without the prompt:

1. Go to **Settings > General**
2. Toggle off **"Ask for custom instructions before AI generation"**
3. AI will generate content immediately without asking for additional input

You can re-enable it anytime.

![Custom instructions dialog](../images/ai-custom-instructions.png)

---

## AI Usage Tips

### Getting Better Results

1. **Fill in your site data** — AI uses your site description and keywords as context. The more complete your site data, the better the output.
2. **Write specific goals** — Vague goals produce generic content. Be specific about your audience, value proposition, and desired tone.
3. **Use custom instructions** — When you need something specific for a particular generation, custom instructions are the most direct way to guide AI.
4. **Iterate** — Generate, review, regenerate with adjusted instructions. AI gets better when you provide feedback through custom instructions.

### Understanding AI Limitations

- AI-generated content is a **starting point**, not a final product. Always review and refine.
- AI may occasionally produce headlines that exceed character limits. Use the ad editor to fix these.
- Generated keywords may include irrelevant terms. Review and remove anything that doesn't fit.
- AI works best in English. Other languages are supported but may produce lower quality results.

---

> The [AI Assistant](ai-assistant.md) provides a chat interface where you can manage your campaigns with natural language commands. Ask it to create campaigns, edit ads, generate keywords, and more — all through conversation. Available in both free and premium tiers.

---

**Related:**
- [Settings](settings.md) — Configure AI provider and preferences
- [Ads](ads.md) — Create and edit responsive search ads
- [Campaigns](campaigns.md) — Create and manage advertising campaigns
- [AI Assistant](ai-assistant.md) — Chat-based campaign management
