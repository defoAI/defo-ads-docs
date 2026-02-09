[Home](../README.md) > [Reference](../README.md#reference) > Keyword Match Types

# Keyword Match Types

Match types control how closely a user's search query must relate to your keyword for your ad to appear. Choosing the right match type balances **reach** (how many people see your ad) with **control** (how relevant those people are).

---

## Overview

Google Ads supports three keyword match types. Each gives you a different level of control over which searches trigger your ads:

| Match Type | Syntax | Reach | Control | Example Keyword | May Match |
|------------|--------|-------|---------|-----------------|-----------|
| **Broad Match** | `women's hats` | Widest | Lowest | women's hats | buy ladies hats, female headwear, women's accessories |
| **Phrase Match** | `"women's hats"` | Medium | Medium | "women's hats" | women's hats on sale, best women's hats, buy women's hats online |
| **Exact Match** | `[women's hats]` | Narrowest | Highest | [women's hats] | women's hats, hats for women |

---

## Broad Match

**Syntax:** No special characters. Just type the keyword as-is.

**Example:** `women's hats`

Broad match gives your keyword the **widest reach**. Your ad may show for searches that are related to your keyword, even if the search does not contain the exact words. Google uses signals like user intent, search history, and related terms to determine relevance.

### What It Matches

Your keyword `women's hats` may trigger ads for searches like:

- "buy ladies hats"
- "women's headwear"
- "female accessories"
- "sun hats for women"
- "hat shop near me" (if user context suggests women's hats)

### When to Use Broad Match

- You want to **discover new search terms** you had not thought of
- You are starting a new campaign and want to gather data on what people search for
- You have **Smart Bidding** enabled (Google recommends broad match with automated bidding)
- You want **maximum reach** and are comfortable filtering irrelevant traffic later

### Caution

Broad match can show your ads for loosely related searches, which may lead to:
- Higher costs from irrelevant clicks
- Lower click-through rates
- Wasted budget on unqualified traffic

**Mitigation:** Use [negative keywords](../guides/negative-keywords.md) to block searches you do not want to trigger your ads.

---

## Phrase Match

**Syntax:** Wrap your keyword in double quotes: `"keyword"`

**Example:** `"women's hats"`

Phrase match shows your ad when the search **includes the meaning** of your keyword. The search must contain your keyword's concept, though it can include additional words before or after.

### What It Matches

Your keyword `"women's hats"` may trigger ads for searches like:

- "women's hats on sale"
- "best women's hats for summer"
- "buy women's hats online"
- "affordable women's hats near me"

### What It Does NOT Match

- "men's hats" (different meaning)
- "women's scarves" (different product)
- "hats" (too broad, missing the women's qualifier)

### When to Use Phrase Match

- You want a **balance between reach and relevance**
- You have a specific product or service and want searches that include its core meaning
- You want to capture long-tail searches (searches with extra qualifying words)
- You are comfortable with moderate traffic volume in exchange for better targeting

---

## Exact Match

**Syntax:** Wrap your keyword in square brackets: `[keyword]`

**Example:** `[women's hats]`

Exact match shows your ad only when the search has the **same meaning or intent** as your keyword. This is the most restrictive match type, giving you the tightest control over when your ads appear.

### What It Matches

Your keyword `[women's hats]` may trigger ads for searches like:

- "women's hats"
- "hats for women"
- "women hats" (close variant)

### What It Does NOT Match

- "women's hats on sale" (additional intent)
- "red women's hats" (too specific)
- "buy women's hats online" (additional words change intent)

### When to Use Exact Match

- You know **exactly** which searches are most valuable to your business
- You want **maximum control** over your budget
- You have a limited budget and cannot afford irrelevant clicks
- You are targeting **high-value, high-intent keywords** where every click matters

### Note on Close Variants

Even with exact match, Google may show your ad for close variants, including:
- Misspellings ("womens hats")
- Singular/plural forms ("woman's hat")
- Reordered words ("hats for women")
- Function words added or removed ("hats for the women")

This is by design and cannot be turned off.

---

## Comparison Table

| Factor | Broad Match | Phrase Match | Exact Match |
|--------|-------------|--------------|-------------|
| **Syntax** | `keyword` | `"keyword"` | `[keyword]` |
| **Reach** | Highest | Medium | Lowest |
| **Relevance** | Lower | Medium | Highest |
| **Control** | Least | Moderate | Most |
| **Cost per click** | Usually lower | Medium | Usually higher |
| **Conversion rate** | Usually lower | Medium | Usually higher |
| **Best with** | Smart Bidding, new campaigns | Most campaigns | High-value terms |
| **Risk** | Irrelevant traffic | Some irrelevant traffic | Missing potential traffic |

---

## Keyword Strategy Tips

### Start with a Mix

For most campaigns, use a combination of match types:

1. **Exact match** for your most important, proven keywords
2. **Phrase match** for your core product terms where you want some flexibility
3. **Broad match** for discovery -- finding new search terms you had not considered

### The Funnel Approach

| Stage | Match Type | Purpose |
|-------|-----------|---------|
| **Discovery** | Broad match | Find what people actually search for |
| **Refinement** | Phrase match | Focus on relevant search themes |
| **Optimization** | Exact match | Concentrate budget on proven winners |

### Use Negative Keywords

Regardless of match type, always maintain a negative keyword list to block irrelevant searches. This is especially important with broad match.

See [Negative Keywords](../guides/negative-keywords.md) for details on creating and managing negative keyword lists and detecting conflicts.

### Monitor Search Terms

After your campaign runs, review the **search terms report** in Google Ads to see exactly what searches triggered your ads. Use this data to:

- Add high-performing search terms as new keywords
- Add irrelevant search terms as negative keywords
- Adjust match types based on performance

### Quality Over Quantity

- 10 well-chosen exact match keywords often outperform 100 broad match keywords
- Group keywords by theme into separate ad groups for more relevant ads
- Write ad copy that closely matches your keywords for higher Quality Scores

### Character Limits

Keywords in Defo Ads follow Google Ads limits:
- Maximum keyword length: **80 characters**
- No special characters except the match type syntax (`""` or `[]`)

---

## Setting Match Types in Defo Ads

When you add keywords in Defo Ads, you can set the match type for each keyword individually:

1. Navigate to your ad group's **Keywords** tab
2. Click **"Add Keyword"** or select existing keywords
3. Choose the match type from the dropdown: Broad, Phrase, or Exact
4. The appropriate syntax is applied automatically

![Setting keyword match type](../images/ref-keyword-match-type-selector.png)

When using AI to generate keywords, the AI assigns match types based on your campaign goals and best practices. You can change these afterward.

---

**Related:**
- [Keywords](../guides/keywords.md) -- Add and manage keywords in your campaigns
- [Negative Keywords](../guides/negative-keywords.md) -- Block unwanted search terms
- [Campaign Types](campaign-types.md) -- Search campaigns use keywords for targeting
- [AI Features](../guides/ai-features.md) -- AI-generated keyword suggestions
