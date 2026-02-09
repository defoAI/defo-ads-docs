[Home](../README.md) > [Guides](../README.md#guides) > Settings

# Settings

Configure your AI setup, customize prompts, manage your Knowledge Base, and control your data. The Settings page also includes theme and language options accessible from the top navigation bar.

---

## Accessing Settings

Click **Settings** in the sidebar to open the Settings page. The page is organized into tabs:

- **General** — API key and AI behavior preferences
- **Prompt Config** — Customize AI prompt templates
- **Documentation** — Knowledge Base documents
- **Imprint** — Legal and contact information

![Settings page](../images/settings-page.png)

---

## General Tab

The General tab contains your core AI and app preferences.

### OpenAI API Key

Your API key connects Defo Ads to OpenAI for AI-powered features.

1. Get an API key from [platform.openai.com](https://platform.openai.com)
2. Paste it into the **OpenAI API Key** field
3. The key is saved automatically

![API key field](../images/settings-api-key.png)

**Important security details:**
- Your key is stored **locally in your browser only**
- It is **never sent to Defo Ads servers** — AI requests go directly from your browser to OpenAI
- If you clear your browser data, you'll need to re-enter the key
- You can remove the key at any time by clearing the field

> **Tip:** You can use Defo Ads without an API key. All features work except AI generation. You can always add a key later.

### AI Behavior: Custom Instructions

Toggle: **"Ask for custom instructions before AI generation"**

- **On** (default) — Before each AI generation, a dialog appears where you can provide specific instructions (e.g., "Use formal tone" or "Focus on price savings")
- **Off** — AI generates content immediately without prompting for additional instructions

This is a convenience setting. When off, you can still influence AI output through your Knowledge Base documents and prompt templates.

### User Proficiency Level

Defo Ads adapts its AI explanations based on your experience level:

| Level | Description |
|-------|-------------|
| **Beginner** | AI provides detailed explanations and simpler suggestions |
| **Intermediate** | Balanced detail with some technical terminology |
| **Advanced** | Concise output, assumes knowledge of Google Ads concepts |

Your proficiency level is initially determined through an assessment when you first use the app. You can:

- **View your current level** in the General tab
- **Reset assessment** — Click the reset button to retake the proficiency assessment

![User proficiency](../images/settings-proficiency.png)

---

## Prompt Config Tab

The Prompt Config tab lets you view and customize the AI prompt templates used throughout Defo Ads.

### Viewing Prompts

The tab displays a list of all prompt templates, organized by feature area:

- Campaign generation prompts
- Ad generation and review prompts
- Keyword generation prompts
- Site analysis prompts
- Translation prompts
- And more

Each prompt shows its name and a **"Customized"** badge if you've modified it from the default.

![Prompt config list](../images/settings-prompt-config.png)

### Editing a Prompt

1. Click on any prompt to open it in the editor
2. Modify the prompt text
3. Use **placeholders** to insert dynamic data — available placeholders are listed below the editor for each prompt

Common placeholders include:

| Placeholder | Description |
|-------------|-------------|
| `{campaignGoals}` | The campaign's goals text |
| `{siteDescription}` | The linked site's business description |
| `{siteKeywords}` | Keywords extracted from the site |
| `{adGroupName}` | The current ad group's name |
| `{keywords}` | Keywords in the current ad group |
| `{language}` | The target language for generation |
| `{customInstructions}` | Custom instructions provided by the user |

4. Click **"Save"** to apply your changes

![Prompt editor](../images/settings-prompt-editor.png)

### Resetting Prompts

If a customized prompt isn't producing good results, you can restore the default:

- **Reset one prompt** — Click the **reset icon** next to any customized prompt
- **Reset all prompts** — Click **"Reset All"** to restore every prompt to its factory default

Resetting is non-destructive to your other settings and data.

> **Tip:** Before customizing prompts, try using **custom instructions** and **Knowledge Base documents** first. These are easier to manage and don't require understanding prompt engineering.

---

## Documentation Tab

The Documentation tab is where you manage your **Knowledge Base** — custom documents that provide AI with additional context about your business.

This is covered in detail in the [Knowledge Base](knowledge-base.md) guide. In summary:

- **Add documents** with markdown content
- **Enable/disable** documents without deleting them
- **Edit** existing documents
- **Delete** documents you no longer need

![Documentation tab](../images/settings-documentation-tab.png)

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
- Your Knowledge Base documents
- Your theme and language preferences

> **Warning:** This action cannot be undone. If you want to keep your data, **export a JSON backup** first. See [Import & Export](import-export.md).

---

## Premium Settings

> **Premium Feature** -- Premium subscribers have access to additional settings tabs.

Premium adds these tabs to the Settings page:

- **Team** — Manage team members, invite collaborators, set permissions. See [Team Collaboration](../premium/team-collaboration.md).
- **Account** — View subscription status, manage billing, view usage statistics, and delete your account. See [User Profile](../premium/user-profile.md).

Premium users also do not need to configure an OpenAI API key, as AI is fully managed through the Premium service.

---

## Common Questions

### Where is my data stored?

In the **free version**, all data is stored in your browser's localStorage. Clearing browser data will delete your campaigns. Back up regularly using [Import & Export](import-export.md).

In the **premium version**, data is stored securely in the cloud and synced across devices.

### Can I use Defo Ads without an API key?

Yes. All campaign management features work without an API key. Only AI-powered features (generation, review, translation) require either an API key (free) or a Premium subscription.

### Will changing prompts affect existing campaigns?

No. Prompt changes only affect **future** AI generations. Existing ads, keywords, and other content remain unchanged.

### How do I transfer my data to a new browser?

1. In your current browser: **Import / Export > Export > JSON** (all campaigns)
2. In your new browser: Open Defo Ads, complete the welcome wizard
3. Go to **Import / Export > Import > JSON** and upload your backup file

---

**Related:**
- [AI Features](ai-features.md) — Overview of all AI-powered features
- [Knowledge Base](knowledge-base.md) — Custom documents for AI context
- [Team Collaboration](../premium/team-collaboration.md) — Manage team members (Premium)
- [User Profile](../premium/user-profile.md) — Account and subscription management (Premium)
