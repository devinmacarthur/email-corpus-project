# Email Management Strategy — Recommendations

*Generated from analysis of 43,035 unique messages (Nov 2023 – Feb 2026)*
*Includes linguistic pattern analysis of 29,095 human-written messages*

---

## The Problem

The Executive Director's inbox processes **~58 messages/day** (median 54, spikes to 100+ on busy days). Based on message classification and handling time estimates:

- **12.9 hours/week** spent on email (~32% of the work day)
- **73.8%** of messages are human-written and potentially actionable
- **25.3%** are noise (automated, newsletters, sync artifacts, junk)
- **46.2%** of all traffic is internal (oregoned.org + nea.org)
- **Median reply time: 2.5 hours** — P90 is 3.3 days (some threads go cold)

The real burden isn't spam or newsletters — it's the **31,748 human messages** requiring read + decide + act.

### What the Human Messages Actually Look Like

Linguistic analysis of 29,095 human-written messages reveals distinct communication patterns:

| Communication Type | Volume | Daily Avg | % of Human Mail |
|-------------------|--------|-----------|-----------------|
| Uncategorized (complex/mixed intent) | 14,391 | 19.4 | 49.5% |
| Escalation / urgent | 4,609 | 6.2 | 15.8% |
| Action requests ("please review/approve/send") | 4,347 | 5.9 | 14.9% |
| Scheduling (meetings, availability) | 2,639 | 3.6 | 9.1% |
| Acknowledgments ("thanks, got it, will do") | 2,481 | 3.4 | 8.5% |
| FYI / informational (no action needed) | 2,398 | 3.2 | 8.2% |
| Follow-ups ("checking in, circling back") | 835 | 1.1 | 2.9% |
| Decision requests ("need your approval") | 373 | 0.5 | 1.3% |
| Delegation ("can you take the lead on") | 212 | 0.3 | 0.7% |
| Status updates / reports | 144 | 0.2 | 0.5% |

**Key structural findings:**
- **37% are medium-length** (150-400 words), **34% are long** (400-800 words) — this is a text-heavy inbox
- **44% contain at least one question** — many are multi-question messages (5% have 4+ questions)
- **36% open with a greeting** but only **3.5% have formal sign-offs** — fast informal communication culture
- **12.5% reference attachments** — significant attachment-heavy workflow
- **82% of acknowledgments are replies** (not originals) — most "thanks" messages are responses
- **62% of action requests appear in reply chains** — requests often emerge mid-thread, not as fresh messages
- **Sent items skew heavily toward escalation** (1,900 sent) — the ED sends urgent/time-sensitive messages more than any other type

---

## Tier 1: Quick Wins (Outlook Rules — Free, 1-2 hours to set up)

**Impact: Removes ~15 messages/day from inbox view**

These items hit the inbox but require no decision-making. Outlook rules can file them automatically:

| Rule | Auto-file to folder | Est. messages/day |
|------|---------------------|-------------------|
| Concur expense reminders | `Auto/Concur` | 1.5 |
| Daily AC-PM Counts Report | `Auto/Reports` | 1.0 |
| Signature requests (AdobeSign) | `Auto/Signatures` | 1.0 |
| Sync Issues folder noise | (already filed) | — |
| Calendar notifications (no subject) | `Auto/Calendar` | — |
| Read receipts / delivery notifications | Delete | 0.5 |
| Washington Post articles | `Reading/WashPost` | 0.8 |
| Democracy Docket | `Reading/DemDocket` | 0.7 |
| Medium / Substack digests | `Reading/Newsletters` | 0.5 |
| MasterClass emails | `Reading/MasterClass` | 0.2 |
| City Club of Portland | `Reading/CityClub` | 0.1 |

**Setup:** Create 10-12 Outlook rules based on sender address or subject keywords. Takes ~1-2 hours once. No ongoing maintenance.

---

## Tier 2: Copilot for Microsoft 365

**Impact: Saves ~2-3 hours/week on human message processing**

Copilot's strongest features for this inbox profile:

