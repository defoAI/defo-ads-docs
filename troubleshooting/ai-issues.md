[Home](../README.md) > [Troubleshooting](../README.md#troubleshooting) > AI Issues

# AI Issues

Defo Ads uses AI to generate ad content, keywords, and campaign structures. This page covers common AI-related problems and how to resolve them for both the free and premium versions.

---

## Free Version Issues

The free version uses your own OpenAI API key to make AI requests directly from your browser. Issues are typically related to your API key or OpenAI account.

### API Key Required

**Error message:** "API Key Required" or "No API key configured"

**Cause:** You have not entered your OpenAI API key in the app settings.

**Solution:**

1. Go to **Settings** in the sidebar
2. Navigate to the **General** section
3. Enter your OpenAI API key in the API key field
4. Click **Save**

**Where to get an API key:** Go to [platform.openai.com](https://platform.openai.com), sign in, navigate to **API Keys**, click **"Create new secret key"**, and copy the key (starts with `sk-`).

![API key settings](../images/ts-ai-api-key-settings.png)

> **Important:** Your API key is stored in your browser's localStorage and is never sent to Defo Ads servers.

---

### Invalid API Key

**Error message:** "Invalid API key" or "Incorrect API key provided"

**Cause:** The API key you entered is not valid or has been revoked.

**Solution:**

1. **Check the key format.** OpenAI API keys start with `sk-`. Make sure you copied the entire key without extra spaces.
2. **Verify the key is active.** Log in to [platform.openai.com/api-keys](https://platform.openai.com/api-keys) and check that the key is listed and not revoked.
3. **Create a new key.** If the key was revoked or you are unsure, create a new one and replace it in Settings.
4. **Check for trailing spaces.** When pasting the key, ensure there are no invisible whitespace characters at the beginning or end.

---

### AI Generation Failed

**Error message:** "AI generation failed" or "Error generating content"

**Cause:** The request to OpenAI failed. This can have several causes.

**Solutions (check in order):**

1. **Check your API key balance.** Log in to [platform.openai.com/usage](https://platform.openai.com/usage) and verify you have available credits. If your balance is zero, add funds.

2. **Check OpenAI service status.** Visit [status.openai.com](https://status.openai.com) to see if OpenAI is experiencing an outage or degraded performance.

3. **Try again.** Transient errors happen occasionally. Wait a moment and retry the generation.

4. **Simplify your request.** Very large generation requests (e.g., generating 10+ ad groups with full ads and keywords) may time out. Try generating fewer items at once.

5. **Check your browser's network.** Open your browser's developer console (F12 > Network tab) to see if the request is being blocked by an extension, firewall, or corporate proxy.

---

### Rate Limit from OpenAI

**Error message:** "Rate limit exceeded" or "Too many requests (429)"

**Cause:** You are making too many API requests in a short period. OpenAI enforces rate limits based on your account tier.

**Solution:**

1. **Wait and retry.** Rate limits typically reset within 60 seconds.
2. **Reduce request frequency.** If you are generating content for multiple campaigns in a row, add a short pause between requests.
3. **Check your OpenAI tier.** Free OpenAI accounts have stricter rate limits. Consider upgrading your OpenAI account for higher limits.

> **Note:** This is an OpenAI rate limit, not a Defo Ads limit. The free version of Defo Ads does not impose any rate limiting.

---

## Premium Version Issues

The premium version uses managed AI provided by the Defo Ads backend. You do not need your own API key, but usage is subject to your plan's daily limits.

### AI Quota Exceeded

**Error message:** "AI quota exceeded" or "Daily token limit reached"

**Cause:** You have used all of your daily AI tokens for the current period.

**Solution:**

1. **Check your usage.** Go to your **User Profile** to see your current token usage and the time until the next reset.
2. **Wait for reset.** Daily limits reset every 24 hours. The exact reset time is shown in your User Profile.
3. **Upgrade your plan.** If you consistently hit the limit, consider upgrading to a plan with a higher token allowance.
4. **Use AI more efficiently.** Generate full campaigns at once rather than individual components, and provide detailed context so the AI produces good output on the first try.

![AI quota usage in profile](../images/ts-ai-quota-usage.png)

See [Limits & Quotas](../reference/limits-and-quotas.md) for details on how token limits work.

---

### AI Service Unavailable

**Error message:** "AI service unavailable" or "Service temporarily down"

**Cause:** The backend AI provider (EdenAI or its underlying models) is experiencing temporary issues.

**Solution:**

1. **Wait a few minutes** and try again. Most AI service outages are brief.
2. **Try a simpler request.** If generating a full campaign fails, try generating just headlines or just keywords.
3. **Check back later.** If the issue persists for more than 30 minutes, the team is likely already working on it.

This is a server-side issue and does not require any action on your part beyond waiting.

---

### Generation Takes Too Long

**Error message:** No error, but the generation spinner runs for a very long time.

**Expected times:**

| Request Type | Typical Time |
|-------------|-------------|
| Single headline or description | 5-10 seconds |
| Full ad (all headlines + descriptions) | 10-20 seconds |
| Full campaign (ad groups + keywords + ads) | 30-60 seconds |
| Campaign with Knowledge Base context | 30-90 seconds |

**If generation exceeds these times:**

1. **Be patient.** Large requests with detailed context take longer. The AI is processing your site data, knowledge base documents, and campaign goals.
2. **Do not close the page.** Closing the page will cancel the request and you will lose the progress.
3. **Check your internet connection.** Slow connections can delay responses.
4. **Simplify your request.** Generate fewer components at once (e.g., just ad groups first, then keywords separately).

If a request takes more than 2 minutes without completing, it has likely timed out. Refresh the page and try again with a smaller request.

---

## General AI Tips

These tips apply to both the free and premium versions and help you get better results from AI generation.

### Provide Better Context

The quality of AI output directly depends on the context you provide. More detail leads to better ads.

**Good context leads to good output:**

- **Site descriptions:** Add detailed descriptions of your business, products, and services when creating a site. Include unique selling points, target audience, and key benefits.
- **Campaign goals:** Write specific, detailed goals. "Drive sign-ups for our free trial of the project management tool, targeting small business owners who manage remote teams" produces far better output than "get more sign-ups."
- **Knowledge Base documents:** Upload or paste documents about your business, products, case studies, or brand guidelines. The AI uses these to generate more relevant content. See [Knowledge Base](../guides/knowledge-base.md).

![Site description for AI context](../images/ts-ai-site-context.png)

### Use Custom Instructions

The **custom instructions** field lets you guide the AI for each generation request. Use it to:

- Specify tone: "Use a professional, formal tone"
- Request specific content: "Mention our 30-day money-back guarantee in at least one headline"
- Set constraints: "Do not use exclamation marks"
- Request language: "Generate all content in German"
- Guide style: "Keep descriptions factual, avoid superlatives"

### Use the Prompt Editor

In **Settings**, the **Prompt Editor** lets you customize the system prompts that the AI uses for content generation. This is an advanced feature for users who want fine-grained control over how the AI behaves.

**When to use the Prompt Editor:**

- When default AI output consistently does not match your brand voice
- When you want to enforce specific writing rules across all generations
- When you have domain-specific terminology the AI should use

> **Caution:** Editing prompts incorrectly can degrade AI output quality. If you are unsure, start with small changes and test the results before making larger modifications.

### Improve AI Output Quality

If the AI output is not meeting your expectations:

| Problem | Solution |
|---------|----------|
| Content is too generic | Add more detail to your site description and campaign goals |
| Wrong tone or style | Use custom instructions to specify your preferred tone |
| Irrelevant keywords | Add negative keywords after generation; refine your goals text |
| Content in wrong language | Set the campaign target language and add a language instruction |
| Too similar to competitors | Add unique selling points to your site description and Knowledge Base |
| Descriptions are too vague | Provide specific product details, pricing, and offers in your context |

### When to Edit Manually

AI generation is a starting point, not the final product. You should always review and edit:

- **Brand-specific details** -- Prices, offers, and promotions the AI cannot know about
- **Legal requirements** -- Disclaimers, trademark symbols, or compliance language
- **Calls to action** -- Tailor these to your specific conversion goals
- **Local nuances** -- Cultural references or regional terminology

---

## Error Reference

Quick lookup for common AI error codes:

| Error Code | Meaning | Version | Solution |
|------------|---------|---------|----------|
| `API_KEY_REQUIRED` | No API key configured | Free | Enter key in Settings |
| `INVALID_API_KEY` | API key is invalid | Free | Check or replace key |
| `OPENAI_RATE_LIMIT` | Too many requests to OpenAI | Free | Wait 60 seconds, retry |
| `OPENAI_INSUFFICIENT_QUOTA` | OpenAI account out of credits | Free | Add funds at platform.openai.com |
| `AI_QUOTA_EXCEEDED` | Daily token limit reached | Premium | Wait for reset or upgrade plan |
| `AI_SERVICE_UNAVAILABLE` | Backend AI is down | Premium | Wait and retry |
| `GENERATION_TIMEOUT` | Request took too long | Both | Simplify request, retry |
| `INVALID_REQUEST` | Malformed generation request | Both | Check inputs, retry |

---

## Still Having Issues?

If AI problems persist:

1. **Free version:** Verify your API key works by testing it directly at [platform.openai.com/playground](https://platform.openai.com/playground)
2. **Premium version:** Check your usage in User Profile and ensure you have quota remaining
3. **Both versions:** Try a simple generation first (single headline) to isolate the issue
4. **Contact support** with the error message and what you were trying to generate

---

**Related:**
- [AI Features](../guides/ai-features.md) -- How AI generation works in Defo Ads
- [Knowledge Base](../guides/knowledge-base.md) -- Add documents for better AI context
- [Settings](../guides/settings.md) -- Configure API keys and prompt editor
- [Limits & Quotas](../reference/limits-and-quotas.md) -- Token limits and daily resets
- [Common Issues](common-issues.md) -- General troubleshooting
- [Sync Errors](sync-errors.md) -- Google Ads sync problems
