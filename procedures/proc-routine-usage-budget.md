Unofficial checklist: count the runs your routines will make before you add one or raise a frequency.

1. List the routines [BOT_NAME] owns, plus the ones you plan to add. A Bot can own up to 50.
2. For each schedule, work out runs in its busiest hour: 60 divided by [SCHEDULE_MINUTES], rounded up. An interval under five minutes is not allowed.
3. Add the schedules of all your routines for the busiest hour and write the sum as [SCHEDULED_RUNS_PER_HOUR].
4. For each event trigger, count matching events in a busy hour, not an average hour. When one event matches several routines, count each. Write the sum as [PEAK_EVENTS_PER_HOUR].
5. Read every Slack trigger again. "Any message" in a busy channel, or all of Slack, can fire far more often than a mention or a phrase in one channel.
6. Add the two sums and the tests you plan to press. Compare with 300 runs per hour for all routines together.
7. Check each routine alone against 200 runs per hour.
8. Set [WEEKLY_RUN_BUDGET], your own weekly target. Every run consumes usage, and the weekly usage limit is separate from the hourly run limits.
9. Read the run records of the routines you already have. Only the 20 most recent are kept for each, so read them before they roll off.
10. Look for runs that failed with "Automation run rate limit exceeded". Failed runs are not retried automatically. Read what a failed run finished before you run it again by hand.
11. If the plan is over any limit or over your own target, lengthen intervals or narrow the matching rules. Keep the work that must happen.
12. If a count is still unknown, leave the frequency as it is and write the open question down. Counting runs approves nothing: sending, publishing, purchasing, paying, deleting and production changes stay behind approval.
