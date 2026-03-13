# Screenshot Requirements

This document tracks screenshots that need to be captured or replaced for the documentation update (US-ADS-069).

Screenshots can be captured using:
- The running app (`./scripts/run_application.sh` from `defo-ads-api/`)
- Playwright E2E screenshot tests (`npx playwright test e2e/docs/ --headed` from `defo-ads-premium/`)
- Manual browser screenshots

## Naming Convention

`{feature}-{description}.png` — all lowercase, hyphens between words.

## New Screenshots Needed

### Onboarding Wizard (6 screenshots)
- [ ] `onboarding-step-welcome.png` — Welcome step with language selector → `getting-started/onboarding-wizard.md`
- [ ] `onboarding-step-auth.png` — Account/auth step with Google sign-in → `getting-started/onboarding-wizard.md`
- [ ] `onboarding-step-organisation.png` — About You step with purpose chips → `getting-started/onboarding-wizard.md`
- [ ] `onboarding-step-plans.png` — Plan selection with plan cards → `getting-started/onboarding-wizard.md`
- [ ] `onboarding-step-platforms.png` — Platform connection step → `getting-started/onboarding-wizard.md`
- [ ] `onboarding-step-done.png` — Completion step with summary → `getting-started/onboarding-wizard.md`

### Connections View (4 screenshots)
- [ ] `connections-overview-tab.png` — Overview tab with all platform cards → `premium/integrations.md`
- [ ] `connections-google-tab.png` — Google Ads detail tab → `premium/integrations.md`
- [ ] `connections-msads-tab.png` — Microsoft Ads detail tab → `premium/integrations.md`
- [ ] `connections-quota-stats.png` — Usage & statistics section → `premium/integrations.md`

### Conversion Tracking (3 screenshots)
- [ ] `conversions-list.png` — Updated conversions page with summary stats → `premium/conversions.md`
- [ ] `conversions-wizard.png` — Conversion creation wizard → `premium/conversions.md`
- [ ] `conversions-tracking-code.png` — Tracking code installation dialog → `premium/conversions.md`

### Sync Page (3 screenshots)
- [ ] `sync-section-layout.png` — Section-based layout (Push/Pull/Remove) → `premium/sync.md`
- [ ] `sync-pending-badge.png` — Pending changes badge in sidebar → `premium/sync.md`
- [ ] `sync-record-summary.png` — Sync record detail page → `premium/sync.md`

### Keywords (2 screenshots)
- [ ] `keyword-detail-page.png` — Keyword detail page with General tab → `guides/keywords.md`
- [ ] `keyword-creation-dialog.png` — Keyword creation dialog from list view → `guides/keywords.md`

### AI Assistant (2 screenshots)
- [ ] `ai-suggestion-chips.png` — Context-aware suggestion chips below chat → `guides/ai-assistant.md`
- [ ] `ai-activity-feed.png` — Live agent activity feed → `guides/ai-assistant.md`

### Campaign Details (1 screenshot)
- [ ] `budget-advisor-view.png` — Budget Advisor with cap and allocation → `guides/campaign-details.md`

### Navigation (1 screenshot)
- [ ] `plan-status-indicator.png` — Plan status indicator in top nav bar → `premium/subscription.md`

### Settings (1 screenshot)
- [ ] `settings-page-updated.png` — Settings page without Prompt Config tab → `guides/settings.md`

## Screenshots to Replace (Existing but Stale)

These existing screenshots may show outdated UI and should be re-captured:

- [ ] `settings-page.png` — May still show Prompt Config tab
- [ ] `settings-prompt-config.png` — Removed feature, delete this file
- [ ] `settings-prompt-editor.png` — Removed feature, delete this file
- [ ] `sync-multi-platform-overview.png` — Old sync layout, needs new section-based view
- [ ] `sync-page-overview.png` — Old sync layout
- [ ] `integrations-multi-platform.png` — Old integrations layout
- [ ] `integrations-overview.png` — Old overview layout
- [ ] `subscription-plan-comparison.png` — May show old horizontal scroll layout

## Screenshots to Delete (Removed Features)

- [ ] `settings-prompt-config.png` — Prompt Config tab no longer exists
- [ ] `settings-prompt-editor.png` — Prompt editor no longer exists
- [ ] `ai-prompt-editor.png` — Prompt editor no longer exists

---

**Total: ~23 new screenshots + ~8 replacements + ~3 deletions**
