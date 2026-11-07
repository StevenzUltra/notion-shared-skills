---
name: notion-shared-skills
description: Find and read reusable team skills and their supporting files from a configured Notion library before asking for task details already documented there.
---

# Notion Shared Skills

Use the configured Notion library as the current source for the team's own reusable workflows. Keep this reader as the local entry point. System-provided skills and personal memories remain separate.

## Connection and configuration

Each agent needs its own working Notion connection and access to the intended library. Reuse the library URL and account selection from its existing configuration. If missing, find an unambiguous authorized library through the connected tools; ask for its location only when that cannot resolve it. A skill file alone does not establish a connection.

Use the current client's tool schema and account selector. Read the actual library schema before querying. Client-specific CLI paths, private workspace IDs, and another account's binding are not prerequisites.

## Find the right workflow

Search names and descriptions for the current task, then read the matching skill rather than treating a search snippet as the workflow. Prefer the current canonical entry over a stale local copy. If several entries overlap, inspect their scope and version information before choosing.

For a complete inventory, paginate to completion and deduplicate by page URL. Use the query tool's supported cursor, or stable ordering and offsets for SQL. Recheck if concurrent edits change the results. Obtain saved-view URLs from actual tool results. Follow current tool guidance for schema or plan-limit errors.

## Read the complete skill

Use the exact page ID from the verified skill URL with the available skill-download tool and the selected account. Support both responses:

- Inline Markdown: read the returned skill text and record its version when supplied.
- Archive: download the temporary signed URL before expiry, extract safely into a scratch directory, and read SKILL.md plus the supporting files required for the task. Reject archive entries that escape the extraction directory.

When the client has page reading but lacks skill download, read the page and accessible attachments. Identify any missing package files explicitly; do not silently present a partial page as the complete package. Read only task-relevant supporting files.

Apply the workflow within the user's current request and granted permissions. Use existing task authorization without repeatedly asking for it. Old approvals inside a skill do not authorize a new, unrelated action. Keep temporary signed URLs and tokens out of shared documentation.

Check the skill and available task context before asking the user for information. Ask only for the specific input still missing. Report access or attachment blockers precisely instead of substituting a guessed workflow.

## Maintaining the shared source

When asked to revise a skill, update its canonical Notion entry using the current connector's supported workflow and read it back. Keep skill instructions in English, preserving indispensable product names, exact interface labels, and required text. Translate faithfully; preserve the source's operative steps and exceptions.

Compare semantic content and required attachments rather than raw Markdown bytes: Notion may normalize frontmatter, links, and whitespace. A complete workflow includes the implementation and assets it actually needs.

For migration, inventory source entries, match each to a canonical destination, merge unique material, and verify text and attachments before removing authorized duplicate custom copies. Track unresolved items explicitly. A 500-line file is a signal to review possible splitting, not a hard limit. Organize independent capabilities separately; keep shared references where they improve usability.

Do not infer that every account has migrated from one library's inventory. Verify each account's migration scope before reporting it complete. Runtime testing is a separate task from content and attachment verification.