### High-Value Features
1. **Summarize long threads** — The governance, budget, and legal threads often run 10+ messages. Copilot can surface the latest status in one paragraph instead of reading the full chain.

2. **Draft routine replies** — Many internal messages are acknowledgments, meeting confirmations, or info-forwarding. Copilot can draft these for quick review-and-send.

3. **Prioritize inbox** — Copilot can flag messages from key senders (board members, legal counsel at stoel.com/mbjlaw.com, NEA leadership) and deprioritize bulk internal announcements.

4. **Meeting prep summaries** — Before board meetings or RA sessions, Copilot can pull together all related email threads from the past week.

### Moderate-Value Features
5. **Search across threads** — "Find the latest email from Stoel about the grievance" is faster than manual search in a high-volume inbox.

6. **Catch-up after absence** — "Summarize what I missed since Friday" across 200+ weekend messages.

### Limitations for This Use Case
- Copilot **cannot** auto-file or create rules (must be done manually)
- Copilot responses stay within the M365 ecosystem — no integration with external tools
- Requires M365 Copilot license ($30/user/month)

---

## Tier 3: Custom AI Tooling (If Copilot isn't sufficient)

**Impact: Could reduce email time by 30-40% with tailored automation**

These are custom solutions built on the data patterns we've identified:

### Option A: Weekly Email Digest Generator
Build a script that produces a weekly summary:
- New messages by topic (budget, legal, legislative, governance)
- Threads awaiting reply (>48h without response)
- Action items extracted from message subjects
- Volume trends vs. previous week

**Effort:** 2-3 days to build. Runs automatically.

### Option B: Smart Triage Dashboard
A simple web dashboard showing:
- Today's messages sorted by priority (key senders first, noise last)
- One-click actions: Reply, Forward, File, Flag
- Topic tags auto-applied from subject analysis
- "Needs response" queue (messages from key contacts with no reply after 24h)

**Effort:** 1-2 weeks. Requires ongoing maintenance.

### Option C: Hybrid Approach (Recommended if going custom)
Combine the Outlook rules (Tier 1) with a **daily briefing email** sent at 7am:
- Yesterday's message count and top senders
- Threads that went unanswered
- This week's email volume trend
- Flagged items from key sender domains (stoel.com, mbjlaw.com, aflcio.org)

**Effort:** 3-5 days. Low maintenance.

---

## Template & Quick-Response Opportunities

**Estimated savings: ~4 hours/week (215 hours/year)**

Linguistic analysis identified 8 high-volume communication patterns where templates or AI-assisted drafting could dramatically reduce handling time:

### 1. Action Request Response (~6/day, saves 72h/year)
Incoming requests to review, approve, sign, or send something. These follow a predictable pattern: someone asks the ED to do X by Y.

**Template:** *"Thanks for sending. I'll [review/approve/complete] by [DATE]. Please [send any additional context / coordinate with NAME]."*

**Copilot use:** Extract the specific action requested and deadline, auto-draft a confirmation or delegation reply.

### 2. Meeting Scheduling (~3.6/day, saves 66h/year)
Availability requests and meeting coordination. Over half occur within reply chains (51%).

**Template:** *"I'm available [TIMES]. [NAME] will send a calendar invite. / Let's use [SCHEDULING TOOL] to find a time."*

**Copilot use:** Check calendar, draft availability reply with open time slots. This is Copilot's strongest use case.

### 3. FYI Handling (~3.2/day, saves 29h/year)
Messages explicitly marked as informational — "for your awareness," "just sharing," "no action needed."

**Action:** Auto-file to a `Reading/FYI` folder. Include in a weekly digest rather than reading each one in real-time.

### 4. Quick Acknowledgment (~3.4/day, saves 21h/year)
Simple replies: "Thanks," "Got it," "Will do," "Sounds good." These are **82% reply messages** — the ED is confirming receipt.

**Template:** One-click acknowledgment buttons: `✓ Got it` | `✓ Will review` | `✓ Thanks, will follow up by [DATE]`

**Copilot use:** Auto-draft a contextual acknowledgment based on what was sent.

