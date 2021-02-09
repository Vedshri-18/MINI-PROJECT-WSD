push.md
## *push*
The git push command is used to upload local repository content to a remote repository. Pushing is how you transfer commits from your local repository to a remote repo.
Pushing is how you transfer commits from your local repository to a remote repo. It's the counterpart to git fetch, but whereas fetching imports commits to local branches, pushing exports commits to remote branches. Remote branches are configured using the git remote command. Pushing has the potential to overwrite changes, caution should be taken when pushing. 

The given example in the Screenshot describes:
one of the standard methods for publishing local contributions to the central repository. First, it makes sure your local master is up-to-date by fetching the central repository’s copy and rebasing your changes on top of them. The interactive rebase is also a good opportunity to clean up your commits before sharing them. Then, the git push command sends all of the commits on your local master to the central repository.

