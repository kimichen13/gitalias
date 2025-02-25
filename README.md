# Kimi's Git Aliases

A customized collection of Git aliases focused on topic branch and Jira workflow management, based on the comprehensive [GitAlias](https://github.com/GitAlias/gitalias) project.

## 📥 Installation

There are two ways to install these Git aliases. 

> Note: The configuration file is named `.kimi.gitalias.ini`, but feel free to rename it to any name you prefer (e.g., `.my.gitalias.ini`). Just make sure to use the same name in both the download/copy command and the `git config` command.

### Option 1: Quick Install (Using curl)

```bash
# Download and install directly to your home directory
curl -o ~/.kimi.gitalias.ini https://raw.githubusercontent.com/kimicla/gitalias/main/kimi.gitalias.ini
git config --global include.path "~/.kimi.gitalias.ini"

# Verify installation
git aliases  # Should list all available aliases
```

### Option 2: Using Git Clone

1. Clone this repository:
```bash
git clone https://github.com/kimicla/gitalias.git
cd gitalias
```

2. Include the aliases in your global Git config:
```bash
# Add to your global Git config
git config --global include.path "$PWD/kimi.gitalias.ini"

# Or copy to your home directory and include it (you can rename the file if you prefer)
cp kimi.gitalias.ini ~/.kimi.gitalias.ini
git config --global include.path "~/.kimi.gitalias.ini"
```

## 🚀 Quick Start

Most frequently used commands:
```bash
git get     # Update your branch
git ss      # Quick status check
git aa      # Stage all changes
git cm      # Commit with message
git push1   # Push to remote
```

For detailed workflow instructions, please check our [Workflow Guide](WORKFLOW.md).

## 📖 Documentation

- [Workflow Guide](WORKFLOW.md) - Comprehensive daily Git workflow guide
- [Original GitAlias](https://github.com/GitAlias/gitalias) - Full collection of Git aliases

## 🔧 Available Aliases

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

### Status & Information
* `git ss` - Short status
* `git ssb` - Short status with branch info
* `git bv` - Branch list with details
* `git bvv` - Branch list with upstream info

### Reset & Undo Operations
* `git reset-commit` - Soft reset of last commit
* `git reset-commit-hard` - Hard reset of last commit
* `git uncommit` - Undo last commit
* `git unadd` - Unstage changes
* `git discard` - Discard changes in working directory
* `git cleanout` - Clean and reset working directory

### Sync & Update Operations
* `git get` - Fetch, pull with rebase, and update submodules
* `git put` - Commit all changes and push
* `git push1` - Push current branch to origin
* `git pull1` - Pull current branch from origin
* `git pushy` - Force push with lease (safer than --force)

### Log & History
* `git lg` - Log with graph
* `git lo` - Log one line per commit
* `git ll` - Detailed log with graph and formatting
* `git who` - Show contributor statistics

## 🔄 Workflow Features

### Setup and Configuration
* `git setup` - Sets up Git aliases by configuring the topic base branch and Jira prefix
* `git set-topic-branch` - Prompts for and sets the desired topic base branch name globally
* `git set-jira-prefix` - Prompts for and sets the desired Jira prefix (globally or locally)

### Topic Branch Management
* `git topic-base-branch` - Shows the topic base branch name from config or defaults to default branch
* `git topic-begin <branch-name>` - Starts a new topic branch
* `git topic-end` - Completes work on current topic branch

### Jira Integration
* `git jira <prefix> <id> <description>` - Creates a new branch with Jira formatting
* `git jira-rebase` - Rebases current Jira topic branch onto the base topic branch

### Publishing Workflow
* `git publish [remote]` - Publishes current branch to remote
* `git unpublish [remote]` - Removes current branch from remote

### Work In Progress
* `git wip` - Saves work in progress
* `git unwip` - Restores from work in progress

### Stash Operations
* `git snapshot` - Stash changes while keeping them in working directory

### Utility Commands
* `git aliases` - List all configured aliases
* `git panic` - Create emergency backup tarball

### Core Utilities
* `git default-branch` - Shows the default branch name
* `git current-branch` - Shows the current branch name

## 📖 Detailed Documentation

For detailed workflow instructions and best practices, please refer to our [Workflow Guide](WORKFLOW.md). This guide includes:
- Daily workflow procedures
- Code review process
- Handling urgent bugs
- Best practices
- Commit message conventions
- Common operations and scenarios

## Credits

This is a focused subset of aliases based on the excellent [GitAlias](https://github.com/GitAlias/gitalias) project. The original project contains hundreds of additional aliases and is available under GPL-2.0-or-later license.

For the full collection of Git aliases and documentation, please visit:
- [GitAlias Repository](https://github.com/GitAlias/gitalias)
- [GitAlias Website](https://gitalias.com)

## License

This customized subset inherits the GPL-2.0-or-later license from the original GitAlias project.
