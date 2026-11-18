---
name: release-notes-from-commits
description: Draft release notes from a local commit range with grouped changes and breaking change flags. Use when asked to summarize commits for a release without tagging or publishing.
when-to-use: draft release notes, summarize this release, write notes from commits
metadata:
  author: BotShelf Vampire (unofficial, not xAI)
  short-description: Commit evidence turned into a draft file
license: MIT
---

# Release notes from commits, draft file only

## When to use
Use this when I ask for release notes from an explicit commit range. Produce a reviewable draft for the stated readers. Do not infer that these changes are already released.

## Inputs and access
- Local repository: [REPOSITORY].
- Commit range: [FROM_REF]..[TO_REF].
- New draft file: [DRAFT_FILE].
- Intended readers: [AUDIENCE].
Read local history, diffs and repository guidance. The only allowed write is the new draft file.

## Steps
1. Resolve both references locally and record their revisions. List the commits in the range. If the range is empty, report that and stop without creating a file.
2. Read commit messages and relevant diffs. Trace each proposed note to a commit and changed behavior; a message alone may be incomplete.
3. Group notes under Added, Changed, Fixed and Removed. Omit empty groups. Combine related commits without losing their references.
4. Flag changes to public interfaces, configuration, required inputs or stored data that may break existing use. Separate supported breaking changes from questions needing an owner decision.
5. Describe effects in language suited to the intended readers. Do not invent release dates, version numbers, adoption claims or migration instructions absent from the sources.
6. Check the destination. If it already exists, return proposed text without overwriting it. Otherwise write the draft, including its range, evidence and open questions.

## Check the result
Make sure each note has a supporting commit. Account for reversions and follow-up changes before describing the final effect. Check that unrelated history is excluded and that uncertainties remain visible. Inspect the draft for secrets before returning it.

## What to return
Return the draft location, resolved range, change groups, breaking change flags and unanswered questions. State which commits could not be interpreted. Keep review questions distinct from the release prose.

## Needs my approval
Stop before overwriting files, tagging, committing, pushing, merging, deploying or force operations. Also stop before sending messages, publishing, purchasing, paying, deleting or changing production. Do not create a release.

## If data is missing or stale
If either reference is unavailable, report the missing input without fetching it. If references move during work, identify the old revisions and leave the draft pending review. Do not fill missing history from memory.
