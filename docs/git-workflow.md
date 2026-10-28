## Git Workflow Guide

## 1. What Is Git?

Git is a distributed version control system that tracks changes in files and helps developers collaborate on projects.

## 2. Common Git Workflow

1. Initialize a repository using `git init`.
2. Check changes using `git status`.
3. Stage files using `git add`.
4. Save changes using `git commit`.
5. Create branches for new features.
6. Push branches to GitHub.
7. Open a pull request for review.
8. Merge approved changes into the target branch.

## 3. Branching Strategy
- `main`: Contains the stable project version.
- `dev`: Integrates work before it reaches `main`.
- `feature/\*`: Contains individual features or improvements.

## 4. Merge vs. Rebase

## Merge

Combines changes from one branch into another and can preserve the branch history with a merge commit.

```bash

git switch dev

git merge feature/git-workflow-docs

```

## Rebase

Reapplies commits on top of another base commit, creating a more linear history.

```bash

git switch feature/git-workflow-docs

git rebase dev

```

Avoid rebasing shared branches unless the team has agreed on that workflow.

## 5. Pull Requests
A pull request (PR) proposes merging changes from one branch into another on GitHub. It allows reviewers to inspect changes, discuss improvements, and approve the merge.

## 6. Merge Conflicts
Merge conflicts happen when Git cannot automatically reconcile changes, often because the same lines were changed in different branches.

General resolution steps:

1. Run `git status` to find conflicted files.
2. Open each conflicted file.
3. Resolve the conflict markers.
4. Stage the resolved files using `git add`.
5. Complete the merge or rebase.

## 7. Git Tags
Tags mark specific points in the repository's history, commonly used for releases.

```bash

git tag -a v1.0.0 -m "Version 1.0.0"

git push origin v1.0.0

```

## 8. Git Stash
`git stash` temporarily saves uncommitted tracked changes so you can switch tasks without committing them.

```bash

git stash

git stash list

git stash pop

```

## 9. The .gitignore File

`.gitignore` lists files and directories Git should ignore when they are untracked, such as temporary files, editor settings, and environment files containing secrets.

It does not automatically remove files already tracked by Git.

## 10. Useful Commands
| Command | Purpose |

|---|---|

| `git status` | Check repository status |

| `git log --oneline` | View compact commit history |

| `git branch` | List local branches |

| `git switch -c branch-name` | Create and switch to a branch |

| `git diff` | Inspect unstaged changes |

| `git fetch` | Download remote updates |

| `git pull` | Fetch and integrate remote updates |

| `git push` | Upload local commits |
