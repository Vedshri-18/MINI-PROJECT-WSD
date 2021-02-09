Commit.md
## *Commit*
It is used to record the changes in the repository. It is the next command after the git add. Every commit contains the index data and the commit message. Every commit forms a parent-child relationship. When we add a file in Git, it will take place in the staging area. A commit command is used to fetch updates from the staging area to the repository.

The staging and committing are co-related to each other. Staging allows us to continue in making changes to the repository, and when we want to share these changes to the version control system, committing allows us to record these changes.

Commits are the snapshots of the project. Every commit is recorded in the master branch of the repository.
We can recall the commits or revert it to the older version. Two different commits will never overwrite because each commit has its own commit-id.

Commit messages are important, especially since Git tracks your changes and then displays them as commits once they're pushed to the server. By writing clear commit messages, you can make it easier for other people to follow along and provide feedback,

## How to Commit
1. Fork a repository on GitHub(If not a Collaborator)
2. Clone it onto your computer
3. Make a branch and move to it
4. Make a Commit 

## The Git Commit command
**$ git commit**
The commit command will commit the changes and generate a commit-id. The commit command without any argument will open the default text editor and ask for the commit messages.