### 5. Follow-Up (~1.1/day, saves 13h/year)
"Circling back," "checking in," "any update?" messages. Two-thirds are replies in existing threads.

**Template:** *"Following up on my [DATE] message about [TOPIC]. Could you provide an update by [DATE]?"*

### 6. Decision Request (~0.5/day, saves 6h/year)
Messages requiring approval or sign-off. These are **high-value, low-volume** — every one matters.

**Action:** Flag in priority inbox. Don't template the response, but ensure these never get buried.

### 7. Delegation (~0.3/day, saves 5h/year)
Assigning ownership of tasks or projects.

**Template:** *"I'd like you to take the lead on [TASK]. Context: [SUMMARY]. Please [report back by DATE / loop in NAME]."*

### 8. Status Update (~0.2/day, saves 3h/year)
Incoming reports and progress updates.

**Action:** Auto-tag with topic keywords. Summarize for board prep and governance review.

### Pattern Insight: The Escalation Signature

The ED's **sent email** is dominated by escalation-type messages (1,900 sent vs. 2,709 received). This suggests the ED's primary email function is **pushing urgency through the organization** — forwarding with "please handle ASAP," flagging deadlines, escalating blocked items.

This is the communication pattern where AI assistance has the **least** value (urgency requires human judgment) but where **better upstream systems** (task tracking, deadline dashboards, automated reminders) could reduce the need to escalate by email in the first place.

---

## Recommended Implementation Roadmap

### Week 1: Foundation
- [ ] Set up 10-12 Outlook auto-filing rules (Tier 1)
- [ ] Measure: count inbox messages before/after rules are active for one week
- [ ] Estimate: should see ~15 fewer messages/day hitting inbox

### Week 2-3: Evaluate Copilot
- [ ] Enable Copilot trial if available on the M365 plan
- [ ] Test: thread summarization on 5 governance/budget threads
- [ ] Test: draft replies for 10 routine internal messages
- [ ] Test: "What did I miss since Friday" catch-up
- [ ] Assess: does it save meaningful time vs. manual handling?

### Week 4: Decide on Tier 3
- [ ] If Copilot is sufficient → stop here, monitor
- [ ] If gaps remain → build the daily briefing email (Option C)
- [ ] If more needed → scope the triage dashboard (Option B)

### Ongoing
- [ ] Review Outlook rules monthly (are new noise sources appearing?)
- [ ] Track email hours/week quarterly (is the trend improving?)

---

## Key Data Points for Decision-Making

| Metric | Value |
|--------|-------|
| Total unique messages analyzed | 43,035 |
| Human messages linguistically analyzed | 29,095 |
| Date range | Nov 2023 – Feb 2026 |
| Average messages/day | 58 |
| Median messages/day | 54 |
| Peak day | 1,756 messages |
| Current email hours/week | 12.9h |
| % of work day on email | 32% |
| Human (actionable) messages | 73.8% |
| Auto-fileable noise | 25.3% |
| Internal traffic | 46.2% |
| Top sender domain | oregoned.org (16,043 msgs) |
| Median reply time | 2.5 hours |
| Unique sender domains | 805 |
| Template savings potential | ~4.1h/week (215h/year) |
| Messages with questions | 44.2% |
| Messages referencing attachments | 12.5% |
| Medium-to-long messages (150+ words) | 71.1% |

---

## Combined Savings Estimate

| Strategy | Hours/Week Saved |
|----------|-----------------|
| Tier 1: Outlook rules (auto-file noise) | 0.4h |
| Tier 2: Copilot (thread summaries, draft replies) | 2-3h |
| Templates & quick-response patterns | 2-4h |
| **Total potential reduction** | **~5-7h/week** |
| **From 12.9h → ~6-8h/week** | **38-54% reduction** |

---

## Files Produced

All analysis data is in `data/reports/`:
- `corpus_stats.json` — Raw corpus statistics (Layer 3, safe to share)
- `pattern_analysis.json` — Classification, time patterns, topics, network
- `workload_model.json` — Workload estimates and reduction scenarios
- `linguistic_analysis.json` — Communication intent, structure, and template opportunities
- `strategy_recommendations.md` — This document
