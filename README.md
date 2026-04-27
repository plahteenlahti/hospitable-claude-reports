# Hospitable Claude Reports

This folder contains prompt templates for generating  operations and revenue briefings for a short-term rental host using Hospitable.

The reports are designed to be run on a schedule and read quickly. Each one focuses on what the host needs to know now, what needs attention, and which actions could improve guest experience or revenue.

## Reports

### Daily ops briefing

File: `daily-review.md`

A short morning briefing for the day ahead. It highlights today’s check-ins, checkouts, same-day turnovers, open guest issues, repeat guest patterns, and any useful local context.

Use it when the host needs a quick 90-second view of the day.

### Weekly outlook

File: `weekly-review.md`

A Monday morning view of the next seven days. It summarizes occupancy, upcoming arrivals and departures, pricing or availability anomalies, gap nights, unanswered reviews, and recent review themes.

Use it to plan the week and catch small issues before they become operational problems.

### Monthly review and 3-month profit outlook

File: `monthly-review.md`

A monthly revenue and operations review. It looks back at the previous month, compares performance year over year when possible, and produces a forward-looking 90-day plan focused on profit opportunities.

Use it at the start of each month to review revenue, occupancy, ADR, RevPAR, booking pace, high-demand windows, review backlog, and pricing actions.

## Shared principles

All reports follow the same basic rules:

- Filter out cancelled reservations.
- Keep the output brief and useful.
- Skip empty sections.
- Never invent missing information.
- Surface only the issues that need attention.
- Use specific details like guest names, dates, times, platforms, nights, and properties when available.
- Write only the final briefing markdown, with no preamble or closing note.

## Hospitable tools used

The reports rely on Hospitable MCP tools such as:

- `list_properties`
- `get_upcoming_checkins`
- `get_upcoming_checkouts`
- `list_reservations`
- `get_calendar`
- `list_reviews`
- `list_messages`

Each report lists the tools it needs and explains when to use them.

## Local market context

The monthly and daily reports include Finnish demand signals where relevant. These include events and seasonal patterns such as Vappu, Juhannus, Helsinki Pride, Flow Festival, Pori Jazz, Suomi-Areena, and the Yyteri summer season.

This helps the host spot pricing opportunities and avoid treating high-demand or low-demand periods like ordinary dates.

## Intended workflow

Run the reports on this cadence:

- Daily report every morning.
- Weekly outlook every Monday at 07:00.
- Monthly review on the 1st of each month at 07:00.

Together, these reports give the host a practical operating rhythm: handle today, plan the week, and improve the next 90 days.

# Example outputs
 
Real briefings produced by the prompts in this repo, generated against a live two-property Hospitable account.
 
---
 
## Daily briefing — Sun 26 Apr 2026
 
### Today
 
**Pori — same-day turnover** (cleaning window: 12:00–16:00, 4 hours)
- 12:00 — Vanessa K. checks out, 4 nights via Booking.com
  - ⚠️ Open issue: "Incorrect WiFi password" — check the sticker / welcome card and follow up in the thread before next guest arrives
- 16:00 — Adriana A. checks in, 4 nights via Airbnb, solo, from Romania
  - Language: convo is English, but guest's native language is Romanian. Phone is +358 (likely already in Finland).
**Kamppi**
- Daniel I. mid-stay (long booking, 11 nights, checks out Thu 30 Apr). No arrivals or departures today.
### This week
 
**Thu 30 Apr — heaviest day**, both properties turn over.
- Pori: Adriana out 12:00 → Helle A. (Booking, Estonia) in 16:00 — 4-hr clean
- Kamppi: Daniel out 12:00 → gap night, no arrival until Friday
**Fri 1 May — Vappu (Finnish May Day)**
- Kamppi: Monica R. in 16:00, 5 nights via Airbnb. Kamppi sits in the middle of the Vappu celebrations — proactive note about noise might be smart.
- Pori: Helle continues.
### Flags
 
