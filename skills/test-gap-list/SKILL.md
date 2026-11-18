---
name: test-gap-list
description: Map changed repository code paths to existing tests and propose one test for each supported gap. Use when asked which tests a diff still needs.
when-to-use: list test gaps, find untested changed paths, suggest tests for this diff
metadata:
  author: "BotShelf Vampire (unofficial, not xAI)"
  short-description: Changed paths with evidence and first test cases
license: MIT
---

# Changed paths and the tests they still need

## When to use
Use this when I ask which changed paths need tests. Focus on missing execution paths and assertions, rather than a general code review.

## Inputs and access
- Local repository: [REPOSITORY].
- Comparison base: [BASE_REF].
- Target revision: [TARGET_REF].
- Test directories and suites: [TEST_SCOPE].
- Existing coverage report, or none: [COVERAGE_EVIDENCE].
Read local source, tests, fixtures and configuration only. Do not run tests, generate coverage or fetch remote files.

## Steps
1. Read repository guidance, resolve the revisions and record the diff scope. Leave existing working changes untouched.
2. Map changed branches, error paths, boundary inputs and state transitions. Give each path a condition, expected observable outcome and source location. Group paths only when one test can distinguish their behavior.
3. Follow test callers, shared fixtures and parameterized cases. Check suite selection and skipped cases. Record directories and symbols searched; a missing direct reference does not establish that no test reaches a path.
4. Match any supplied coverage report to its revision and run scope. Label an unexercised path as such only within that report's scope. Otherwise say "no matching test found" or "execution unknown." Treat missing assertions separately from missing execution.
5. For each supported gap, propose one test name, likely test file, setup, input and assertion. Explain what regression it would catch. Rank cases by consequence and how well each distinguishes the changed behavior; do not invent a defect to justify a test.

## Check the result
Recheck each gap against indirect and parameterized tests. Cite evidence for expected behavior. Remove duplicates and paths outside the diff. Do not equate line coverage with a meaningful assertion.

## What to return
Return resolved revisions, a path map and prioritized gaps. For each gap include evidence, search scope, uncertainty and the first proposed test. List unread suites and unavailable reports. Return recommendations in the response only.

## Needs my approval
Ask before writing any files, running tests, committing, pushing, merging, deploying, force operations or opening a pull request. Stop before sending messages, publishing, purchasing, paying, deleting or changing production.

## If data is missing or stale
Stop if either revision is unavailable. Discard stale coverage as execution evidence and continue source inspection with explicit limits. Report partial coverage of the review; never infer a passing suite or complete test coverage from missing data.
