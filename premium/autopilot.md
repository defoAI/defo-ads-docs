[Home](../README.md) > [Premium Features](README.md) > AI Autopilot

# AI Autopilot

Defo Ads Autopilot is your 24/7 campaign optimization engine. It monitors performance across Google Ads and Microsoft Advertising, identifies opportunities, and either recommends or automatically applies changes to maximize your results.

---

## How It Works

Autopilot runs on a continuous **Learn, Optimize, Report** cycle:

```
1. Learn     Collect baseline performance data (7-14 days)
2. Optimize  Analyze trends, propose and apply optimizations
3. Report    Weekly performance reports with full transparency
```

Every decision is logged with reasoning in the activity feed, so you always know what Autopilot did and why.

---

## Two Modes

| Mode | How It Works | Best For |
|------|-------------|----------|
| **Recommend** | Autopilot analyzes and suggests changes. You review and approve each one. | Building trust, learning what optimizations matter |
| **Auto-Optimize** | Autopilot applies changes automatically within your guardrails. | Hands-off management, saving time at scale |

You can switch between modes at any time. Start with Recommend to see what Autopilot would do, then graduate to Auto-Optimize when you are confident.

---

## What Autopilot Optimizes

Autopilot handles the 80% of campaign management that Smart Bidding does not touch:

- **Budget reallocation** shifts spend from underperforming campaigns to high performers
- **Keyword bid adjustments** fine-tunes bids based on conversion and click patterns
- **Ad performance review** pauses underperforming ads, reactivates strong ones
- **Negative keyword management** blocks wasteful search terms automatically
- **Audience refinement** adjusts targeting based on performance signals
- **Budget pacing** ensures you stay on track for your monthly cap

---

## Cross-Platform Support

Autopilot works across both Google Ads and Microsoft Advertising from a single dashboard. Optimizations are platform-aware: budget shifts respect per-platform allocations, and reporting shows per-platform breakdowns.

---

## Budget Safety Guardrails

Every optimization runs through guardrail checks before being applied:

| Guardrail | What It Protects | Default |
|-----------|-----------------|---------|
| **Monthly Cap** | Total monthly spend cannot exceed your budget | Set by you |
| **Daily Flexibility** | Daily budget changes stay within a percentage band | 20% |
| **Max CPC** | No bid can exceed your maximum cost-per-click | Set by you |
| **Bid Velocity** | Bids cannot change too fast between cycles | 15% per cycle |
| **Budget Shift Limit** | No single campaign loses more than X% of its budget | 25% |
| **Pause Protection** | Last active ad in a group cannot be paused | Always on |
| **Minimum Data** | Actions require minimum impressions before triggering | 100 impressions |
| **Confidence Threshold** | Statistical confidence must meet threshold | 95% |

If a guardrail blocks a change, Autopilot logs the reason and moves on. No surprises.

---

## Activity Feed

Every action Autopilot takes is recorded with:

- **What changed** (entity, field, old value, new value)
- **Why** (reasoning based on performance data)
- **When** (timestamp)
- **Confidence level** (statistical confidence of the optimization)

The activity feed is accessible from the Autopilot dashboard and included in weekly reports.

---

## Real-Time Alerts

Autopilot monitors for issues and notifies you when attention is needed:

- **Budget pacing** alerts if projected spend will exceed your monthly cap
- **Performance drops** alerts on significant day-over-day CTR declines (>30%)
- **Auto-reverts** alerts when a change is rolled back due to negative impact
- **Sync failures** alerts when changes cannot be pushed to the ad platform
- **Escalations** alerts when optimization has been blocked for an entity

---

## Weekly Reports

Every week, Autopilot generates a performance report containing:

- Week-over-week metrics (clicks, impressions, CTR, CPC, spend)
- Comparison to pre-Autopilot baseline
- Summary of all changes made
- Top improvements with impact metrics
- Concerns and items needing attention
- Budget status (spent, remaining, projected)
- Per-platform performance breakdown
- Focus areas for the coming week

---

## Getting Started

### Step 1: Configure

Choose your optimization mode (Recommend or Auto-Optimize), set your monthly budget cap and max CPC, then select which campaigns Autopilot should manage.

### Step 2: Activate

Autopilot begins its learning phase, collecting 7-14 days of baseline performance data. During this time, no changes are made.

### Step 3: Learning Phase

Watch the learning progress on your dashboard. Autopilot needs enough data points across all selected campaigns to establish reliable baselines.

### Step 4: Active Optimization

Once learning completes, Autopilot begins its optimization cycles. In Recommend mode, check your recommendations regularly. In Auto-Optimize mode, review the activity feed and weekly reports.

### Step 5: Review and Adjust

Use weekly reports to evaluate performance. Adjust guardrails, add or remove campaigns, or switch modes based on results.

---

## FAQ

### Will Autopilot spend more than my budget?

No. The monthly cap guardrail prevents any optimization that would push projected spend over your limit. If pacing is ahead of schedule, Autopilot alerts you.

### Can I override Autopilot's changes?

Yes. Manual changes are always respected. When you make a change via the Budget page or directly in Google Ads, Autopilot sees it as a user preference and factors it into future optimizations.

### What happens if Autopilot makes a bad change?

Autopilot monitors the impact of every change. If performance declines beyond the revert threshold (default 20%) within the revert window (default 48 hours), the change is automatically rolled back and you are notified.

### Does Autopilot work with Smart Bidding?

Yes. Smart Bidding handles auction-level bid adjustments (about 20% of optimization). Autopilot handles the other 80%: budget allocation, ad rotation, keyword management, and audience refinement.

### Can I use Autopilot with both Google Ads and Microsoft Advertising?

Yes. Autopilot manages campaigns across both platforms from a single configuration. Budget allocations respect per-platform splits, and reporting includes per-platform breakdowns.

### What plan do I need for Autopilot?

Autopilot capabilities vary by plan:

| Feature | Starter | Growth | Agency |
|---------|---------|--------|--------|
| Recommend mode | - | Yes | Yes |
| Auto-Optimize mode | - | Yes | Yes |
| Budget guardrails | - | Yes | Yes |
| Weekly reports | - | Yes | Yes |
| Multi-account | - | - | Yes |

---

**Related:**
- [Premium Features](README.md)
- [Performance Dashboard](performance-dashboard.md)
- [Subscription & Billing](subscription.md)
