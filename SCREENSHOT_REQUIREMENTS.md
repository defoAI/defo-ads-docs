# Screenshot Requirements

This document tracks screenshots that need to be captured or replaced for the documentation update (US-ADS-069).

Screenshots can be captured using:
- The running app (`./scripts/run_application.sh` from `defo-ads-api/`)
- Playwright E2E screenshot tests (`python3 scripts/run_e2e_tests.py --type fe --test capture-doc-screenshots` from `defo-ads-api/`)
- Manual browser screenshots

## Naming Convention

`{feature}-{description}.png` — all lowercase, hyphens between words.

## New Screenshots Needed

### Onboarding Wizard (6 screenshots)
- [x] `onboarding-step-welcome.png` — Welcome step with language selector → `getting-started/onboarding-wizard.md`
- [x] `onboarding-step-auth.png` — Account/auth step with Google sign-in → `getting-started/onboarding-wizard.md`
- [ ] `onboarding-step-organisation.png` — About You step with purpose chips → `getting-started/onboarding-wizard.md` *(requires manual capture — Google OAuth blocks E2E)*
- [ ] `onboarding-step-plans.png` — Plan selection with plan cards → `getting-started/onboarding-wizard.md` *(requires manual capture)*
- [ ] `onboarding-step-platforms.png` — Platform connection step → `getting-started/onboarding-wizard.md` *(requires manual capture)*
- [ ] `onboarding-step-done.png` — Completion step with summary → `getting-started/onboarding-wizard.md` *(requires manual capture)*

### Connections View (4 screenshots)
- [x] `connections-overview-tab.png` — Overview tab with all platform cards → `premium/integrations.md`
- [x] `connections-google-tab.png` — Google Ads detail tab → `premium/integrations.md`
- [x] `connections-msads-tab.png` — Microsoft Ads detail tab → `premium/integrations.md`
- [x] `connections-quota-stats.png` — Usage & statistics section → `premium/integrations.md`

### Conversion Tracking (3 screenshots)
- [x] `conversions-list.png` — Updated conversions page with summary stats → `premium/conversions.md`
- [x] `conversions-wizard.png` — Conversion creation wizard → `premium/conversions.md`
- [x] `conversions-tracking-code.png` — Tracking code installation dialog → `premium/conversions.md`

### Sync Page (3 screenshots)
- [x] `sync-section-layout.png` — Section-based layout (Push/Pull/Remove) → `premium/sync.md`
- [x] `sync-pending-badge.png` — Pending changes badge in sidebar → `premium/sync.md`
- [x] `sync-record-summary.png` — Sync record detail page → `premium/sync.md`

### Keywords (2 screenshots)
- [x] `keyword-detail-page.png` — Keyword detail page with General tab → `guides/keywords.md`
- [x] `keyword-creation-dialog.png` — Keyword creation dialog from list view → `guides/keywords.md`

### AI Assistant (2 screenshots)
- [x] `ai-suggestion-chips.png` — Context-aware suggestion chips below chat → `guides/ai-assistant.md`
- [x] `ai-activity-feed.png` — Live agent activity feed → `guides/ai-assistant.md`

### Campaign Details (1 screenshot)
- [x] `budget-advisor-view.png` — Budget Advisor with cap and allocation → `guides/campaign-details.md`

### Navigation (1 screenshot)
- [x] `plan-status-indicator.png` — Plan status indicator in top nav bar → `premium/subscription.md`

### Settings (1 screenshot)
- [x] `settings-page-updated.png` — Settings page without Prompt Config tab → `guides/settings.md`

## Screenshots to Replace (Existing but Stale)

These existing screenshots have been re-captured via E2E tests:

- [x] `settings-page.png` — Re-captured without Prompt Config tab
- [x] `sync-multi-platform-overview.png` — Re-captured with new section-based view
- [x] `sync-page-overview.png` — Re-captured with new layout
- [x] `integrations-multi-platform.png` — Re-captured with new Connections view
- [x] `integrations-overview.png` — Re-captured with new layout
- [x] `subscription-plan-comparison.png` — Re-captured with current layout

## Screenshots Deleted (Removed Features)

- [x] `settings-prompt-config.png` — Deleted (Prompt Config tab no longer exists)
- [x] `settings-prompt-editor.png` — Deleted (Prompt editor no longer exists)
- [x] `ai-prompt-editor.png` — Deleted (Prompt editor no longer exists)

---

**Summary: 19/23 new screenshots captured via E2E + 6 replacements refreshed + 3 deletions completed**
**Remaining: 4 onboarding wizard screenshots need manual capture (post-OAuth steps)**
