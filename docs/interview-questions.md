\# Git Interview Questions and Answers



\## 1. What is Git?



Git is a distributed version control system that tracks changes in files, maintains project history, and helps developers collaborate.



\## 2. What is the difference between merge and rebase?



\- \*\*Merge:\*\* Combines branch changes and may create a merge commit. It preserves the existing branch history.

\- \*\*Rebase:\*\* Replays commits on top of another base commit, producing a more linear history.



\## 3. What is a pull request?



A pull request (PR) is a GitHub feature used to propose changes from one branch into another. It supports code review, discussion, and approval before merging.



\## 4. How do you resolve merge conflicts?



1\. Run `git status` to identify conflicted files.

2\. Open the files and review the conflict markers.

3\. Edit the files to keep the intended changes.

4\. Stage the resolved files with `git add`.

5\. Complete the merge with `git commit`, or continue the rebase with `git rebase --continue`.



\## 5. What are Git tags?



Git tags are references to specific commits, often used to mark software releases such as `v1.0.0`.



Example:



```bash

git tag -a v1.0.0 -m "First release"

```



\## 6. What is a Git workflow?



A Git workflow is a process a team follows to manage changes, including branching, committing, reviewing, merging, and releasing code.



\## 7. Explain git stash.



`git stash` temporarily saves eligible uncommitted changes so you can switch tasks without creating a commit.



Useful commands:



```bash

git stash

git stash list

git stash pop

```



\## 8. What is the use of .gitignore?



`.gitignore` tells Git which untracked files or directories to ignore, such as temporary files, build artifacts, and local environment files. It does not automatically untrack files already committed.



