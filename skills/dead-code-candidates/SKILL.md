---
name: dead-code-candidates
description: List apparently unused repository code with search evidence and possible indirect callers. Use when asked to find dead code or assess cleanup candidates without removing anything.
when-to-use: find dead code, list unused functions, assess cleanup candidates, inspect unused modules
metadata:
  author: "BotShelf Vampire (unofficial, not xAI)"
  short-description: Unused code candidates with search evidence
license: MIT
---

# Dead code candidates, evidence before removal

## When to use
Use this when I ask for code that may no longer be used. A missing reference is a search result, not permission to remove code. Keep the repository unchanged.

## Inputs and access
- Local repository: [REPOSITORY].
- Candidate directories or modules: [CANDIDATE_SCOPE].
- Known entry points: [ENTRY_POINTS].
- Search exclusions: [EXCLUSIONS].
Use readable local source, configuration and history. Do not fetch remote code, run the application or request secrets.

## Steps
1. Record the revision and existing working changes. Read repository guidance and identify executable entry points, exports and generated code boundaries.
2. Select possible unused declarations or modules within the candidate scope. Search their names, aliases, import paths and registration strings across the readable repository, respecting exclusions.
3. For each candidate, record the search expressions, directories searched, excluded files and matching locations. Separate declarations, comments and tests from calls that can reach the code.
4. Inspect configuration, registries, command dispatch, reflection and dynamic imports where relevant. Follow reexports and wrapper calls. Flag public interfaces and external consumers whose use cannot be judged from this repository.
5. Group mutually referencing candidates so internal calls do not hide the absence of a reachable entry point. If reachability remains unclear, label it unresolved.
6. List candidates only with their evidence and a remaining question. For each, name the next focused check a maintainer could make before considering removal.

## Check the result
Revisit each cited definition and search scope. Remove candidates with an observed reachable caller. Distinguish no references found from only test references or uncertain dynamic use. Never describe a text search as proof of nonuse.

## What to return
Return a candidate table with file and line, symbol, search evidence, possible indirect use and next check. Follow it with exclusions, unresolved cases and scope limits. If none qualify, say so without claiming the repository contains no dead code.

## Needs my approval
Delete nothing and open no pull request. Stop before edits, commits, pushes, merges, deployments or force operations. Ask before sending messages, publishing, purchasing, paying, deleting anything or changing production. Return notes only.

## If data is missing or stale
Report unreadable paths and incomplete searches. If source changes during review, withhold affected candidates until reviewed again. Do not reconstruct missing callers from memory.
