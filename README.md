# Grok Bot tools (unofficial)

71 texts to copy into **Grok Bot** or **Grok Build**: 28 skills in `SKILL.md` form, 18 routine briefs, 14 Bot setup sheets and 11 checklists.
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
| [Changed paths and the tests they still need](skills/test-gap-list/SKILL.md) | Grok Build | Maps changed code paths to existing tests, lists gaps with search evidence, and proposes one first test per gap. Stops before writing files, committing or pushing. |
| [Changelog entry check, findings only](skills/changelog-entry-check/SKILL.md) | Grok Build | Compares an existing changelog entry with the diff, lists missing or overstated details, and stops before file edits, commits, pushes or tags. |
| [Contract dates and terms, quoted clauses only](skills/contract-date-list/SKILL.md) | Grok Bot | Lists dates, notice periods and renewal terms from supplied contract text, with a clause quote for each. Marks unclear wording and stops before signing, sending or cancelling; gives no legal opinion. |
| [Dead code candidates, evidence before removal](skills/dead-code-candidates/SKILL.md) | Grok Build | Lists code that appears unused, with reference searches, search scope and possible indirect callers. Stops at a candidate list; deletes nothing and opens no pull request. |
| [Dependency update order, plan only](skills/dependency-update-plan/SKILL.md) | Grok Build | Lists dependencies with evidence of newer versions, reads available changelogs, and orders proposed updates with risks. Stops at a plan; no installs or repository edits without approval. |
| [Document freshness check, proposed edits only](skills/doc-freshness-check/SKILL.md) | Grok Bot | Checks document dates, versions, prices and owners against named current sources, then lists proposed edits. Stops before editing, sending or publishing any document. |
| [Failing test triage, proposed diff only](skills/failing-test-triage/SKILL.md) | Grok Build | Runs the named failing tests, traces the first supported cause, and proposes a small diff. Stops before applying it, weakening tests, committing or pushing. |
| [FAQ proposals from resolved tickets](skills/faq-from-tickets/SKILL.md) | Grok Bot | Proposes FAQ questions and answers from resolved tickets, removes customer details and lists supporting ticket references for each. Stops before publishing or editing the help site. |
| [First incident notes, no production changes](skills/incident-first-notes/SKILL.md) | Grok Bot | Turns an alert or error event into draft incident notes with known facts, a sourced timeline, unknowns and suggested checks. Stops before production changes, paging or sending updates. |
| [Inbox triage, drafts only](skills/inbox-triage-drafts/SKILL.md) | Grok Bot | Sorts new mail into four piles, drafts replies for the pile that needs one, and stops. It never sends, archives or deletes. |
| [Meeting notes into decisions and actions](skills/meeting-notes-to-actions/SKILL.md) | Grok Bot | Turns meeting notes into decisions, actions and open questions. Owners and dates appear only when stated. Stops before sending notes or creating tasks. |
| [Migration plan review, no database execution](skills/migration-plan-review/SKILL.md) | Grok Build | Reviews a migration file for locking, backfill size, code rollout order and recovery options. Returns risks and open questions, then stops before file changes; it never runs a migration against any database. |
| [Newsletter issue from supplied notes](skills/newsletter-draft-from-notes/SKILL.md) | Grok Bot | Turns supplied notes and sources into one newsletter issue with a subject, preview and cited sections. Stops at a draft before sending or publishing. |
| [One customer reply from named policies](skills/customer-reply-draft/SKILL.md) | Grok Bot | Drafts one customer reply using only named policy documents, with clause references and marked gaps. Stops before sending, refunding, closing the case or changing customer records. |
| [PR review notes, no posted comments](skills/pr-review-notes/SKILL.md) | Grok Build | Reviews a repository diff or branch for correctness risks, missing tests and unclear names. Returns findings with file and line, then stops before commits, pushes, merges or comment posting. |
| [README command check, proposed edits only](skills/readme-command-check/SKILL.md) | Grok Build | Checks README commands, paths and task names against repository definitions. Returns proposed edits and stops before executing commands, editing files, committing or pushing. |
| [Receipt reconciliation, report only](skills/receipt-reconcile/SKILL.md) | Grok Bot | Matches receipts to a statement export and lists matches, mismatches and missing receipts. It stops at a report and never pays, files or submits an expense claim. |
| [Release notes from commits, draft file only](skills/release-notes-from-commits/SKILL.md) | Grok Build | Reads a repository commit range, groups changes and flags possible breaking changes. Writes one draft file and stops before tagging, committing or publishing. |
| [Renewal price check, questions only](skills/renewal-price-check/SKILL.md) | Grok Bot | Reads the current renewal price, compares it with the last payment, and drafts questions for the vendor. It stops before contacting the vendor, renewing, cancelling or buying. |
| [Review a draft skill before saving](skills/review-a-draft-skill/SKILL.md) | Grok Bot | Reviews a draft skill against six required parts and adds decision rules, failure handling and approval boundaries. Returns revised text and stops before overwriting a saved skill. |
| [Spreadsheet export checks, row report only](skills/spreadsheet-sanity-check/SKILL.md) | Grok Bot | Checks a spreadsheet export for blanks, duplicates, values outside stated ranges and totals that disagree. Reports source rows and stops before editing the source file or sending the report. |
| [Support tickets, sorted with reply drafts](skills/support-ticket-sort/SKILL.md) | Grok Bot | Sorts new support tickets by urgency and type, explains each choice, and drafts first replies. Stops before sending, closing tickets or issuing refunds. |
| [Task handoff note, ready for review](skills/handoff-note/SKILL.md) | Grok Bot | Writes a handoff note with the current state, completed work, open work, locations, next step and pending approvals. Stops before sending it or taking the next action. |
| [Travel option comparison, no booking](skills/travel-option-compare/SKILL.md) | Grok Bot | Looks up current travel prices and compares options against dates, budget and travel rules. Returns priced options and gaps, then stops before booking, paying or holding a seat. |
| [Vendor quote comparison, questions only](skills/vendor-quote-compare/SKILL.md) | Grok Bot | Compares named vendors against the same requested line items, shows missing terms and drafts questions for each vendor. It stops before buying, accepting a quote or sending anything. |
| [Weekly status digest, draft only](skills/weekly-status-digest/SKILL.md) | Grok Bot | Collects the week's work from a work log and named sources into a digest with completed work, blockers and next steps. It stops at a draft and never sends it. |

