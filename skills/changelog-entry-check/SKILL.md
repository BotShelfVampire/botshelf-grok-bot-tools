---
name: changelog-entry-check
description: Compare an existing changelog entry with a local diff and list omissions or overstated claims. Use when asked whether release wording matches the change.
when-to-use: check this changelog entry, compare changelog with diff, find overstated release claims
metadata:
  author: "BotShelf Vampire (unofficial, not xAI)"
  short-description: Changelog claims matched to changed behavior
license: MIT
---

# Changelog entry check, findings only

## When to use
Use this when I ask whether an existing changelog entry describes a particular change accurately. Review the entry against the final diff, including any reversions. Keep all files unchanged.

## Inputs and access
- Local repository: [REPOSITORY].
- Entry file and section: [CHANGELOG_ENTRY].
- Comparison base: [BASE_REF].
- Change endpoint or supplied diff: [CHANGE_TARGET].
Read local code, history, tests and release guidance. Do not fetch missing references or request secrets.

## Steps
1. Resolve the comparison and record its revisions or supplied diff identity. Locate the exact entry and note its heading, version and audience where stated.
2. Split the entry into factual claims. For each, find the changed code and enough surrounding behavior to explain what users can actually do after the change.
3. Match each claim to file and line evidence. Mark it supported, overstated, contradicted or unresolved. Flag wider availability, removed limitations or performance claims that the diff does not establish.
4. Work back from the diff to find omitted user effects. Check changed defaults, accepted inputs, error behavior and compatibility requirements. Exclude internal rearrangements unless they affect the stated audience.
5. Separate confirmed omissions from questions about intent. Suggest a narrow correction for each supported mismatch, retaining the entry's scope. Do not invent a release date, version or rollout status.

## Check the result
Reconcile both directions: each entry claim has a status, and each relevant changed behavior has an entry reference or an omission reason. Recheck citations against the recorded revisions. Do not treat a test name or commit message alone as evidence of behavior.

## What to return
Return the comparison identity, entry location, missing details and overstated claims. For each finding include the original wording, code evidence, user effect and proposed correction. Finish with unresolved questions and unread scope. Return the review in chat only.

## Needs my approval
Stop before editing files, committing, pushing, tagging, merging, deploying or force operations. Stop before sending messages, publishing notes, purchasing, paying, deleting files or changing production.

## If data is missing or stale
If the entry or comparison is unavailable, identify the gap and stop. If either changes during review, mark affected findings pending a fresh comparison. Do not reconstruct missing content from memory.
