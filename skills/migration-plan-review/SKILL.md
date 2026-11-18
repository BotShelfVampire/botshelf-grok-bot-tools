---
name: migration-plan-review
description: Review a repository migration file for locking, backfill scope, rollout order and recovery options. Use when asked to assess a database change before execution.
when-to-use: review this migration, assess migration order, check backfill risks, inspect migration recovery
metadata:
  author: "BotShelf Vampire (unofficial, not xAI)"
  short-description: Migration review without database execution
license: MIT
---

# Migration plan review, no database execution

## When to use
Use this when I ask for a review of a proposed database migration and its related application change. Read files only; never execute the migration against any database, including local or disposable databases.

## Inputs and access
- Repository: [REPOSITORY].
- Migration file: [MIGRATION_FILE].
- Related diff and comparison base: [CODE_CHANGE].
- Engine, version and supplied behavior notes: [ENGINE_DETAILS].
- Dated size estimates and write activity: [DATA_PROFILE].
Use local sources. Do not connect to a database or request credentials.

## Steps
1. Read repository guidance and record the migration revision and code comparison. List schema operations and data updates in their written order.
2. For each operation, identify affected tables, indexes and constraints. Use supplied engine details to discuss possible locks, scans or rewrites. Separate supported behavior from questions that need an engine specialist.
3. Inspect backfill predicates, batching, transaction scope, progress tracking and restart behavior. Relate the affected data estimate to the proposed batch size. Do not invent row counts or completion times.
4. Trace old and new application reads and writes. Describe which schema each version expects and whether both can coexist during rollout. Flag removals or constraints that require a preceding code or data change.
5. Read the reversal steps. Distinguish restoring a schema from restoring lost data. List assumptions about backups, retained columns or a forward repair, and mark any irreversible operation.
6. Order the concerns by impact and attach file and line evidence. Propose review questions and sequence changes without editing files.

## Check the result
Account for every migration operation. Ensure each recovery suggestion addresses both schema and data. A reversal script alone is not evidence that recovery will succeed.

## What to return
Return an operation risk table, backfill questions, proposed rollout order and recovery limits. Include source revisions, unknowns and any unread scope.

## Needs my approval
Ask before editing files, committing, pushing, merging, deploying or force operations. Stop before sending, publishing, purchasing, paying, deleting or changing production. This review never runs migrations or database commands.

## If data is missing or stale
Missing engine details or data estimates leave dependent conclusions open. If a source revision changes, mark affected findings stale and request the current files. Return completed observations separately from unresolved questions.
