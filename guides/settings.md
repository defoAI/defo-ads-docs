[Home](../README.md) > [Guides](../README.md#guides) > Settings

# Settings

Configure your AI setup and control your data. The Settings page also includes theme and language options accessible from the top navigation bar.

---

## Accessing Settings

Click **Settings** in the sidebar to open the Settings page. The page is organized into tabs:

- **General** — AI provider selection, API key management, and behavior preferences
- **Team** — Team member management (Premium)
- **Notifications** — Email and notification preferences (Premium)
- **Imprint** — Legal and contact information

> **Note:** Platform connections and conversion tracking have their own dedicated pages accessible from the sidebar. See [Connections](../premium/integrations.md) and [Conversions](../premium/conversions.md).

![Settings page](../images/settings-page.png)

---

## General Tab

The General tab contains your core AI and app preferences.

### AI Provider

You can choose between two AI providers:

- **Premium AI** (default) — Uses your plan's AI allowance. No setup required. AI translations, generation, and image creation are handled automatically.
- **Your Own API Key** — Use your personal OpenAI key. You control costs directly.

Toggle between the two options using the provider cards in the General tab. When "Your Own API Key" is selected, the API Key input field becomes visible.

### OpenAI API Key

Your API key connects Defo Ads to OpenAI for AI-powered features. This field is only shown when using your own API key.

1. Get an API key from [platform.openai.com](https://platform.openai.com)
2. Paste it into the **OpenAI API Key** field
3. The key is saved automatically

![API key field](../images/settings-api-key.png)

**Important security details:**
- Your key is stored **locally in your browser only**
- It is **never sent to Defo Ads servers** — AI requests go directly from your browser to OpenAI
- If you clear your browser data, you'll need to re-enter the key
- You can remove the key at any time by clearing the field

> **Tip:** Using your own API key is optional. The default managed AI provider works out of the box with no setup required.

### AI Behavior: Custom Instructions

Toggle: **"Ask for custom instructions before AI generation"**

- **On** (default) — Before each AI generation, a dialog appears where you can provide specific instructions (e.g., "Use formal tone" or "Focus on price savings")
- **Off** — AI generates content immediately without prompting for additional instructions

### User Proficiency Level

Defo Ads adapts its AI explanations based on your experience level:

| Level | Description |
|-------|-------------|
| **Beginner** | AI provides detailed explanations and simpler suggestions |
| **Intermediate** | Balanced detail with some technical terminology |
| **Advanced** | Concise output, assumes knowledge of ads platform concepts |

Your proficiency level is initially determined through an assessment when you first use the app. You can:

- **View your current level** in the General tab
- **Reset assessment** — Click the reset button to retake the proficiency assessment

![User proficiency](../images/settings-proficiency.png)

---

## Imprint Tab

The Imprint tab displays legal company information and contact details, including:

- Company name and address
- Contact email
- Legal disclaimers
- Links to privacy policy and terms of service

---

## Theme

Switch between **dark mode** and **light mode** using the theme toggle in the **top navigation bar** (not in Settings).

![Theme toggle](../images/settings-theme-toggle.png)

- Click the sun/moon icon to switch themes
- Your preference is saved and persists across sessions
- Dark mode reduces eye strain in low-light environments and can save battery on OLED screens

---

## Language

Switch the app language using the language selector in the **top navigation bar**.

Supported languages:

| Language | Code |
|----------|------|
| English | EN |
| German | DE |
| French | FR |

![Language selector](../images/settings-language-selector.png)

- Click the language code or flag icon in the top bar
- Select your preferred language from the dropdown
- The entire interface updates immediately
- Your preference is saved and persists across sessions

> **Note:** AI-generated content language is controlled separately. When generating ads, you can choose the target language regardless of your interface language.

---

## Data Management

### Clear All Data

If you need to start fresh or want to remove all your data:

1. Go to **Settings > General** (scroll to the bottom)
2. Click **"Clear All Data"**
3. A **confirmation dialog** appears listing exactly what will be deleted:
   - All campaigns
   - All ad groups
   - All ads
   - All keywords
   - All sites
   - All negative keyword lists
4. Click **"Confirm"** to permanently delete all data

![Clear all data dialog](../images/settings-clear-data-dialog.png)

**What is preserved:**
- Your OpenAI API key
- Your customized prompt templates
- Your theme and language preferences

> **Warning:** This action cannot be undone. If you want to keep your data, **export a JSON backup** first. See [Import & Export](import-export.md).

---

## Additional Settings Tabs

Additional tabs are available depending on your plan:

- **Team** — Manage team members, invite collaborators, set permissions. See [Team Collaboration](../premium/team-collaboration.md).
- **Notifications** — Configure email and notification preferences.

![Settings Notifications tab](../images/settings-notifications-tab.png)

> **Note:** Account management including deleting your account is available from the [User Profile](../premium/user-profile.md) page.

You can choose to use the managed AI provider (no API key needed) or your own OpenAI key. See the [AI Provider](#ai-provider) section above.

> **Note:** Platform connections (Google Ads, Microsoft Advertising) are managed from the dedicated **Connections** page in the sidebar, not from Settings. See [Connections](../premium/integrations.md).

---

## Common Questions

### Where is my data stored?

Your data is stored securely in the cloud and synced across devices. You can access your campaigns from any browser or device by signing in to your account.

### Can I use Defo Ads without an API key?

Yes. Managed AI is included with all plans — no API key needed. If you prefer to use your own OpenAI key, you can configure it in **Settings > General**.

### How do I transfer my data to a new device?

Simply sign in to your Defo Ads account on the new device. Your campaigns are stored in the cloud and automatically available.

---

**Related:**
- [AI Features](ai-features.md) — Overview of all AI-powered features
- [Connections](../premium/integrations.md) — Connect and manage ad platforms (Premium)
- [Team Collaboration](../premium/team-collaboration.md) — Manage team members (Premium)
- [User Profile](../premium/user-profile.md) — Account and subscription management (Premium)