- **Repeat-guest pattern**: Monica R. had a Kamppi booking cancelled minutes after booking on 19 Mar, then rebooked 1–6 May. Glance at her conversation thread before arrival.
- **Open issue ticket** on Vanessa @ Pori is still listed as "Incorrect WiFi password" — should be resolved/marked handled, otherwise it'll keep showing up here.
- **Two same-day turnovers this week** (today + Thu), both at Pori.
### Cleaner handoff — Pori, today
 
> Hei Tiina,
>
> Pori today: Vanessa out 12:00, Adriana in 16:00 (4-hr turn). Adriana on solo guest Romaniasta, 4 yötä.
>
> Edellinen vieras raportoi WiFi-salasanaongelmasta — voitko tarkistaa että lapun salasana täsmää reitittimen kanssa kun olet siellä? Kiitos!
 
---
 
## Weekly outlook — Mon 27 Apr → Sun 3 May 2026
 
### The week at a glance
 
- **Kamppi**: 6/7 nights booked (86%) — Daniel I. mid-stay through Wed, gap Thu, Monica R. in Fri for Vappu
- **Pori**: 7/7 nights booked (100%) — Adriana A. through Wed, Helle A. from Thu (same-day turnover Thu)
### Schedule
 
**Thu 30 Apr — heavy day**
- Pori: Adriana A. out 12:00 → Helle A. in 16:00 — 4-hr clean ⚠️
- Kamppi: Daniel I. out 12:00 → no arrival, gap Thu night
**Fri 1 May — Vappu (Finnish May Day)**
- Kamppi: Monica R. in 16:00, 5 nights via Airbnb. Repeat-booker pattern (cancelled previous Kamppi booking, rebooked) — worth a glance at the thread before arrival.
### Flags
 
- **Single gap night at Kamppi** (Thu 30 Apr) — too late to fill 3 days out. Priced at €58 (weekday standard) — flag for similar future Thu→Fri gaps where a 1-night allowance + €5 discount might pick up Vappu travelers arriving early.
- **Open issue ticket** on previous Pori stay ("Incorrect WiFi password") still listed as unresolved — should be cleared or it'll keep appearing on daily briefings.
- **Review backlog**: 2 new 5★ reviews this week, both unanswered (Kamppi 19 Apr "great location"; Pori 22 Apr). Total backlog 93 across both properties.
### Recent reviews
 
Two 5★ reviews landed this week, both Finnish-language with similar themes — location and quiet building (Pori), location and ease of communication (Kamppi). No themes to act on; both worth a brief reply to keep the response rate clean.
 
---
 
## Monthly review + 3-month outlook — March 2026
 
> _This run was on 26 Apr (not the 1st). "Month just ended" is treated as March 2026; "next 3 months" covers May–July 2026._
 
### Headlines
 
| Property | Revenue | Occupancy | ADR | RevPAR | YoY |
|---|---|---|---|---|---|
| Kamppi | €893.64 | 48.4% | €59.58 | €28.83 | no YoY baseline yet |
| Pori | €462.86 | 35.5% | €42.08 | €14.93 | no YoY baseline yet |
 
Both properties softened sharply MoM — Kamppi revenue down ~26% from Feb (€1,200 / 19 nights / 68% occ), Pori down ~35% (€716 / 17 nights / 61% occ). Pori dropped from 6 short stays in February to 3 in March on roughly the same nightly rate band.
 
### What happened — March
 
All six March bookings were Airbnb — no Booking.com or direct mix this month. All accepted, none cancelled, no issue alerts. Pace skewed mid-month: Kamppi ran nearly continuous 10–27 March (three back-to-back stays totaling 15 nights, including a 7-night booking from Jack T. at €342 and a high-rate 4-night stay from Fu M. at €307). Pori had longer gaps with stays on 12–16, 24–27, and a 31 Mar – 4 Apr that bled into April. Pori's nightly rate band of €29–38 was consistent with February's; the volume drop looks like a weekday visibility / conversion issue rather than pricing alone.
 
