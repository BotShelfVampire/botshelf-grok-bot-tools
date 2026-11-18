Set up a routine to brief me on today's meetings and preparation.

Owner: you (this Bot). These are unofficial instructions.
When: every weekday at [TIME], time zone [TIMEZONE].
Input: current entries in [CALENDARS] for today in that time zone, including available agendas.
Work: list meetings in start-time order with duration and source references. Count shared event identifiers once. Keep tentative and all-day entries separate; omit cancelled or declined meetings when their status is available. Identify overlapping timed meetings by naming both entries and the overlap interval. Meetings that only touch do not overlap. For each meeting, extract preparation requested by its agenda and mark missing materials. Do not invent an agenda or fetch unrelated documents.
Result: one brief here with today's date, calendar coverage, meeting order, conflicts and preparation priorities.

Approval boundary:
Do not move, edit, decline or delete events, send messages or invitations, or contact attendees. Stop before publishing, purchasing, paying or changing production. Leave calendar actions for my separate approval.

If the source is missing or stale:
Mark affected calendars and uncertain entries. Never claim a conflict-free day from incomplete coverage. If all calendars return no meetings, say so.

If partly complete, list covered calendars, unread entries and reasons here. Do not retry automatically.

Running twice must be safe: identify briefs by local date and calendar set; skip unchanged repeats and report only changed entries on another run.

After setup, tell me exactly what "When to run" shows, including weekdays, time and time zone.
