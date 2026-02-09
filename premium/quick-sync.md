[Home](../README.md) > [Premium](README.md) > Quick Sync

> **Premium Feature** — This feature requires a Defo Ads Premium subscription. [Compare plans](../getting-started/free-vs-premium.md)

# Quick Sync

Quick Sync is a streamlined one-click sync experience for returning users. After your first sync, Defo Ads remembers your configuration and lets you repeat the same operation with a single button press. No need to re-select accounts, campaigns, or options every time.

---

## What Is Quick Sync?

Quick Sync eliminates the repetitive steps of configuring a sync operation. Instead of walking through the full sync wizard each time, you see a summary of your last sync configuration and can start immediately.

This is especially useful for users who regularly import or export the same set of campaigns with the same settings.

![Quick Sync summary](../images/quick-sync-summary.png)

---

## How It Works

### Remembering Your Last Configuration

When you complete a sync using the full wizard (see [Bidirectional Sync](sync.md)), Defo Ads saves your configuration, including:

- **Sync direction** — Import, export, or both
- **Selected accounts** — Which Google Ads accounts were used
- **Selected campaigns** — Which campaigns were included
- **Sync options** — Any filters or preferences you set

The next time you visit the Sync page, Quick Sync presents this saved configuration as a ready-to-go summary.

### The Quick Sync Summary

The Quick Sync card shows a concise overview of what will happen:

| Field | Description |
|-------|-------------|
| **Import count** | Number of campaigns to import (with account name) |
| **Export count** | Number of campaigns to export (with account name) |
| **Account names** | The Google Ads accounts involved |
| **Options used** | Any special options from the last sync |
| **Last synced** | When the previous sync was completed |

![Quick Sync details](../images/quick-sync-details.png)

### Starting Quick Sync

Click the **Start Sync** button to begin. The sync uses the same configuration as your last operation. Progress tracking works exactly the same as the full sync — you see the progress bar, per-entity statuses, and error details.

### Customizing Before Syncing

If you want to change the configuration before syncing, click the **Customize Sync...** link below the summary. This opens the full sync wizard where you can:

- Add or remove campaigns from the selection
- Change the source or destination account
- Adjust sync options
- Switch between import and export

After customizing, the new configuration becomes the saved Quick Sync configuration for next time.

---

## First Time vs. Returning

### First Sync

The very first time you sync, Quick Sync is not available because there is no previous configuration to remember. You must use the full sync wizard:

1. Choose import or export
2. Select your Google Ads account
3. Pick the campaigns to sync
4. Start the sync

After this first sync completes successfully, Quick Sync becomes available.

### Returning Syncs

On subsequent visits to the Sync page, you are greeted with the Quick Sync card instead of the full wizard. You can:

- **Start immediately** with one click
- **Customize** if your needs have changed
- **Switch to full wizard** to start a completely different sync operation

![First time vs returning](../images/quick-sync-first-vs-returning.png)

---

## Smart Selection

Quick Sync does not just replay your last exact selection. It applies smart logic to update the selection based on what has changed since your last sync.

### For Import

- **New remote campaigns** — If new campaigns have appeared in your Google Ads account since the last sync, Quick Sync automatically includes them in the import selection
- **Previously imported campaigns** — These remain selected so they receive any updates from Google Ads
- **Removed campaigns** — Campaigns that no longer exist in Google Ads are automatically excluded

### For Export

- **Draft campaigns** — New campaigns you have created in Defo Ads since the last sync are automatically selected for export
- **Modified campaigns** — Campaigns that have been edited since the last export are flagged for re-export
- **Already exported campaigns** — These remain in the selection for updates
- **Campaigns without changes** — May be included but will be skipped during processing if there is nothing new to push

### Smart Selection Indicators

The Quick Sync summary highlights what is new or changed since the last sync:

- **"3 new campaigns to import"** — New remote campaigns detected
- **"2 campaigns modified since last export"** — Local changes ready to push
- **"Updated selection"** — The selection has been adjusted from the last configuration

![Smart selection indicators](../images/quick-sync-smart-selection.png)

---

## Sync History

Quick Sync maintains a history of your sync activity to help you track patterns and troubleshoot issues.

### Tracked Statistics

| Statistic | Description |
|-----------|-------------|
| **Total syncs** | The total number of sync operations you have performed |
| **Last sync timestamp** | The exact date and time of your most recent sync |
| **Preferred account** | The Google Ads account you sync with most frequently |
| **Success rate** | Percentage of sync operations that completed without errors |

### Viewing History

Sync history is available in two places:

1. **Quick Sync card** — Shows the last sync timestamp and total sync count
2. **Activity Feed** — On the Performance Dashboard, shows detailed sync events with timestamps

![Sync history](../images/quick-sync-history.png)

---

## Quick Sync Workflow Examples

### Daily Import Routine

1. Open Defo Ads and navigate to Sync
2. Quick Sync shows: "Import 12 campaigns from My Business Account"
3. Click **Start Sync**
4. New data from Google Ads flows into Defo Ads in seconds
5. Continue your work with up-to-date campaign data

### Weekly Export of New Campaigns

1. You have created 3 new campaigns during the week
2. Navigate to Sync — Quick Sync detects the new campaigns
3. Summary shows: "Export 3 new campaigns + 5 existing to My Business Account"
4. Click **Start Sync**
5. New campaigns go live on Google Ads

### After Making Bulk Edits

1. You edited budgets for 8 campaigns in Defo Ads
2. Navigate to Sync — Quick Sync flags the modified campaigns
3. Summary shows: "Export 8 modified campaigns to My Business Account"
4. Click **Start Sync**
5. Changes are pushed to Google Ads

---

## Tips

- **Quick Sync is per-user** — Your saved configuration is independent of other team members
- **Review the summary** before starting — especially after a long gap between syncs, the smart selection may have changed
- **Use Customize for one-off changes** — If you need to exclude a campaign just once, click Customize instead of changing your regular workflow
- **Quick Sync and Scheduled Sync are independent** — Quick Sync is manual; Scheduled Sync runs automatically. They do not interfere with each other

---

**Related:**
- [Bidirectional Sync](sync.md) — Full sync wizard and detailed sync reference
- [Scheduled Sync](scheduled-sync.md) — Automated background syncs
- [Google Ads Connection](google-ads-connection.md) — Setting up your account connection
- [Performance Dashboard](performance-dashboard.md) — View sync events in the Activity Feed
