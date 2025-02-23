# Kimi's Git Aliases

A customized collection of Git aliases focused on topic branch and Jira workflow management, based on the comprehensive [GitAlias](https://github.com/GitAlias/gitalias) project.

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
