# Git on Teams

## Git in the final projects

In the final projects you will have to manage a Git repository to work all the Team together, there are many ways to do it, but these are our recommendations:

* **Separate front-end and back-end code:** Create one repository for the back-end code and another one for the front-end code, or in the same repository create a folder for the back-end and a different folder for the front-end, but take into account to manage the folders and package.json properly without breaking others work
* **One Team, One Repo:** Create the repositories in the account of one member of the team, and grant the others students to work there. The other members should clone directly the repository, DO NOT FORK IT! if you fork it every member of the team will work in an independent repository adding difficulties to manage merges of work
  * To give push privileges to other team members, go to your repository in GitHub, and click Settings->Manage access -> Invite a collaborator
* **Use a Git strategy:** once you divide your work in different functionalities and are assigned to team members, to reduce the number of merges and do not involve everybody in the common files, you should have a strategy to work
* **Assign a Git Release Manager:** Assign a member of the team that knows all the code structure and will be the best member to join all functionalities together. The Migracode Team and mentors will help this member to solve conflicts and manage the versions of the project.
* **Use gitignore:** Check this [link](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)

## Small Teams&#x20;

### Git strategy

There are strategies with more branches and more structured, like the common strategy in companies, but taking into account number of people, the criticality of our software and to not spend many hours merging. We recommend you this strategy for the final project!

* 3 type of branches: _master_, _develop_ and _developers_ branches
* 2 user roles: _Release Manager_ and _Developer_

![](<../.gitbook/assets/image (19).png>)

**Branches:**

* _**master**_: The master branch stores the official release history, the versions that we will show to the client or to the class after each sprint.
* _**develop**_: The develop branch serves as an integration branch for features. Once develop has acquired enough features for a release, those will be tested before merge it with master.
* _**developer**_** branches**: Each new developer has a branch with their name, as _dev-john_ or _john_. _developer_ branches are created from _develop_ and the developer will always work there.

**Roles:**

* **Release Manager**: is the one that manages _master_ and _develop_. This user, that at the same time is a Developer, do all merges between developers branches and _develop_. Also is the one that creates versions in _master_.
* **Developer**: all the members on the team are developers, they develop the assigned features in the branch.



### Main actions and commands

**First steps:**

**Create the repositories (Release Manager):**

* Create and add write and push privileges to all developers
* Create a new branch develop from master:
  * `git checkout master` be sure you are on master branch
  * `git checkout -b develop` Create the branch _develop_ from _master_
  * `git push -u origin develop` Push the local branch to remote, so it is published on Github and other members can see it
* Create a new branch for each developer from develop:
  * `git checkout -b dev_john`
  * `git push -u origin develop`

**Move to working repositories (all developers):**

* Each developer should get the new branches from remote and move to the assigned branch:
  * `git fetch --all` Get all new branches created
  * `git checkout dev_john` Move yo your name branch

**Daily work:**

* All developers should commit and push all your work
  * `git add .`
  * `git commit -m "new feature"`
  * `git push`

**End of a sprint:**

**Create the sprint version (Release Manager):**

* `git checkout develop`
* `git fetch --all`
* Merge develop branch with the branch of each developer
  * `git merge dev_john`
  * `git add .`
  * `git commit -m "merge with john"`
  * `git push`
* Check that all functionalities are working together, have a meeting to check the version and fix all integration or merge problems
* As a closed version, move the code to _master_:
  * `git checkout master`
  * `git merge develop`
  * `git add .`
  * `git commit -m "merge with john"`
  * `git push`
* Go back to your working branch
  * `git checkout dev_me`

**Update your working branches with last version (all developers)**

* `git fetch --all` to get last version of all branches
* `git merge develop`
* `git add .`
* `git commit -m "merge with develop"`
* `git push`

## Main companies

Here you can find an example on how to manage planned and unplanned (with bugs) versions of a software. [More information](https://nvie.com/posts/a-successful-git-branching-model/)

![](<../.gitbook/assets/image (176).png>)

* _**master**_: The master branch stores the official release history, for each published version a tag is assigned with a version number
* _**hotfix**_: is the branch we use to fix bugs from the published version as soon as possible, without adding new features. As we can see in v0.1 version the software has a bug, we fix it in the Hotfix branch, and then we merge it directly with master. Also this change is added to develop branch for future versions.
* _**release-xxx**_: release branches are created from develop, to have a version that should be tested in detail to become a new version, if during the test some bugs are found are fix directly in this branch. xxx is the name o the release
* _**develop**_: The develop branch serves as an integration branch for features. Once develop has acquired enough features for a release, a new release branch is created to test it before go to master.
* _**feature-xxx**_: Each new feature with name xxx, should reside in its own branch. But, instead of branching off of master, feature branches use develop as their parent branch. When a feature is complete, it gets merged back into develop. Features should never interact directly with master.
