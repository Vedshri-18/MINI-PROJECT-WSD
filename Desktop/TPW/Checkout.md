Checkout.md
## *Checkout*
In Git, the term checkout is used for the act of switching between different versions of a target entity. The git checkout command is used to switch between branches in a repository. Be careful with your staged files and commits when switching between branches.

The git checkout command operates upon three different entities which are files, commits, and branches. Sometimes this command can be dangerous because there is no undo option available on this command.

It checks the branches and updates the files in the working directory to match the version already available in that branch, and it forwards the updates to Git to save all new commit in that branch.
You can demonstrate how to view a list of available branches by executing the git branch command and switch to a specified branch.

To demonstrate available branches in repository, use the below command:

 $ git branch  
Now, you have the list of available branches. To switch between branches, use the below command.

Syntax:

 $ git checkout <branchname> 