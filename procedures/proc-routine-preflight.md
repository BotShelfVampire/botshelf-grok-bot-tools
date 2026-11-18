Unofficial checklist: read a routine's settings and run one safe test before you let it run on its own.

1. Click [BOT_NAME] at the top of the chat, open Details, and find [ROUTINE_NAME]. Check that this is the Bot you meant to own the job.
2. If the routine is already switched on and you are not sure of it, pause it while you read.
3. Read "When to run". Compare the days and times with what you asked for. Two runs must be at least five minutes apart.
4. Open Settings, then Bot, and read "Timezone". Check that it is the zone the schedule assumes.
5. For an event trigger, read the matching rule. Check that it names one channel, repository or project, not everything.
6. Read the input in the request. It should name the account or source and how far back to look.
7. Read the result line. It should say where the output goes and where a partial result is reported.
8. Read the approval boundary. It should stop before sending, publishing, purchasing, paying, deleting and changing production. Mail written by a routine stays a draft until you press Send.
9. Read the missing-data rule. It should say what happens when the source is unreadable, empty or old, and it should not fall back on memory.
10. Read the repeat rule. A second run on the same input should not create a second draft or record.
11. Prepare [SAFE_INPUT]. Press Test once. A test does real work, so stay with it.
12. Read the result in the Bot's chat. Look for anything sent, changed or deleted that you did not expect.
13. If an approval card appeared, read it. Cards from background work expire after 30 minutes and the action is then reported as not done.
14. Resume the routine only when every line above matched. Otherwise use Edit, and test again.