### Routine briefs (`routines/`)

| Item | Runs on | What it does, and where it stops |
| --- | --- | --- |
| [Email task proposals, chat list only](routines/routine-email-task-proposals.md) | Grok Bot | Turns matching mail to the Bot’s own address into one proposed task in a chat list. Stops before replies, task execution or creating anything in other apps. |
| [First notes for a new incident](routines/routine-sentry-new-issue-notes.md) | Grok Bot | Writes first incident notes for a new Sentry issue in one project at the chosen severity or above. It leaves checks as proposals, pages nobody and makes no production changes. |
| [Friday weekly status digest](routines/routine-weekly-status-friday.md) | Grok Bot | Runs a saved status skill every Friday and puts a weekly digest in the Bot's chat. Follow-ups stay drafts; nothing is sent elsewhere or changed in production. |
| [Monthly document freshness review](routines/routine-doc-freshness-monthly.md) | Grok Bot | Reviews a document set each month and lists proposed edits with their evidence in the Bot's chat. It stops before editing, commenting, sending notifications or publishing. |
| [Monthly renewal watch, questions only](routines/routine-renewal-watch-monthly.md) | Grok Bot | Checks upcoming renewals each month, looks prices up again and drafts questions in the Bot's chat. It stops before renewing, cancelling, paying or sending questions. |
| [Monthly review of dated memories](routines/routine-memory-review-monthly.md) | Grok Bot | Lists this Bot's memories containing dates, prices, owners or versions and proposes a fresh lookup or forgetting. Stops before looking up replacements or changing remembered information. |
| [New Linear issue triage notes](routines/routine-linear-new-issue-notes.md) | Grok Bot | Prepares request, missing information and suggested size notes for newly created issues matching one team and label. Stops before changing any Linear status, assignee or label. |
| [New pull request review notes](routines/routine-github-pr-review-notes.md) | Grok Bot | Writes review notes in the Bot's chat when a pull request opens in one repository against one base branch. It posts no GitHub comments, changes no files and never merges. |
| [One-channel Slack phrase digest](routines/routine-slack-phrase-digest.md) | Grok Bot | Adds one source-linked line to a running chat list when a new message in one Slack channel contains the chosen phrase. Stops before posting anything in Slack or acting on the message. |
| [PagerDuty incident and recent change notes](routines/routine-pagerduty-incident-notes.md) | Grok Bot | Writes first notes for a new incident in one service, compares recent change records and suggests checks. Stops before acknowledging, resolving, escalating, paging or changing production. |
| [Receipt emails into an expense list](routines/routine-email-receipt-filing.md) | Grok Bot | Extracts vendor, date, amount and currency from matching receipt emails to the Bot and adds them to a list. It stops before paying, submitting expenses or sending mail. |
| [Slack mentions into a request list](routines/routine-slack-mention-intake.md) | Grok Bot | Records requests when this Bot is mentioned in one Slack channel and explains its understanding in Bot chat. It stops before posting to Slack or acting on the request. |
| [Webhook form intake with field checks](routines/routine-webhook-form-intake.md) | Grok Bot | Checks webhook form data and adds one normalized record to the chosen intake list. It rejects malformed input and stops before sending, publishing or changing production. |
| [Weekday calendar and meeting preparation brief](routines/routine-daily-calendar-brief.md) | Grok Bot | Lists today's meetings, overlaps and preparation from current calendar entries each weekday. Stops before moving, declining or deleting events, sending invitations or contacting attendees. |
| [Weekday morning inbox brief](routines/routine-morning-inbox-brief.md) | Grok Bot | Asks a Bot to run an inbox triage every weekday morning and post one short brief in its chat. Replies stay drafts. |
| [Weekly release notes from merged changes](routines/routine-release-notes-weekly-draft.md) | Grok Bot | Drafts weekly release notes from changes merged since the previous completed review and returns them in chat. Stops before publishing, tagging, creating a release or changing the repository. |
| [Weekly review of expired approvals](routines/routine-expired-approvals-weekly.md) | Grok Bot | Lists actions this Bot reported as not done after an approval card expired during the past week. Asks which to prepare again and stops before redoing any action. |
| [Weekly routine usage review](routines/routine-usage-review-weekly.md) | Grok Bot | Reviews this Bot's recent routine runs, failures and empty results, then proposes changes in chat. It stops before pausing, editing, deleting, running Test or sending notifications. |

