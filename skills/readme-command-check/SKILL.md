---
name: readme-command-check
description: Compare README commands and paths with local repository definitions and propose corrections. Use when asked to check setup or task instructions against the codebase.
when-to-use: check README commands, check documented paths, compare README tasks with scripts
metadata:
  author: "BotShelf Vampire (unofficial, not xAI)"
  short-description: README command and path corrections as a list
license: MIT
---

# README command check, proposed edits only

## When to use
Use this when I ask whether README commands and paths match the repository. Check what each instruction refers to and propose specific edits. Do not execute the documented commands during this review.

## Inputs and access
- Local repository: [REPOSITORY].
- README file: [README_FILE].
- Sections to inspect: [SECTIONS].
- Intended shell and operating system: [ENVIRONMENT].
Use read access to documentation, script definitions, task configuration and files. Keep the working tree unchanged and use no network sources.

## Steps
1. Read repository guidance and record the current revision and relevant working changes. Extract commands and paths from the named sections, preserving their line numbers and stated prerequisites.
2. Track the working directory through each sequence. Distinguish literal paths from example values, generated outputs and files that should already exist. Check path spelling and case against the repository.
3. Resolve each named script or task to its definition. Inspect referenced entry files and arguments. Follow local wrappers far enough to identify the underlying task without running them.
4. Compare command order with required setup steps. Flag undefined tasks, missing entry files, misplaced directory changes and options unsupported by the inspected definitions. Treat shell or environment differences as conditional findings.
5. For each supported mismatch, propose the smallest wording or command correction and cite its repository evidence. When intent is unclear, supply a question instead of inventing a replacement command.

## Check the result
Each proposal must identify a README line and the corresponding definition or bounded file search. Do not mistake a generated path's current absence for an error. Distinguish a command that names an existing task from one known to work at runtime; static inspection establishes only the former.

## What to return
Return a list of proposed edits with the original instruction, reason, evidence location and replacement text. Follow it with unresolved commands, environment assumptions and sections not inspected. Report when no supported correction was found within the stated scope.

## Needs my approval
Stop before editing files, running project commands, installing dependencies, committing, pushing, merging, deploying or force operations. Stop before sending messages, publishing documentation, purchasing, paying, deleting files or changing production.

## If data is missing or stale
Report missing definitions or unreadable files as unresolved. If the README or relevant definitions change during review, identify affected proposals and withhold them until compared again. Do not guess from memory.
