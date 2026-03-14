# Quick Sync

Quick Sync lets you sync your campaigns with all connected platforms in a single click, without navigating through the full sync workflow.

## What Quick Sync Does

Quick Sync performs an immediate sync between Defo Ads and all your connected advertising platforms. It pushes your latest local changes to each platform and pulls in any changes made directly on those platforms since the last sync.

This is the fastest way to ensure your campaigns are up to date across all platforms.

![Quick Sync Summary](../images/quick-sync-summary.png)

---

## Multi-Platform Quick Sync

When you trigger a Quick Sync, it syncs with **all connected platforms simultaneously**:

- If you have Google Ads and Microsoft Advertising connected, Quick Sync will sync with both at the same time.
- Each platform syncs independently, so a delay or error on one platform does not block the other.
- The sync is bidirectional — local changes are pushed and remote changes are pulled.

---

## How to Use Quick Sync

1. Click the **Quick Sync** button in the application toolbar or dashboard.
2. The sync begins immediately with all connected platforms.
3. Monitor progress using the sync indicators (see below).
4. When complete, your campaigns reflect the latest state from all platforms.

No additional configuration or confirmation is required — Quick Sync is designed to be a one-click operation.

---

## When to Use Quick Sync vs Scheduled Sync

| Scenario | Recommended Option |
|----------|-------------------|
| You just made changes and want them on your platforms now | **Quick Sync** |
| You want to check for changes made on a platform | **Quick Sync** |
| You want ongoing automatic synchronization | **Scheduled Sync** |
| You need syncs to happen while you are away | **Scheduled Sync** |
| You made a large batch of changes and want immediate confirmation | **Quick Sync** |
| You want a set-and-forget sync setup | **Scheduled Sync** |

Quick Sync and Scheduled Sync work together. After a Quick Sync, the scheduled sync timer resets, so the next automatic sync occurs one full interval later.

---

## Sync Progress Indicators

While a Quick Sync is running, the interface displays progress indicators:

- **Toolbar indicator** — The Quick Sync button shows a spinning state while sync is in progress.
- **Per-platform progress** — Each connected platform shows its own sync progress (e.g., "Google Ads: syncing... 60%").
- **Completion notification** — When all platforms finish syncing, a notification confirms the result.

If any platform encounters an error during sync, the indicator will show a warning icon for that platform while the others may complete successfully.

![Quick Sync Details](../images/quick-sync-details.png)

---

## Handling Sync Errors

If a Quick Sync encounters errors:

- **Partial success** — If one platform syncs successfully but another fails, the successful sync is kept. You do not need to re-sync the platform that already succeeded.
- **Error details** — Click the warning indicator to see details about what went wrong (e.g., authorization expired, API rate limit reached, network timeout).
- **Retry** — After resolving the issue, click Quick Sync again. It will attempt to sync all platforms, but platforms already up to date will complete instantly.

### Common Errors

| Error | Cause | Fix |
|-------|-------|-----|
| Authorization expired | OAuth token has expired | Reconnect the platform on the [Connections](integrations.md) page |
| Rate limit exceeded | Too many API requests in a short period | Wait a few minutes and try again |
| Network timeout | Connectivity issue | Check your internet connection and retry |
| Validation error | A campaign has data incompatible with the target platform | Review the error details and fix the flagged entities |

---

## Related

- [Sync](sync.md) — Full sync documentation including per-platform sync and conflict resolution
- [Scheduled Sync](scheduled-sync.md) — Automatic background synchronization
- [Connections](integrations.md) — Connect and manage your platforms

![Quick Sync History](../images/quick-sync-history.png)