### Bot setup sheets (`bots/`)

| Item | Runs on | What it does, and where it stops |
| --- | --- | --- |
| [Calendar desk, review and proposed moves](bots/bot-calendar-desk.md) | Grok Bot | Reviews upcoming commitments against your scheduling rules and keeps a list of proposed moves. It stops before changing events, declining invitations or sending invites. |
| [Code review desk, pull request notes only](bots/bot-code-review-desk.md) | Grok Bot | Prepares pull request notes in named repositories and tracks concerns across revisions. It stops before commenting, approving, merging or pushing and returns the notes in chat. |
| [Custom Rules for draft preparation](bots/bot-custom-rules-starter.md) | Grok Bot | Provides seven Ask first rules and three narrow Allow automatically rules. Sending, publishing, purchases, payments, deletion and production changes stop for approval. |
| [Docs desk, proposed updates and open decisions](bots/bot-docs-desk.md) | Grok Bot | Tracks stale facts and proposed edits across a named document set, carrying open decisions between reviews. Stops before editing documents, posting comments or publishing changes. |
| [Expense desk, receipts to drafts](bots/bot-expenses-desk.md) | Grok Bot | Sets one Bot to organize receipts and prepare expense summaries. It stops at drafts and never purchases, pays or submits claims. |
| [Inbox desk, triage and reply drafts](bots/bot-inbox-desk.md) | Grok Bot | Sets one Bot to sort mail and prepare reply drafts from current threads. It stops before sending and asks first before archiving, deleting or replacing drafts. |
| [Incident desk, first notes and open questions](bots/bot-incident-notes-desk.md) | Grok Bot | Prepares incident notes on what fired, recent changes and what to check next. It stops at notes and never changes production, pages anyone or posts publicly. |
| [One job for a new Bot](bots/bot-one-job-starter.md) | Grok Bot | Sets one job, remembered rules, sources and approval boundaries for a new Bot. It stops at a proposed action before sending, publishing, paying, deleting or changing production. |
| [Primary Bot, offers before action](bots/bot-primary-brief.md) | Grok Bot | Gives the primary Bot one coordination job, a roster and quiet hours. It proposes work first and waits for a yes before acting, including creating Bots or sending anything. |
| [Purchasing desk, quotes and renewal preparation](bots/bot-purchasing-desk.md) | Grok Bot | Prepares purchase comparisons and renewal decisions from current quotes, with expiry dates and open questions. Stops before contacting vendors; never buys, renews, cancels or pays. |
| [Release desk, preparation notes only](bots/bot-release-desk.md) | Grok Bot | Sets up a Bot to draft release changes, risks and a checklist from repository records. It stops at preparation notes and never tags, deploys or merges. |
| [Research desk, briefs with sources](bots/bot-research-desk.md) | Grok Bot | Sets up a Bot to compare sources, draft research briefs and mark unsupported claims as unverified. It stops at a brief in chat and never publishes. |
| [Team intake desk, records and routing notes](bots/bot-team-intake-desk.md) | Grok Bot | Records team requests with proposed owners or queues and missing information. It stops before contacting owners, changing assignments or doing the requested work. |
| [Team support desk, drafts only](bots/bot-team-support-desk.md) | Grok Bot | Sets one shared support job, lists what teammates can access, and prepares triage notes and reply drafts. It stops before sending, closing tickets or publishing the Bot. |

