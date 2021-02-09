pull.md
## *Pull*
The git pull command is used to fetch and download content from a remote repository and immediately update the local repository to match that content. Merging remote upstream changes into your local repository is a common task in Git-based collaboration work flows. The git pull command is actually a combination of two other commands, git fetch followed by git merge. In the first stage of operation git pull will execute a git fetch scoped to the local branch that HEAD is pointed at. Once the content is downloaded, git pull will enter a merge workflow. A new merge commit will be-created and HEAD updated to point at the new commit.

## How Git Pull works
The git pull command first runs git fetch which downloads content from the specified remote repository. Then a git merge is executed to merge the remote content refs and heads into a new local merge commmit.

## Common Options for Git Pull
1. git pull <remote>
Fetch the specified remote’s copy of the current branch and immediately merge it into the local copy. This is the same as git fetch followed by git merge origin/.

2. git pull --no-commit <remote>
Similar to the default invocation, fetches the remote content but does not create a new merge commit.

3. git pull --rebase <remote>
Same as the previous pull Instead of using git merge to integrate the remote branch with the local one, use git rebase.

4. git pull --verbose
Gives verbose output during a pull which displays the content being downloaded and the merge details.

