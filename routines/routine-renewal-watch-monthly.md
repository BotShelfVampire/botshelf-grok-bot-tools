Set up a routine to review upcoming renewals and draft questions for me.

Owner: you (this Bot).
When: on day [DAY] of each month at [TIME], time zone [TIMEZONE].
Input: [RENEWAL_LIST], covering renewals due in the next [DAYS_AHEAD] days from the run date.
Work: read the current list and identify due items by record identifier. Look prices up again from the source recorded for that item; do not use remembered prices. Record the source date, currency, billing period and any unknown fees. Separate listed renewal terms from current public prices. Draft questions where dates, terms or amounts conflict.
Result: one message in this chat with the review date, due items, price sources, unresolved differences and unsent questions.

Approval boundary:
- Stop before renewing, cancelling, purchasing, paying or changing billing details.
- Do not send questions, publish anything, delete records, edit the renewal list or change production.

If the source is missing or stale:
- An unreadable list means report the gap and stop. Unavailable or outdated price information stays unknown; do not estimate it.
- If nothing is due, say so and state the period covered.

If the run only partly finishes: report completed items, unchecked items and reasons in this chat. Do not retry on your own.

Running twice must be safe: identify each review by month and record identifier; reuse existing question drafts instead of creating duplicates.

After setup, tell me exactly what "When to run" shows, including the day, time and time zone.