### Checklists (`procedures/`)

| Item | Runs on | What it does, and where it stops |
| --- | --- | --- |
| [Build a deep link with an unsent message](procedures/proc-deep-link-builder.md) | Grok Bot | Guides you through a Bot id, short message, URL encoding and an opening check. Stops with the message unsent and the link unpublished. |
| [Check a Bot before sharing](procedures/proc-share-scrub.md) | Grok Bot | Checks a Bot’s sharing material and team access for private information. Stops before sharing, publishing, sending, payment, deletion or production changes. |
| [Check a first message before you send it](procedures/proc-first-message-check.md) | Grok Bot | A checklist for the first message to a new Bot: one job, sources, rules to remember, approval boundaries, no secrets. Stops before the message is sent; nothing is sent, published, paid for or deleted. |
| [Check a Team Bot draft before Publish](procedures/proc-team-bot-before-publish.md) | Grok Bot | A checklist for a Team Bot that is still a Draft: the About description, plugins, apps, secrets, skills, files and roles. Stops before Publish; nothing is published, paid for or deleted. |
| [Check a webhook routine before use](procedures/proc-webhook-trigger-check.md) | Grok Bot | Walks through a safe webhook request and its run result. Stops before downstream messages, publishing, payments, deletion or production changes. |
| [Move old Description text into chat](procedures/proc-description-to-chat.md) | Grok Bot | For people who kept instructions in a personal Bot's Description: say the same rules in chat, ask the Bot to remember them, check what it kept. Sends nothing outside the Bot's chat; publishes and deletes nothing. |
| [Plan a routine usage budget](procedures/proc-routine-usage-budget.md) | Grok Bot | Estimates scheduled and event-driven runs against documented limits. Stops before increasing activity with unknown counts or allowing sending, publishing, payments, deletion or production changes. |
| [Review a skill learned from a demonstration](procedures/proc-taught-skill-hardening.md) | Grok Bot | Turns a demonstrated workflow draft into instructions with decision rules, failure handling and a safe example. Stops before sending, publishing, payment, deletion or production changes. |
| [Review your Custom Rules](procedures/proc-custom-rules-review.md) | Grok Bot | A checklist for reading every "Ask first" and "Allow automatically" rule, finding overlaps and gaps, and writing proposed changes. Stops before any rule is changed; nothing is sent, published, paid for or deleted. |
| [Routine preflight before it runs alone](procedures/proc-routine-preflight.md) | Grok Bot | Checks a routine before a safe Test and resuming scheduled work. Stops on unresolved checks or any action that would send, publish, pay, delete or change production. |
| [See and correct what a Bot remembers](procedures/proc-memory-check.md) | Grok Bot | Ask a Bot what it remembers on one topic, then correct or remove entries one at a time. Nothing is forgotten without your decision; nothing is sent, published, paid for or deleted elsewhere. |

`index.json` lists every item with its stops, first three moves, blanks and sources.

## License and sources

MIT, see [LICENSE](LICENSE). Sources: [SOURCES.md](SOURCES.md). Other people's shared Bots are not copied here.

## Problems and results

If a text does not behave as it says, open an issue with the item name, what you ran it on, and what happened (leave out private data).
"Grok" and "Grok Bot" are names of xAI products; they are used here only to say what the texts are for.

## Related

- Site: [botshelfvampire.com](https://botshelfvampire.com/). Everything in one searchable index: [Explore](https://botshelfvampire.com/explore/)
- [botshelf-ai-team-registry](https://github.com/BotShelfVampire/botshelf-ai-team-registry): the Build Library registry and the free AI teams (`free-ai-teams/`, MIT)
- [botshelf-mcp](https://github.com/BotShelfVampire/botshelf-mcp): the read-only MCP server for the shelf (`com.botshelfvampire/botshelf` in the MCP Registry). Setup lines: https://botshelfvampire.com/mcp/
