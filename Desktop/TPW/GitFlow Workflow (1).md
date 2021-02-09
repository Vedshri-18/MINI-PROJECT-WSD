# GitFlow Workflow
A Git Workflow is a recommendation for how to use Git to accomplish work in a consistent and productive manner.

# *What is a successful Git workflow?*
When evaluating a workflow for your team, it's most important that you consider your team’s culture. Some things to consider when evaluating a Git workflow are:
 
*  Does this workflow scale with team size?
* Is it easy to undo mistakes and errors with this workflow?
* Does this workflow impose any new unnecessary cognitive overhead to the team?

# *How the GitFlow works*
https://wac-cdn.atlassian.com/dam/jcr:2bef0bef-22bc-4485-94b9-a9422f70f11c/02%20(2).svg?cdnVersion=1446


* *Develop and Master Branches*

Instead of a single master branch, this workflow uses two branches to record the history of the project. The master branch stores the official release history, and the develop branch serves as an integration branch for features. It's also convenient to tag all commits in the master branch with a version number. The first step is to complement the default master with a develop branch. A simple way to do this is for one developer to create an empty develop branch locally and push it to the server:

 * git branch develop

* git push -u origin develop

This branch will contain the complete history of the project, whereas master will contain an abridged version. 

 * *Feature Branches*

 Each new feature should reside in its own branch, which can be pushed to the central repository for backup/collaboration. But, instead of branching off of master, feature branches use develop as their parent branch. When a feature is complete, it gets merged back into develop. Features should never interact directly with master.
 https://wac-cdn.atlassian.com/dam/jcr:b5259cce-6245-49f2-b89b-9871f9ee3fa4/03%20(2).svg?cdnVersion=1446

 Note that feature branches combined with the develop branch is, for all intents and purposes, the Feature Branch Workflow. But, the Gitflow Workflow doesn’t stop there.

 # *Creating a feature branch*

Without the git-flow extensions:
 
* git checkout develop 

* git checkout -b feature_branch


When using the git-flow extension:

* git flow feature start feature_branch



# *Finishing a feature branch*

When you’re done with the development work on the feature, the next step is to merge the feature_branch into develop.


Without the git-flow extensions:

* git checkout develop git merge feature_branch


Using the git-flow extensions:

* git flow feature finish feature_branch


# *Release Branches*

https://wac-cdn.atlassian.com/dam/jcr:a9cea7b7-23c3-41a7-a4e0-affa053d9ea7/04%20(1).svg?cdnVersion=1446

Once develop has acquired enough features for a release (or a predetermined release date is approaching), you fork a release branch off of develop. Creating this branch starts the next release cycle, so no new features can be added after this point—only bug fixes, documentation generation, and other release-oriented tasks should go in this branch. Once it's ready to ship, the release branch gets merged into master and tagged with a version number. In addition, it should be merged back into develop, which may have progressed since the release was initiated.

Using a dedicated branch to prepare releases makes it possible for one team to polish the current release while another team continues working on features for the next release. 

Making release branches is another straightforward branching operation. Like feature branches, release branches are based on the develop branch. A new release branch can be created using the following methods.


Without the git-flow extensions:

* git checkout develop git checkout -b release/0.1.0


When using the git-flow extensions:

* $ git flow release start 0.1.0 Switched to a new branch 'release/0.1.0'

Once the release is ready to ship, it will get merged it into master and develop, then the release branch will be deleted. It’s important to merge back into develop.

To finish a release branch, use the following methods:

Without the git-flow extensions:

>* git checkout master git merge release/0.1.0

 With the git-flow extension:

* git flow release finish '0.1.0'


# *Hotfix Branches*

https://wac-cdn.atlassian.com/dam/jcr:61ccc620-5249-4338-be66-94d563f2843c/05%20(2).svg?cdnVersion=1446

Maintenance or “hotfix” branches are used to quickly patch production releases. Hotfix branches are a lot like release branches and feature branches except they're based on master instead of develop. This is the only branch that should fork directly off of master. As soon as the fix is complete, it should be merged into both master and develop (or the current release branch), and master should be tagged with an updated version number.

Having a dedicated line of development for bug fixes lets your team address issues without interrupting the rest of the workflow or waiting for the next release cycle. You can think of maintenance branches as ad hoc release branches that work directly with master. A hotfix branch can be created using the following methods:


Without the git-flow extensions:

* git checkout master git checkout -b hotfix_branch

When using the git-flow extensions: 

* $ git flow hotfix start hotfix_branch

Similar to finishing a release branch, a hotfix branch gets merged into both master and develop.

* git checkout master git merge hotfix_branch git checkout develop git merge hotfix_branch git branch -D hotfix_branch

* $ git flow hotfix finish hotfix_branch

# Example

A complete example demonstrating a Feature Branch Flow is as follows. Assuming we have a repo setup with a master branch.

* git checkout master

* git checkout -b develop

 * git checkout -b feature_branch

* #work happens on feature branch

* git checkout develop

* git merge feature_branch

* git checkout master

* git merge develop

* git branch -d feature_branch>

# Summary

 Gitflow is one of many styles of Git workflows you and your team can utilize.
Some key takeaways to know about Gitflow are:

* The workflow is great for a release-based software workflow.
* Gitflow offers a dedicated channel for hotfixes to production.

The overall flow of Gitflow is:
* A develop branch is created from master

* A release branch is created from develop

* Feature branches are created from develop
* When a feature is complete it is merged into the develop branch
* When the release branch is done it is merged into develop and master
* If an issue in master is detected a hotfix branch is created from master
* Once the hotfix is complete it is merged to both develop and master
