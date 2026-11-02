---
name: github-auto-sync
description: Initialize or connect a local Git repository to GitHub, perform the first verified push, and configure recurring automatic commits and pushes. Use when the user asks to publish a project and keep it synchronized on a schedule.
---

# GitHub Auto Sync

Set up a local project so its intended files are safely pushed to the requested GitHub repository and subsequent changes are synchronized on the user's schedule.

## Establish the repository

1. Inspect the working tree, current branch, configured remotes, Git identity, and any repository instructions before changing state.
2. Preserve existing history and configuration. Initialize Git only when the directory is not already a repository. Do not overwrite a conflicting remote without first identifying the mismatch to the user.
3. Use the remote URL and branch requested by the user. Do not create or modify a GitHub repository unless the user requested that external change.
4. Stage only files within the user's stated scope. If the request clearly covers the whole project, `git add -A` is appropriate. Never discard unrelated or uncommitted work.
5. Create the initial commit only when there are staged changes. Use the user's commit message when supplied.

## Push and verify

Push the selected branch and set upstream tracking. A local commit is not a successful push.

After pushing, verify all of the following:

- the push command exited successfully;
- the local branch tracks the expected remote branch;
- `git ls-remote --heads <remote> <branch>` returns the expected commit.

If HTTPS fails at the TLS or transport layer, first confirm general GitHub connectivity. When an existing SSH key is available, test it non-interactively with `ssh -o BatchMode=yes -T git@github.com`. If GitHub authenticates the expected account, switching the remote to `git@github.com:OWNER/REPO.git` is a valid recovery. Do not create, upload, or replace credentials without the user's authorization.

Report success only after remote verification. If neither HTTPS nor an already-authorized SSH identity works, keep the local commits intact and state the exact remaining authentication or network blocker.

## Configure recurring synchronization

Use the Codex app's automation capability for recurring work. Resolve the current directory to its saved local project before creating the automation. Prefer updating an existing matching automation instead of creating a duplicate.

The saved automation prompt must:

- operate only in the resolved project path;
- verify the expected branch and remote URL;
- run `git add -A`;
- exit quietly when the staged diff is empty;
- create a timestamped commit only when changes exist;
- push to the expected remote branch;
- never pull, reset, delete files, force-push, rebase, or rewrite history;
- notify the user only when a push or commit fails, authentication is required, or human action is otherwise needed.

Use the interval the user requested. For a five-minute schedule, use a recurring rule equivalent to `FREQ=MINUTELY;INTERVAL=5`. Keep failure-only notifications unless the user explicitly wants routine status messages.

After creating or updating the automation, report its active status, schedule, project path, branch, and remote. Do not claim that the automation proves the initial push succeeded; verify the first push separately.
