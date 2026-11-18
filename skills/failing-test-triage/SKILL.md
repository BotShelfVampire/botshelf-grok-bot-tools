---
name: failing-test-triage
description: Run named failing tests and trace their first supported cause when asked to diagnose a repository test failure. Return a small proposed diff without applying it.
when-to-use: diagnose a failing test, trace this test failure, explain a failed assertion
metadata:
  author: BotShelf Vampire (unofficial, not xAI)
  short-description: Test failure evidence and a proposed diff
license: MIT
---

# Failing test triage, proposed diff only

## When to use
Use this when I ask you to investigate failing repository tests. Keep the scope to the named failures and their direct causes.

## Inputs and access
- Local repository: [REPOSITORY].
- Test command: [TEST_COMMAND].
- Existing failure output: [FAILURE_LOG].
Read source, tests and local configuration. Run commands only in the local test environment. Inspect the command and its setup before running it; stop if it could contact production or perform an action needing approval.

## Steps
1. Record the current revision and existing working changes. Leave those changes alone.
2. Read the supplied failure output and identify the command, failing test and earliest relevant error. Separate setup failures from assertion failures.
3. Run the specified tests once. Capture the exit status and relevant output without secrets. If setup is unavailable, stop execution and describe what is missing.
4. Trace the earliest causal failure through the test and implementation. Cite file names and lines. Distinguish a supported cause from a hypothesis; later failures may be consequences.
5. Propose the smallest implementation change as a diff in the response. Explain how it addresses the cause and which focused checks should follow. Do not apply it or change expectations to hide a failure.

## Check the result
Confirm the diagnosis agrees with the captured output and cited source. Check that the proposed diff preserves test coverage and unrelated working changes. List commands actually run separately from suggested checks. Do not describe an unapplied fix as successful.

## What to return
Return the reproduction command and outcome, first supported cause, evidence locations, proposed diff, and next checks. Include incomplete work and unresolved hypotheses.

## Needs my approval
Ask before applying edits, installing dependencies, committing, pushing, merging, deploying or using force operations. Stop before sending messages, publishing, purchasing, paying, deleting files or changing production. Never weaken, skip or delete tests to make the failure disappear.

## If data is missing or stale
If the log refers to another revision, identify the mismatch. If the failure does not recur, report that outcome and the remaining uncertainty. Do not invent a cause or run unrelated commands indefinitely.
