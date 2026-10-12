# Git and GitHub Assignment

## Overview

This repository documents my hands-on practice with Git Cherry-pick, Git Rebase, and Markdown Release Notes.

The objective of this assignment is to understand Git commands, manage branches, and maintain clear project documentation.

## 1. Git Cherry-pick

**Objective:** Apply a specific commit from one branch to another without merging the entire branch.

### Steps Performed

1. Created a `feature` branch from `main`.
2. Added a Login feature and committed the changes.
3. Added a Registration feature as a separate commit.
4. Switched to the `main` branch.
5. Cherry-picked only the Login feature commit.

### Command Used

```bash
git switch main
git cherry-pick 4b9bcdc
```

### Result

- Original Login commit: `4b9bcdc`
- Cherry-picked Login commit: `abbb874`
- The Login feature was added to `main` without bringing the Registration feature.

## 2. Git Rebase

**Objective:** Reapply feature branch commits on top of the latest `main` branch.

### Steps Performed

1. Created a `rebase-demo` branch.
2. Added and committed a Dashboard feature.
3. Switched to `main` and committed a Profile feature.
4. Switched back to `rebase-demo`.
5. Rebasing placed the Dashboard commit after the latest `main` commit.

### Command Used

```bash
git switch rebase-demo
git rebase main
```

### Result

- Original Dashboard commit: `af51141`
- Rebased Dashboard commit: `1d6079d`
- The rebased branch contains both Profile and Dashboard features.
- The commit history is linear.

## 3. Markdown Release Notes

**Objective:** Learn how to document software releases using Markdown.

The release notes will be maintained in `RELEASE_NOTES.md` and will include verified release information such as:

- Version and release date
- New features
- Bug fixes
- Improvements
- Known issues

## Conclusion

Through this assignment, I gained practical experience in selecting commits with Git Cherry-pick, updating branch history with Git Rebase, and preparing structured software release documentation.
