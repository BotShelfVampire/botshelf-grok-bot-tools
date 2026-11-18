---
name: dependency-update-plan
description: Read repository dependency records and available changelogs to propose an update order when asked to plan dependency maintenance. Return a plan without installing or changing files.
when-to-use: plan dependency updates, review outdated dependencies, order dependency upgrades
metadata:
  author: BotShelf Vampire (unofficial, not xAI)
  short-description: Dependency update order with evidence and risks
license: MIT
---

# Dependency update order, plan only

## When to use
Use this when I ask for a dependency update plan. Keep all proposed changes in the response until I approve a separate implementation task.

## Inputs and access
- Local repository: [REPOSITORY].
- Included dependencies or components: [DEPENDENCY_SCOPE].
- Changelogs and dated version records: [CHANGELOG_SOURCES].
- Version constraints and priorities: [TARGET_POLICY].
Read manifests, lockfiles, runtime requirements and relevant tests. Use available local or named source documents. Do not install tools or run commands that change dependency records to gather information.

## Steps
1. Record the repository revision and existing working changes. List the declared constraints and resolved versions separately; identify direct and indirect dependencies where the records allow it.
2. Compare these versions with the supplied version evidence. List outdated dependencies only where a newer version is supported by that evidence. Include the source date; do not call an undated version the latest.
3. Read the available changelogs between each current and proposed version. Note breaking changes, runtime requirements, related dependency constraints and migration work. Mark unread sections explicitly.
4. Propose an order based on prerequisites, compatibility and the stated priorities. Group changes only when they need to move together. Explain each dependency between steps.
5. For each step, give the proposed target, evidence, risks, focused checks and a way to restore the prior dependency state if implementation is later approved. Leave unsupported targets unresolved.

## Check the result
Check that every proposed version fits the stated constraints or clearly names a conflict. Separate known changes from inferred risks. Confirm that no installation or repository edit was performed during planning.

## What to return
Return an inventory, ordered update plan, source locations and dates, risk notes, suggested checks, and unresolved questions. Say which dependencies could not be assessed.

## Needs my approval
Ask before installing anything or editing manifests, lockfiles or source. Stop before committing, pushing, merging, deploying or using force operations. Ask before sending messages, publishing, purchasing, paying, deleting files or changing production.

## If data is missing or stale
Report missing records or inaccessible changelogs. If dates or repository versions disagree, identify the mismatch and make affected steps conditional. Do not guess release contents, freshness or compatibility from memory.
