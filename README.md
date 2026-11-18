# Grok Bot tools (unofficial)

40 texts to copy into **Grok Bot** or **Grok Build**: 16 skills in `SKILL.md` form, 10 routine briefs, 8 Bot setup sheets and 6 checklists.
Each one says what it does, where it goes, where it stops, and which blanks to fill.

> **Unofficial.** Made by [BotShelf Vampire](https://botshelfvampire.com/), an independent shelf. xAI did not write, review or approve anything here.
> **Untested.** The texts were prepared from the public xAI documentation (read on 2026-11-18). Nobody at BotShelf Vampire has recorded a run on a real account. Read a text before you use it.

[日本語の説明](README.ja.md) · Web version with search: https://botshelfvampire.com/grok-bot/tools/

## How to use them

| Kind | Where it goes |
| --- | --- |
| Skill | **Grok Build:** copy `skills/<name>/` into `.grok/skills/` in a repository (or `~/.grok/skills/`); it becomes `/<name>`. **Grok Bot:** the official pages describe no file upload for skills, so paste the text into a chat with the Bot and ask it to save it as a skill by that name, then check it under *Connect apps* → *Private skills*. |
| Routine brief | Send it as a message to the Bot that should own the job. Read *When to run*, then press *Test* once with safe input. |
| Bot setup sheet | Create a Bot and send the sheet as the first message. Lasting rules go into the Bot's memory when you ask it to remember them. |
| Checklist | For you, the person. Work through it with the app open. |

Fill every `[BLANK]` before you use a text. Each text stops before sending, publishing, purchasing, paying, deleting or changing production. Leave those lines in.

## What these add to the official pages

The official pages explain the features and list what a good skill or routine request should contain. These texts are the worked-out versions:
every skill fills all six parts the documentation names (when to use, inputs and access, steps, checks, what to return, what needs approval),
every routine brief states each point the documentation says to confirm, and all of them say what to do when data is missing or old,
how a half-finished run is reported, and how a second run stays harmless. The limits quoted in the texts are the documented ones as of 2026-11-18.

## Contents

### Skills (`skills/<name>/SKILL.md`)

| Item | Runs on | What it does, and where it stops |
| --- | --- | --- |
| [A brief with a source for every claim](skills/source-checked-brief/SKILL.md) | Grok Bot | Answers a question from named sources, attaches a source to every claim and marks unsupported claims. Stops at a draft without publishing or sending it. |
| [Calendar conflicts, proposed moves only](skills/calendar-conflict-sweep/SKILL.md) | Grok Bot | Finds overlapping events and days above your stated meeting limit, then proposes moves. It stops before moving or declining events or sending invitations. |
| [Dependency update order, plan only](skills/dependency-update-plan/SKILL.md) | Grok Build | Lists dependencies with evidence of newer versions, reads available changelogs, and orders proposed updates with risks. Stops at a plan; no installs or repository edits without approval. |
| [Document freshness check, proposed edits only](skills/doc-freshness-check/SKILL.md) | Grok Bot | Checks document dates, versions, prices and owners against named current sources, then lists proposed edits. Stops before editing, sending or publishing any document. |
| [Failing test triage, proposed diff only](skills/failing-test-triage/SKILL.md) | Grok Build | Runs the named failing tests, traces the first supported cause, and proposes a small diff. Stops before applying it, weakening tests, committing or pushing. |
| [First incident notes, no production changes](skills/incident-first-notes/SKILL.md) | Grok Bot | Turns an alert or error event into draft incident notes with known facts, a sourced timeline, unknowns and suggested checks. Stops before production changes, paging or sending updates. |
| [Inbox triage, drafts only](skills/inbox-triage-drafts/SKILL.md) | Grok Bot | Sorts new mail into four piles, drafts replies for the pile that needs one, and stops. It never sends, archives or deletes. |
| [Meeting notes into decisions and actions](skills/meeting-notes-to-actions/SKILL.md) | Grok Bot | Turns meeting notes into decisions, actions and open questions. Owners and dates appear only when stated. Stops before sending notes or creating tasks. |
| [PR review notes, no posted comments](skills/pr-review-notes/SKILL.md) | Grok Build | Reviews a repository diff or branch for correctness risks, missing tests and unclear names. Returns findings with file and line, then stops before commits, pushes, merges or comment posting. |
| [Receipt reconciliation, report only](skills/receipt-reconcile/SKILL.md) | Grok Bot | Matches receipts to a statement export and lists matches, mismatches and missing receipts. It stops at a report and never pays, files or submits an expense claim. |
| [Release notes from commits, draft file only](skills/release-notes-from-commits/SKILL.md) | Grok Build | Reads a repository commit range, groups changes and flags possible breaking changes. Writes one draft file and stops before tagging, committing or publishing. |
| [Renewal price check, questions only](skills/renewal-price-check/SKILL.md) | Grok Bot | Reads the current renewal price, compares it with the last payment, and drafts questions for the vendor. It stops before contacting the vendor, renewing, cancelling or buying. |
| [Review a draft skill before saving](skills/review-a-draft-skill/SKILL.md) | Grok Bot | Reviews a draft skill against six required parts and adds decision rules, failure handling and approval boundaries. Returns revised text and stops before overwriting a saved skill. |
| [Support tickets, sorted with reply drafts](skills/support-ticket-sort/SKILL.md) | Grok Bot | Sorts new support tickets by urgency and type, explains each choice, and drafts first replies. Stops before sending, closing tickets or issuing refunds. |
| [Task handoff note, ready for review](skills/handoff-note/SKILL.md) | Grok Bot | Writes a handoff note with the current state, completed work, open work, locations, next step and pending approvals. Stops before sending it or taking the next action. |
| [Weekly status digest, draft only](skills/weekly-status-digest/SKILL.md) | Grok Bot | Collects the week's work from a work log and named sources into a digest with completed work, blockers and next steps. It stops at a draft and never sends it. |

### Routine briefs (`routines/`)

| Item | Runs on | What it does, and where it stops |
| --- | --- | --- |
| [First notes for a new incident](routines/routine-sentry-new-issue-notes.md) | Grok Bot | Writes first incident notes for a new Sentry issue in one project at the chosen severity or above. It leaves checks as proposals, pages nobody and makes no production changes. |
| [Friday weekly status digest](routines/routine-weekly-status-friday.md) | Grok Bot | Runs a saved status skill every Friday and puts a weekly digest in the Bot's chat. Follow-ups stay drafts; nothing is sent elsewhere or changed in production. |
| [Monthly document freshness review](routines/routine-doc-freshness-monthly.md) | Grok Bot | Reviews a document set each month and lists proposed edits with their evidence in the Bot's chat. It stops before editing, commenting, sending notifications or publishing. |
| [Monthly renewal watch, questions only](routines/routine-renewal-watch-monthly.md) | Grok Bot | Checks upcoming renewals each month, looks prices up again and drafts questions in the Bot's chat. It stops before renewing, cancelling, paying or sending questions. |
| [New pull request review notes](routines/routine-github-pr-review-notes.md) | Grok Bot | Writes review notes in the Bot's chat when a pull request opens in one repository against one base branch. It posts no GitHub comments, changes no files and never merges. |
| [Receipt emails into an expense list](routines/routine-email-receipt-filing.md) | Grok Bot | Extracts vendor, date, amount and currency from matching receipt emails to the Bot and adds them to a list. It stops before paying, submitting expenses or sending mail. |
| [Slack mentions into a request list](routines/routine-slack-mention-intake.md) | Grok Bot | Records requests when this Bot is mentioned in one Slack channel and explains its understanding in Bot chat. It stops before posting to Slack or acting on the request. |
| [Webhook form intake with field checks](routines/routine-webhook-form-intake.md) | Grok Bot | Checks webhook form data and adds one normalized record to the chosen intake list. It rejects malformed input and stops before sending, publishing or changing production. |
| [Weekday morning inbox brief](routines/routine-morning-inbox-brief.md) | Grok Bot | Asks a Bot to run an inbox triage every weekday morning and post one short brief in its chat. Replies stay drafts. |
| [Weekly routine usage review](routines/routine-usage-review-weekly.md) | Grok Bot | Reviews this Bot's recent routine runs, failures and empty results, then proposes changes in chat. It stops before pausing, editing, deleting, running Test or sending notifications. |

### Bot setup sheets (`bots/`)

| Item | Runs on | What it does, and where it stops |
| --- | --- | --- |
| [Custom Rules for draft preparation](bots/bot-custom-rules-starter.md) | Grok Bot | Provides seven Ask first rules and three narrow Allow automatically rules. Sending, publishing, purchases, payments, deletion and production changes stop for approval. |
| [Expense desk, receipts to drafts](bots/bot-expenses-desk.md) | Grok Bot | Sets one Bot to organize receipts and prepare expense summaries. It stops at drafts and never purchases, pays or submits claims. |
| [Inbox desk, triage and reply drafts](bots/bot-inbox-desk.md) | Grok Bot | Sets one Bot to sort mail and prepare reply drafts from current threads. It stops before sending and asks first before archiving, deleting or replacing drafts. |
| [One job for a new Bot](bots/bot-one-job-starter.md) | Grok Bot | Sets one job, remembered rules, sources and approval boundaries for a new Bot. It stops at a proposed action before sending, publishing, paying, deleting or changing production. |
| [Primary Bot, offers before action](bots/bot-primary-brief.md) | Grok Bot | Gives the primary Bot one coordination job, a roster and quiet hours. It proposes work first and waits for a yes before acting, including creating Bots or sending anything. |
| [Release desk, preparation notes only](bots/bot-release-desk.md) | Grok Bot | Sets up a Bot to draft release changes, risks and a checklist from repository records. It stops at preparation notes and never tags, deploys or merges. |
| [Research desk, briefs with sources](bots/bot-research-desk.md) | Grok Bot | Sets up a Bot to compare sources, draft research briefs and mark unsupported claims as unverified. It stops at a brief in chat and never publishes. |
| [Team support desk, drafts only](bots/bot-team-support-desk.md) | Grok Bot | Sets one shared support job, lists what teammates can access, and prepares triage notes and reply drafts. It stops before sending, closing tickets or publishing the Bot. |

### Checklists (`procedures/`)

| Item | Runs on | What it does, and where it stops |
| --- | --- | --- |
| [Build a deep link with an unsent message](procedures/proc-deep-link-builder.md) | Grok Bot | Guides you through a Bot id, short message, URL encoding and an opening check. Stops with the message unsent and the link unpublished. |
| [Check a Bot before sharing](procedures/proc-share-scrub.md) | Grok Bot | Checks a Bot’s sharing material and team access for private information. Stops before sharing, publishing, sending, payment, deletion or production changes. |
| [Check a webhook routine before use](procedures/proc-webhook-trigger-check.md) | Grok Bot | Walks through a safe webhook request and its run result. Stops before downstream messages, publishing, payments, deletion or production changes. |
| [Plan a routine usage budget](procedures/proc-routine-usage-budget.md) | Grok Bot | Estimates scheduled and event-driven runs against documented limits. Stops before increasing activity with unknown counts or allowing sending, publishing, payments, deletion or production changes. |
| [Review a skill learned from a demonstration](procedures/proc-taught-skill-hardening.md) | Grok Bot | Turns a demonstrated workflow draft into instructions with decision rules, failure handling and a safe example. Stops before sending, publishing, payment, deletion or production changes. |
| [Routine preflight before it runs alone](procedures/proc-routine-preflight.md) | Grok Bot | Checks a routine before a safe Test and resuming scheduled work. Stops on unresolved checks or any action that would send, publish, pay, delete or change production. |

`index.json` lists every item with its stops, first three moves, blanks and sources.

## License and sources

MIT, see [LICENSE](LICENSE). Sources: [SOURCES.md](SOURCES.md). Other people's shared Bots are not copied here.

## Problems and results

If a text does not behave as it says, open an issue with the item name, what you ran it on, and what happened (leave out private data).
"Grok" and "Grok Bot" are names of xAI products; they are used here only to say what the texts are for.
