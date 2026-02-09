[Home](../README.md) > [Premium](README.md) > Scheduled Sync

> **Premium Feature** — This feature requires a Defo Ads Premium subscription. [Compare plans](../getting-started/free-vs-premium.md)

# Scheduled Sync

Scheduled Sync automates your Google Ads synchronization so campaigns stay up to date without manual intervention. Configure a schedule once, and Defo Ads handles the rest in the background.

---

## What Is Scheduled Sync?

Scheduled Sync runs sync operations automatically on a recurring basis. Instead of manually navigating to the Sync page and clicking a button, you configure when and how syncs should happen, and Defo Ads takes care of it.

This is ideal for users who:

- Want their Defo Ads data to always reflect the latest from Google Ads
- Need to regularly push local changes to Google Ads
- Prefer a hands-off approach to keeping data synchronized

![Scheduled Sync settings](../images/scheduled-sync-settings.png)

---

## Configuring a Schedule

### Accessing Schedule Settings

1. Navigate to the **Sync** page from the sidebar
2. Click the **Schedule** tab or the gear icon for scheduled sync settings

### Sync Direction

Choose which direction the scheduled sync should operate:

| Direction | Description |
|-----------|-------------|
| **Pull (Import)** | Automatically import campaigns from Google Ads into Defo Ads |
| **Push (Export)** | Automatically export campaigns from Defo Ads to Google Ads |
| **Both** | Run import and export in sequence |

Select the direction that matches your workflow. For example, if you primarily manage campaigns in Google Ads and use Defo Ads for analytics and editing, **Pull** is the right choice. If you create campaigns in Defo Ads and push them live, choose **Push**.

![Direction selection](../images/scheduled-sync-direction.png)

### Frequency

Set how often the scheduled sync should run:

| Frequency | Description |
|-----------|-------------|
| **Every hour** | Frequent updates for fast-moving campaigns |
| **Every 6 hours** | Balanced frequency for most users |
| **Every 12 hours** | Twice daily sync |
| **Daily** | Once per day at a set time |
| **Weekly** | Once per week on a chosen day |

Choose a frequency based on how often your campaigns change. Higher-traffic accounts benefit from more frequent syncs.

![Frequency selection](../images/scheduled-sync-frequency.png)

### Entity Filtering

Optionally, you can filter which entities are included in the scheduled sync:

- **All campaigns** — Sync everything (default)
- **Specific campaigns** — Select which campaigns to include
- **By status** — Only sync campaigns with specific statuses (e.g., Active only)
- **By account** — If multiple Google Ads accounts are connected, choose which account(s) to sync

Entity filtering helps reduce sync time and avoids unnecessary processing of campaigns you do not need updated.

![Entity filtering](../images/scheduled-sync-entity-filtering.png)

### Saving Your Schedule

After configuring direction, frequency, and optional filters, click **Save Schedule**. The schedule becomes active immediately. The next sync will run at the next scheduled interval.

---

## How Scheduled Sync Runs

### Automated Execution

Once configured, Defo Ads triggers the sync automatically at the scheduled times. The sync runs in the background — you do not need to have the app open or be logged in.

### Background Processing

Scheduled syncs operate exactly like manual syncs but without user interaction:

1. The system initiates the sync at the scheduled time
2. Campaigns are processed according to your configuration
3. Import and/or export operations complete
4. Results are logged to the Activity Feed

You do not see a progress bar during a background sync (since you may not be actively using the app), but the results are always available in the Activity Feed after completion.

### What Triggers a Scheduled Sync

- The configured time interval elapses
- Your account has an active subscription
- Your Google Ads connection is valid (not expired)

If any of these conditions are not met, the sync is skipped and a note is logged.

---

## Monitoring Scheduled Syncs

### Activity Feed

The primary way to monitor scheduled syncs is through the **Activity Feed** on the [Performance Dashboard](performance-dashboard.md). Each scheduled sync creates an entry showing:

- **Timestamp** — When the sync ran
- **Direction** — Import, export, or both
- **Entities processed** — Number of campaigns, ad groups, keywords, and ads
- **Result** — Success, partial success, or failure
- **Duration** — How long the sync took

![Activity Feed sync entries](../images/scheduled-sync-activity-feed.png)

### Schedule Status

The Sync page shows the current state of your schedule:

| Status | Meaning |
|--------|---------|
| **Active** | Schedule is running normally |
| **Paused** | Schedule is configured but temporarily paused |
| **Next run** | Shows the date and time of the next scheduled sync |
| **Last run** | Shows when the most recent scheduled sync completed |

![Schedule status](../images/scheduled-sync-status.png)

### Pausing and Resuming

You can temporarily pause a scheduled sync without deleting the configuration:

1. Go to the Sync page, Schedule tab
2. Toggle the **Pause** switch
3. The schedule is suspended until you resume it

This is useful during periods when you are making major changes and do not want background syncs interfering.

---

## Error Handling

### Automatic Retries

If a scheduled sync encounters an error, Defo Ads automatically retries using exponential backoff:

| Retry | Wait Time | Description |
|-------|-----------|-------------|
| 1st retry | 1 minute | Quick retry for transient errors |
| 2nd retry | 5 minutes | Short delay |
| 3rd retry | 30 minutes | Longer delay |
| Final retry | 2 hours | Last attempt before marking as failed |

After all retries are exhausted, the sync is marked as failed and logged to the Activity Feed.

### Common Scheduled Sync Errors

| Error | Cause | Resolution |
|-------|-------|------------|
| **Auth token expired** | Google OAuth token needs refresh | Reconnect on the [Integrations](integrations.md) page |
| **Rate limit exceeded** | Too many API calls | Reduce sync frequency or entity count |
| **Network timeout** | Temporary connectivity issue | Usually resolves on automatic retry |
| **Account suspended** | Google Ads account issue | Check your Google Ads account status |

### Error Notifications

When a scheduled sync fails (after all retries), the failure is recorded in:

- The Activity Feed on the Performance Dashboard
- The Schedule status panel on the Sync page

Review these after each scheduled run to catch issues early.

---

## Per-User Isolation

Scheduled syncs are scoped to individual users:

- **Your schedule is yours** — Other team members have their own independent schedules
- **No interference** — One user's schedule does not affect another's
- **Separate configurations** — Each user can set different directions, frequencies, and filters
- **Independent execution** — Scheduled syncs run independently for each user

This means team members working on the same campaigns can each have their own sync rhythm without conflicts.

---

## Best Practices

### Choosing the Right Frequency

- **High-activity accounts** (multiple daily changes): Every hour or every 6 hours
- **Moderate accounts** (weekly changes): Daily or every 12 hours
- **Low-activity accounts** (monthly adjustments): Weekly

### Direction Recommendations

- **Pull only:** Best if you primarily manage campaigns in Google Ads and use Defo Ads for analysis
- **Push only:** Best if you create campaigns in Defo Ads and want them automatically deployed
- **Both:** Best for full bidirectional workflows where changes happen on both sides

### Combining with Quick Sync

Scheduled Sync and [Quick Sync](quick-sync.md) complement each other:

- Use Scheduled Sync for routine background updates
- Use Quick Sync when you need an immediate sync outside the schedule
- The two do not interfere with each other

---

## Disabling Scheduled Sync

To completely remove a scheduled sync:

1. Go to the Sync page, Schedule tab
2. Click **Delete Schedule** or **Disable**
3. Confirm the action

This removes the schedule entirely. You can create a new one at any time.

---

**Related:**
- [Bidirectional Sync](sync.md) — Full manual sync reference
- [Quick Sync](quick-sync.md) — One-click manual sync
- [Google Ads Connection](google-ads-connection.md) — Connection setup and management
- [Performance Dashboard](performance-dashboard.md) — View sync activity in the Activity Feed