### On the books — next 3 months
 
| Month | Kamppi | Pori | High-demand windows |
|---|---|---|---|
| May 2026 | 20/31 (65%) | 6/31 (19%) | Vappu (1 May), Pori Folk Festival (mid-May) |
| June 2026 | 8/30 (27%) | 2/30 (7%) | Helsinki Day (12 Jun), Juhannus (late Jun) |
| July 2026 | 3/31 (10%) | 0/31 (0%) | **Pori Jazz** (~11–19 Jul), Suomi-Areena |
 
Kamppi's May pickup is healthy; June and July are tracking light but still inside normal STR lead-time. Pori is the urgent one — May is half-empty 5 weeks out, July is fully empty 11 weeks out, and Pori's biggest demand window of the year (Jazz) is currently priced at the standard €50 flat with no min-stay uplift.
 
### Profit opportunities (next 90 days)
 
#### 1. Price up Pori for Pori Jazz week — €600–900, high
**Property:** Pori · **Dates:** 11–19 July · **Lever:** pricing + min-stay
 
Currently priced at €50/night with 2-night min-stay — same as any other week. Pori Jazz drives the largest demand spike of Pori's year; comparable listings typically command 1.8–2.2× normal rates and lift min-stays to 3–4 nights. Recommend €95/night with a 3-night min-stay across 10–20 July. At 80% pickup over 9 nights that's ~€684 vs. a full-priced lock-in of ~€450; the spread is the opportunity. Set this now while festival travelers are still booking.
 
#### 2. Open the back half of May at Pori — €450–675, med
**Property:** Pori · **Dates:** 17–31 May · **Lever:** min-stay + light discount
 
15 unbooked nights at €50 with a 2-night minimum, no Sun–Wed dip. Drop min-stay to 1 night for 17–28 May and test €45 on Sun–Wed nights. At a conservative 50% pickup that's €450–675 of recoverable revenue. At current pace this month is heading sub-25% occupancy.
 
#### 3. Verify and reclaim stale Kamppi blocks — €250, high
**Property:** Kamppi · **Dates:** 12–14 May, 25 May · **Lever:** block-clear
 
Three mid-week singletons / pairs blocked with no surrounding context — at Kamppi's mid-May rates of €55–73, that's ~€250 of potentially recoverable revenue if these are stale rather than intentional owner stays. Confirm and unblock anything that isn't actually claimed.
 
#### 4. Add weekend uplift to Pori — €100–150/month, low
**Property:** Pori · **Dates:** Fri/Sat across May–June · **Lever:** pricing
 
Pori is priced flat at €50 across all days of the week. Test a €5–10 Fri/Sat uplift across May and June. Low confidence on impact (small sample), but it's a one-click change and the standard seasonality argument applies.
 
### Review action queue (top 3 to respond to this week)
 
1. **Pori** · 19 Apr · 4★ · _Anon._ · "Sijainti erinomainen. Hiljainen taloyhtiö."
2. **Kamppi** · 14 Mar · 5★ · _Spanish guest_ · positive — quick public reply to keep response rate up
3. **Pori** · 22 Apr · 5★ · _Anon._ · positive — same as above
Backlog is 93 across both properties going back to 2024; clearing the recent and lowest-rated first compounds best for response-rate signaling on both platforms.
 
### Maintenance items
 
- Confirm whether the Pori 7–16 May block (10 nights) is the intended owner stay
- Resolve the open "Incorrect WiFi password" issue ticket on Pori (still listed as unresolved on the daily briefing)
- Investigate Pori weekday softness in Airbnb Insights — Feb at 60.7% occupancy on 6 short stays, March at 35.5% on 3, similar pricing — likely a discovery / discount-structure issue worth probing before the May/June pace settles
