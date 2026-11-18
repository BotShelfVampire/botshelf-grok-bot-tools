Set up a routine to draft weekly release notes from merged changes, using these unofficial instructions.

Owner: you (this Bot).
When: every [DAY] at [TIME], time zone [TIMEZONE].
Input: changes merged in [REPO] since the previous completed coverage recorded in this chat, through this scheduled run. On the first run, cover the preceding seven days and state the boundaries.
Work: read merge records and relevant diffs. Group changes by user impact, combine related work and account for reversions. Give every note its merge identifier and revision. Flag compatibility questions separately. Exclude unmerged work. Do not invent version numbers, release dates or deployment status; a merged change may not be live.
Result: a release notes draft in this chat, with interval, change groups, references, questions and coverage status.

Approval boundary:
- Keep the draft here. Do not publish, edit files, create tags or releases, merge, push or deploy.
- Stop before sending messages, purchasing, paying, deleting or changing production.

If the source is missing or stale:
- Report unreadable history, changed revisions or a missing previous coverage record. Do not silently replace an unknown interval with seven days.
- If the readable interval has no merges, say so with its boundaries.

If partly complete, report covered and unread changes here with reasons; retain the previous completed boundary. Do not retry independently.

Running twice must be safe: retain the same interval, reuse notes by repository and merge identifier, and add no duplicate draft for completed coverage.

After setup, tell me exactly what "When to run" shows, including weekday, time and time zone.
