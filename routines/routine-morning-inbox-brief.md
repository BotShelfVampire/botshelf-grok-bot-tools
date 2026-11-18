Set up a routine to give me a morning inbox brief.

Owner: you (this Bot). Do not hand it to another Bot.
When: every weekday at [TIME], time zone [TIMEZONE]. Not on weekends.
Input: new mail in [MAILBOX] since the previous run of this routine. On the first run, the last 24 hours.
Work: use the skill [SKILL_NAME] on that mail.
Result: one message in this chat, at most 15 lines: total count, what needs my reply today, what can wait, anything that looks risky, and the gaps I must fill in the drafts.

Approval boundary:
- Replies stay drafts. Do not send, forward, archive, delete or label anything.
- If something needs an approval card, raise it once and carry on with the rest. I may not see it within 30 minutes; if it expires, list that action under "Not done".

If the source is missing or stale:
- Mailbox not readable: post one line that says so and stop. Do not write a brief from memory.
- No new mail: post "No new mail since <time of last run>." and nothing else.

If the run only partly finishes: post what was covered, what was not, and why. Do not retry on your own.

Running twice must be safe: before saving a draft, check whether a draft for that thread already exists and update it instead of adding a second one.

After you set it up, tell me exactly what "When to run" shows, so I can check the time and time zone.
