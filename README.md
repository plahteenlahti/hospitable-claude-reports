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