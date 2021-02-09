Merge.md
## *Merge*
Merging is Git's way of putting a forked history back together again. The git merge command lets you take the independent lines of development created by git branch and integrate them into a single branch.
The git merge is often used in conjunction with git checkout for selecting the current branch and git branch -d for deleting the obsolete target branch.

## *How it works*
Git merge will combine multiple sequences of commits into one unified history. In the most frequent use cases, git merge is used to combine two branches. The following examples in this document will focus on this branch merging pattern. In these scenarios, git merge takes two commit pointers, usually the branch tips, and will find a common base commit between them. Once Git finds a common base commit it will create a new "merge commit" that combines the changes of each queued merge commit sequence.
Git merging combines sequences of commits into one unified history of commits.
There are two main ways Git will merge: Fast Forward and Three way
Git can automatically merge commits unless there are changes that conflict in both commit sequences

## How to merge
1. Fork a repository on GitHub(If not a Collaborator)
2. Clone it onto your computer
3. Make a branch and move to it
4. Make a Commit 
5. Checkout to Master branch
6. Git Merge the new branch with master