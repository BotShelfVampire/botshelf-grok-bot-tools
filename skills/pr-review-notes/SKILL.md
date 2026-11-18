---
name: pr-review-notes
description: Review a repository diff or branch and return notes with file and line references. Use when asked for a PR review, correctness review or missing test check.
when-to-use: review this PR, review this diff, review this branch, find missing tests
metadata:
  author: BotShelf Vampire (unofficial, not xAI)
  short-description: Repository review that stops at notes
license: MIT
---

# PR review notes, no posted comments

## When to use
Use this when I ask for a review of a specific diff or branch. Read the change and its surrounding code before drawing conclusions. Keep the repository unchanged.

## Inputs and access
- Local repository: [REPOSITORY].
- Review target: [REVIEW_TARGET].
- Comparison base: [BASE_REF].
- Particular focus: [REVIEW_FOCUS].
Use local files and history. Do not fetch remote changes or request credentials in chat.

## Steps
1. Read repository guidance, identify the target and base, and record their resolved revisions. Note existing working changes without replacing them.
2. Inspect the diff and the relevant callers, data flow and error handling. Follow changed behavior far enough to explain its effect.
3. Look for correctness risks and boundary cases. For each candidate, identify the input or condition that would cause the problem.
4. Read nearby tests. Describe missing coverage with a concrete case and expected behavior. Do not claim that absent coverage proves a defect.
5. Flag unclear names only when they obscure meaning or could lead to misuse. Keep these suggestions separate from correctness findings.
6. Rank findings by impact. Give the file, line, trigger, consequence and supporting evidence for each. Mark uncertain conclusions as questions.

## Check the result
Check that each cited line belongs to the reviewed revision. Remove duplicate findings and unsupported claims. Distinguish observed code behavior from assumptions. Report the inspected scope and any areas left unread.

## What to return
Return findings first, followed by missing tests, naming suggestions and open questions. If there are no supported findings, say so with the scope limits. Include a short list of checks that a person could run next.

## Needs my approval
Stop before editing files, committing, pushing, merging, deploying, force operations or posting comments. Also stop before sending messages, publishing, purchasing, paying, deleting or changing production. Return notes only.

## If data is missing or stale
If a reference is missing or the comparison is ambiguous, report it and stop. If the target changes during review, identify the mismatch and withhold conclusions about the new revision. Do not reconstruct missing code from memory.
