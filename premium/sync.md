# Sync

Sync keeps your campaigns in Defo Ads aligned with your connected advertising platforms. You can sync with a single platform or all connected platforms at once, and track progress in real time.

## Overview

The Sync page organizes your campaigns into three sections:

- **Push** — Campaigns to send from Defo Ads to your connected platforms. Each campaign row shows which platforms it will be pushed to.
- **Pull** — Campaigns to pull from your connected platforms into Defo Ads. When multiple platforms are connected, campaigns are grouped by source platform.
- **Remove** — Campaigns marked for deletion. Deletions are deferred until the next sync, giving you a chance to review and restore before they are permanently removed from your ad platforms.

Each section is collapsible and shows a count of selected campaigns (e.g., "5/8"). Use the select-all checkbox to quickly include or exclude all campaigns in a section.

<!-- TODO: Replace with updated screenshot showing section-based layout -->
![Sync Page Overview](../images/sync-multi-platform-overview.png)

---

## Pending Changes Badge

When you have unsaved changes that need syncing, a **badge** appears on the Sync item in the sidebar navigation showing the number of pending changes. This makes it easy to see at a glance whether you need to sync.

---

## What Gets Synced

Sync operations cover the full campaign hierarchy:

| Entity | Description |
|--------|-------------|
| **Campaigns** | Campaign settings, budgets, bidding strategies, targeting, status |
| **Ad Groups** | Ad group names, bids, status |
| **Keywords** | Keyword text, match types, bids, status, negative keywords |
| **Ads** | Ad copy (headlines, descriptions), URLs, status |
| **Conversion Actions** | Conversion tracking configuration (when exporting) |

---

## Deferred Deletion

When you delete a campaign that is linked to an ad platform, Defo Ads does **not** immediately remove it from the platform. Instead:

1. The campaign is **soft-deleted** locally and moves to the **Remove** section on the Sync page.
2. You can review the pending deletions before syncing. Each item shows when it was deleted and which platforms it will be removed from.
3. To **restore** a campaign, uncheck it in the Remove section before syncing.
4. When you sync, checked items in the Remove section are permanently deleted from the connected platforms.

This prevents accidental deletions from immediately affecting your live ad campaigns.

---

## Multi-Platform Sync

When you have multiple platforms connected, the Push section shows platform targeting for each campaign:

- **Platform chips** on each row indicate which platforms a campaign will be pushed to.
- You can **toggle each platform** on or off per campaign.
- **Select the account** for each platform independently.
- Platforms with expired authentication are visually disabled and cannot be synced until reconnected.

To sync with all platforms at once, select your campaigns and click **Sync**. Each platform syncs independently, so a delay or error on one platform does not block the other.

---

## Sync Progress Tracking

During a sync operation, Defo Ads displays real-time progress for each platform:

- **Per-platform progress bars** show the percentage of entities processed for each connected platform.
- **Cross-platform status tracking** gives you an overview of which platforms have completed syncing and which are still in progress.
- **Auto-completion** — When all operations finish, the progress view transitions to the sync summary automatically.

Progress indicators update in real time so you can monitor the operation without refreshing.

![Sync Progress](../images/sync-progress-bar.png)

---

## Sync Records

Each sync operation generates a **Sync Record** — a persistent summary with a unique ID that you can reference later.

### Viewing Sync Records

After a sync completes, you are taken to the **Sync Record Summary** page (`/sync/<id>`). You can also access past sync records from the sync history.

### What a Sync Record Shows

- **Overall status** — Completed, Partial (with warnings), or Failed
- **Timestamp and duration** — When the sync ran and how long it took
- **Entity summary** — Total campaigns, ad groups, keywords, and ads synced
- **Per-platform cards** — Expandable sections showing results for each platform:
  - Direction badges (Pushed, Pulled, Removed)
  - Campaign details nested by operation
  - Error count if any failures occurred

Sync records are retained for 90 days.

> **Tip:** You can ask the AI assistant about your sync history using commands like "show my recent syncs" or "what happened in my last sync?"

---

## Platform-Specific Considerations

### Microsoft Advertising

When syncing campaigns to Microsoft Advertising, be aware of the following automatic adjustments:

- **DISPLAY campaigns become Audience campaigns.** Microsoft Advertising does not have a direct equivalent of Google's Display campaigns. Defo Ads automatically maps DISPLAY campaign types to Microsoft's Audience campaign type during sync.
- **Broad match negative keywords are converted to phrase match.** Microsoft Advertising does not support broad match for negative keywords. During sync, any broad match negative keywords are automatically converted to phrase match to maintain compatibility.

### Google Ads

Google Ads supports all campaign types and keyword match types used in Defo Ads without conversion.

---

## Conflict Resolution

When the same entity has been modified both in Defo Ads and on the platform since the last sync, a conflict occurs. Defo Ads handles conflicts as follows:

- **Last write wins** — By default, the most recent change takes precedence. If you edited a campaign in Defo Ads after it was last synced, your local changes will overwrite the platform version when pushed.
- **Pull overwrites local** — When pulling, platform data replaces local data for the imported entities.
- **Review before sync** — Before pushing, the Sync page shows a summary of changes. Review the Push section to catch any unintended overwrites.

> **Tip:** If you are unsure about conflicts, pull first to get the latest platform data, then make your changes in Defo Ads, and push afterward.

---

## Related

- [Quick Sync](quick-sync.md) — One-click sync for immediate updates
- [Scheduled Sync](scheduled-sync.md) — Automatic background synchronization
- [Import & Export Guide](../guides/import-export.md) — CSV and JSON import/export for offline editing
- [Connections](integrations.md) — Connect and manage your ad platforms

![Platform Links](../images/sync-platform-links.png)
