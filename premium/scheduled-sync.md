# Scheduled Sync

Scheduled sync automatically keeps your campaigns in sync with your connected platforms on a regular interval, without requiring manual action.

## How Scheduled Sync Works

When you connect a platform to Defo Ads, a scheduled sync is automatically created for that platform. The system runs sync operations in the background at regular intervals, ensuring your Defo Ads campaigns stay up to date with the latest data from each connected platform.

Scheduled syncs run independently — you do not need to keep the Defo Ads application open for them to execute.

![Scheduled Sync Settings](../images/scheduled-sync-settings.png)

---

## Per-Platform Scheduling

Each connected platform has its own sync schedule. This means:

- Google Ads and Microsoft Advertising can sync on different intervals if configured that way.
- Connecting a new platform automatically creates a schedule for it.
- Disconnecting a platform removes its scheduled sync.

---

## Default Schedule

When you connect a platform, Defo Ads automatically creates a scheduled sync with a **6-hour interval**. This means your campaigns will sync with the connected platform approximately four times per day.

The default schedule is designed to keep your data reasonably current without overloading the platform APIs.

---

## Schedule Management

Scheduled sync settings are **admin-controlled**. This means:

- **Admins** can view, modify, and disable sync schedules from the admin dashboard.
- **Regular users** can see the sync status and the last sync time, but cannot change the schedule.

This separation ensures consistent sync behavior across the organization and prevents accidental schedule changes.

### What Admins Can Do

- View the current sync interval for each connected platform.
- Change the sync interval (e.g., from 6 hours to 12 hours).
- Pause or resume scheduled sync for a specific platform.
- View the sync history log.

### What Users Can See

- The last successful sync time for each platform.
- The next scheduled sync time.
- Whether scheduled sync is active or paused for each platform.

---

## Sync Status Indicator

The Defo Ads interface displays a sync status indicator that shows the current state of your scheduled syncs:

| Status | Meaning |
|--------|---------|
| **Synced** | All platforms are up to date as of the last scheduled sync |
| **Syncing** | A scheduled sync is currently in progress |
| **Pending** | A scheduled sync is queued and will start shortly |
| **Error** | The last scheduled sync encountered an error |
| **Paused** | Scheduled sync has been paused by an admin |

The indicator is visible in the application header so you always know the current sync state at a glance.

![Sync Status](../images/scheduled-sync-status.png)

---

## What Triggers a Scheduled Sync

Scheduled syncs are triggered by the configured time interval. Additionally, a sync may be triggered in the following situations:

- **Platform connection** — A sync runs shortly after you first connect a platform to pull in the initial data.
- **After a manual sync** — The schedule timer resets after a manual sync or quick sync, so the next scheduled sync occurs one full interval after the last sync (manual or scheduled).
- **After an error** — If a scheduled sync fails, the system will retry after a shorter interval before falling back to the regular schedule.

Scheduled syncs do **not** trigger when:

- The platform is disconnected.
- An admin has paused the schedule.
- Another sync (manual or scheduled) is already in progress for that platform.

---

## Viewing Sync History

You can view the history of past sync operations to understand what was synced and when:

1. Navigate to **Settings > Sync History** (or the sync section of your dashboard).
2. The history shows each sync operation with:
   - **Timestamp** — When the sync ran.
   - **Platform** — Which platform was synced.
   - **Direction** — Whether it was an import, export, or bidirectional sync.
   - **Result** — Success, partial success, or failure.
   - **Entities synced** — Number of campaigns, ad groups, keywords, and ads processed.

This log is useful for diagnosing issues or verifying that scheduled syncs are running as expected.

![Sync Activity Feed](../images/scheduled-sync-activity-feed.png)

---

## Related

- [Sync](sync.md) — Full sync documentation including manual sync and conflict resolution
- [Quick Sync](quick-sync.md) — One-click sync for immediate updates
- [Platform Integrations](integrations.md) — Connect and manage your platforms
