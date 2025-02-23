# Kimi's Git Aliases

A customized collection of Git aliases focused on topic branch and Jira workflow management, based on the comprehensive [GitAlias](https://github.com/GitAlias/gitalias) project.

## Common Shortcuts

### Basic Commands
* `git a` - Short for `git add`
* `git b` - Short for `git branch`
* `git c` - Short for `git commit`
* `git d` - Short for `git diff`
* `git f` - Short for `git fetch`
* `git l` - Short for `git log`
* `git m` - Short for `git merge`
* `git o` - Short for `git checkout`
* `git p` - Short for `git pull`
* `git s` - Short for `git status`

### Frequent Operations
* `git aa` - Add all changes
* `git ap` - Add changes interactively (patch)
* `git cm` - Commit with message
* `git ca` - Amend last commit
* `git cane` - Amend last commit without editing message

## Status & Information
* `git ss` - Short status
* `git ssb` - Short status with branch info
* `git bv` - Branch list with details
* `git bvv` - Branch list with upstream info

## Reset & Undo Operations
* `git reset-commit` - Soft reset of last commit
* `git reset-commit-hard` - Hard reset of last commit
* `git uncommit` - Undo last commit
* `git unadd` - Unstage changes
* `git discard` - Discard changes in working directory
* `git cleanout` - Clean and reset working directory

## Sync & Update Operations
* `git get` - Fetch, pull with rebase, and update submodules
* `git put` - Commit all changes and push
* `git push1` - Push current branch to origin
* `git pull1` - Pull current branch from origin
* `git pushy` - Force push with lease (safer than --force)

## Log & History
* `git lg` - Log with graph
* `git lo` - Log one line per commit
* `git ll` - Detailed log with graph and formatting
* `git who` - Show contributor statistics

## Setup and Configuration Aliases

* `git setup` - Sets up Git aliases by configuring the topic base branch and Jira prefix
* `git set-topic-branch` - Prompts for and sets the desired topic base branch name globally
* `git set-jira-prefix` - Prompts for and sets the desired Jira prefix (globally or locally)

## Topic Branch Management

* `git topic-base-branch` - Shows the topic base branch name from config or defaults to default branch
* `git topic-begin <branch-name>` - Starts a new topic branch with:
  - Updates base branch
  - Creates new branch
  - Pushes to remote for collaboration
* `git topic-end` - Completes work on current topic branch:
  - Pushes final changes
  - Deletes branch locally and remotely
  - Returns to base branch

## Jira Integration

* `git jira <prefix> <id> <description>` - Creates a new branch with Jira formatting:
  - Uses configured Jira prefix if available
  - Creates branch name like: `prefix/PROJ-123-description`
* `git jira-rebase` - Rebases current Jira topic branch onto the base topic branch

## Publishing Workflow

* `git publish [remote]` - Publishes current branch to remote (defaults to origin)
* `git unpublish [remote]` - Removes current branch from remote (defaults to origin)

## Work In Progress

* `git wip` - Saves work in progress:
  - Adds all changes
  - Removes deleted files
  - Creates "wip" commit
* `git unwip` - Restores from work in progress:
  - Resets last commit if it was a "wip" commit

## Stash Operations
* `git snapshot` - Stash changes while keeping them in working directory

## Utility Commands
* `git aliases` - List all configured aliases
* `git panic` - Create emergency backup tarball

## Core Utilities

* `git default-branch` - Shows the default branch name
* `git current-branch` - Shows the current branch name

## Credits

This is a focused subset of aliases based on the excellent [GitAlias](https://github.com/GitAlias/gitalias) project. The original project contains hundreds of additional aliases and is available under GPL-2.0-or-later license.

For the full collection of Git aliases and documentation, please visit:
- [GitAlias Repository](https://github.com/GitAlias/gitalias)
- [GitAlias Website](https://gitalias.com)

## License

This customized subset inherits the GPL-2.0-or-later license from the original GitAlias project.
