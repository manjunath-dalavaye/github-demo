# Git Cheat Sheet

Welcome to the **Git Cheat Sheet**! This repository contains a comprehensive list of commonly used Git commands to help you set up, manage, and collaborate on projects with Git and GitHub. These commands will guide you through every aspect of the Git workflow, from setting up a repository to resolving merge conflicts.

## Table of Contents
1. [Setting Up Git](#setting-up-git)
2. [Creating a New Repository](#creating-a-new-repository)
3. [Checking the Status of Files](#checking-the-status-of-files)
4. [Adding Files to Staging Area](#adding-files-to-staging-area)
5. [Committing Changes](#committing-changes)
6. [Viewing History and Logs](#viewing-history-and-logs)
7. [Branching and Merging](#branching-and-merging)
8. [Working with Remote Repositories](#working-with-remote-repositories)
9. [Handling Merge Conflicts](#handling-merge-conflicts)
10. [Stashing Changes](#stashing-changes)
11. [Tagging a Commit](#tagging-a-commit)
12. [Undoing Changes](#undoing-changes)
13. [Deleting a Remote Branch](#deleting-a-remote-branch)
14. [Collaborating via Forks and Pull Requests](#collaborating-via-forks-and-pull-requests)
15. [GitHub Workflow Commands](#github-workflow-commands)

---

## 1. Setting Up Git

Before starting to use Git or GitHub, you need to set up Git in your local environment.

- `git config --global user.name "Your Name"`  
  Sets your Git username globally.
  
- `git config --global user.email "youremail@example.com"`  
  Sets your Git email globally. This email will be used in commits.

- `git config --list`  
  Shows your current Git configurations.

---

## 2. Creating a New Repository

- `git init`  
  Initializes a new Git repository in the current directory.

- `git clone <repository_url>`  
  Clones an existing repository from a URL to your local machine.

---

## 3. Checking the Status of Files

- `git status`  
  Shows the current status of the working directory, including staged, untracked, or modified files.

---

## 4. Adding Files to Staging Area

- `git add <file>`  
  Adds a specific file to the staging area.

- `git add .`  
  Adds all changes (new, modified, or deleted files) in the current directory to the staging area.

---

## 5. Committing Changes

- `git commit -m "Commit message"`  
  Commits the staged changes with a descriptive message.

- `git commit -a -m "Commit message"`  
  Commits changes to tracked files without needing to use `git add`.

---

## 6. Viewing History and Logs

- `git log`  
  Displays a list of all previous commits with their messages and IDs.

- `git log --oneline`  
  Shows a simplified log of commits, with only the commit hash and message.

---

## 7. Branching and Merging

- `git branch`  
  Lists all branches in your repository.

- `git branch <branch-name>`  
  Creates a new branch with the specified name.

- `git checkout <branch-name>`  
  Switches to the specified branch.

- `git checkout -b <branch-name>`  
  Creates and switches to a new branch in one command.

- `git merge <branch-name>`  
  Merges the specified branch into the current branch.

- `git branch -d <branch-name>`  
  Deletes the specified branch after it has been merged.

---

## 8. Working with Remote Repositories

- `git remote -v`  
  Lists all remotes (URLs of the repositories connected to this local repository).

- `git remote add origin <repository_url>`  
  Adds a remote repository (usually on GitHub) and names it "origin".

- `git push origin <branch-name>`  
  Pushes your local branch to the remote repository.

- `git push -u origin <branch-name>`  
  Pushes the branch to the remote and sets the upstream branch.

- `git pull origin <branch-name>`  
  Fetches and integrates changes from the remote repository into your current branch.

- `git fetch origin`  
  Retrieves the latest changes from the remote without merging them into your local branch.

---

## 9. Handling Merge Conflicts

When merging branches, you might encounter conflicts. To handle them:

- `git status`  
  Shows which files have conflicts after a merge.

- `git diff`  
  Shows the differences between the current and conflicting versions of a file.

- **Resolve conflicts manually**  
  Open conflicting files, resolve changes, and remove conflict markers.

- `git add <file>`  
  After resolving conflicts, add the file back to the staging area.

- `git commit`  
  Commit the merged changes after conflicts are resolved.

---

## 10. Stashing Changes

If you want to save your work but not commit it yet:

- `git stash`  
  Temporarily saves (stashes) all your changes and clears the working directory.

- `git stash apply`  
  Applies the stashed changes back to your working directory.

- `git stash pop`  
  Applies the stashed changes and then removes them from the stash list.

- `git stash list`  
  Shows a list of all stashes you have saved.

---

## 11. Tagging a Commit

- `git tag <tag-name>`  
  Tags a specific commit with a name, often used for release points.

- `git tag -a <tag-name> -m "Tag message"`  
  Creates an annotated tag with a message.

- `git push origin <tag-name>`  
  Pushes a specific tag to the remote repository.

- `git push --tags`  
  Pushes all tags to the remote repository.

---

## 12. Undoing Changes

- `git reset --hard`  
  Resets the working directory and index to the last commit, discarding all changes.

- `git reset --soft`  
  Resets to the previous commit but keeps the changes in the working directory.

- `git checkout -- <file>`  
  Discards changes in the working directory for the specified file.

- `git revert <commit>`  
  Creates a new commit that undoes the changes introduced by a previous commit.

---

## 13. Deleting a Remote Branch

- `git push origin --delete <branch-name>`  
  Deletes a remote branch.

---

## 14. Collaborating via Forks and Pull Requests

- **Forking a repository**  
  Fork a repository on GitHub to create your own copy of it.

- `git clone <fork_url>`  
  Clone your forked repository to your local machine.

- **Creating a pull request**  
  After pushing changes to your fork on GitHub, create a pull request to propose that the maintainer review and merge your changes.

---

## 15. GitHub Workflow Commands

- `git rebase <branch-name>`  
  Re-applies commits from one branch on top of another.

- `git cherry-pick <commit>`  
  Applies the changes from a specific commit to the current branch.

