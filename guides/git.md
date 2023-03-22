# Introduction to GIT

## Github Basics <a href="#github-basics" id="github-basics"></a>

### Create a new project in Github <a href="#create-a-new-project-in-github" id="create-a-new-project-in-github"></a>

See the comlete tutorial on [Github: Create a repo](https://docs.github.com/en/github/getting-started-with-github/create-a-repo)

Instead of cloning the repo that you created in Github, you can also initiallize the repo using the command line/terminal by followint the [Add a project using the command line](https://docs.github.com/en/github/importing-your-projects-to-github/adding-an-existing-project-to-github-using-the-command-line)

### Fork and Clone an existing project from Github <a href="#fork-and-clone-an-existing-project-from-github" id="fork-and-clone-an-existing-project-from-github"></a>

We use fork to copy an existing Github repository into out Github account We use clone to copy an existing Github repository into our laptop If we don't fork first, for sure we can clone any repository from others, but if they don't give privileges we will not be able to push the changes, that's why we always fork the repositories

**To fork a repo:**

Firstly you need to click the "Fork" button:

![](<../.gitbook/assets/image (2).png>)

Then you should be brought to your new fork (notice how the repo title changes):

![](<../.gitbook/assets/image (68).png>)

**To clone a repo:**

Now you can clone from your fork by copying the URL here:

![](<../.gitbook/assets/image (93).png>)

The command to clone is:

```
git clone URL_YOU_JUST_COPIED
```

### Basic Git commands <a href="#basic-git-commands" id="basic-git-commands"></a>

#### Commit and push your changes to Github

Once you have your repository, and you do the first changes in the code, do the following instructions to save and push to Github your work:

* `git add .` // track changes on files (create, remove, modify)
* `git commit -m “message”` // save changes
* `git push` // upload your commits from origin (your laptop) to the remote (Github) in branch master (the default)

If you are working with the terminal, before execute the commands, are you in the right repository folder? We can have different folders, each one for a different repository.

#### Configuration commands

* `git config --global user.name "John Doe"`
* `git config --global user.email johndoe@example.com`
* `git config --list`

#### Commands to create a project

* `git init *project name*` //initialize GIT repository in an empty directory (locally)
* `git add .` //track changes on files (create, remove, modify)
* `git commit -m “message”` //save changes
* `git remote add origin *https://github.com/yourusername/yourrepo*`
* `git push -u origin master` //upload origin (my laptop) to the server in branch
* `git status` //show current status
* `git clone *url*` //download files from URL with a file .git



### Remote <a href="#remote" id="remote"></a>

Git has a concept of a "remote". These are other git repositories that can be connected to over the internet. You can push or pull code changes from them. Remotes have a _name_ and a _URL_.

All the remotes that you will use at Migracode are hosted on GitHub, so have a github.com URL.

When you clone a repo from GitHub, the default remote is named `origin` and the URL is set to that of the GitHub repo.

You can view the remotes you have set up with:

```
git remote -v
```

#### Adding a Remote

Follow these instructions if you are getting an permission error when pushing your changes. If you have cloned the original repo _before_ forking, you'll need to follow these instructions. You can check this by running `git remote -v`. If the output looks something like:

```
origin git@github.com:CodeYourFuture/css-skin.git (fetch)
origin git@github.com:CodeYourFuture/css-skin.git (push)
```

then you have cloned before forking. The key is that the `origin` remote is pointing to a CodeYourFuture URL. Don't worry, we can fix it!

The first step is to fork the original repo. Follow the first 2 steps from [forking instructions](https://migracode-barcelona.github.io/syllabus/others/git.html#how-to-fork-a-github-repo) above.

Now, instead of cloning the fork (you have already cloned), you need to add it as a remote.

Run:

```
git remote add fork URL_YOU_COPIED_FROM_FORK
```

This will add a new remote called `fork` that points to your new fork. To check this, run `git remote -v` again. You should see both the `origin` and `fork` remotes.

Now that you have your `fork` remote you can push to it (instead of the `origin` remote, which will error) by running:

```
git push fork
```

You'll need to remember to add the `fork` _every time you push_.



## Other Github functionalities

### Publish your website in Github.io with GitHub Pages

1. Now all that remains is to publish your website! In your repository `http://github.com/your-username/your-repository-name`, you can find the settings icon in the top right corner:&#x20;

![](<../.gitbook/assets/image (92).png>)

**2.** Find the section named Github Pages and select "main branch" under 'Source', then hit "Save".

![](<../.gitbook/assets/image (124).png>)

**3.** Wait a few minutes, then refresh the page and come back to the Github Pages section. Now you should see a green bar saying "Your site is published at `http://github.com/your-username/your-repository-name`". Click the link, verify that your website is there, then share it with your class!



### Making a Pull Request (PR)

So you've done your homework, you've committed your changes and are ready to make a PR. Congrats! 🎉🎉🎉

At this point you should have followed the instructions either to [fork the original repo](https://migracode-barcelona.github.io/syllabus/others/git.html#how-to-fork-a-github-repo) or [added a remote to your fork](https://migracode-barcelona.github.io/syllabus/others/git.html#adding-a-remote). If you haven't make sure you read those sections first.

You will need to push to your fork. If you forked and then cloned (as in the [how to fork instructions](https://migracode-barcelona.github.io/syllabus/others/git.html#how-to-fork-a-github-repo)) then you just need to run `git push`. If you [added a remote to your fork](https://migracode-barcelona.github.io/syllabus/others/git.html#adding-a-remote), then you will need to run `git push fork`.

Next you need to go the original repo in your browser (probably starting with [https://github.com/CodeYourFuture](https://github.com/CodeYourFuture)). Next click the Pull Requests tab:

![](<../.gitbook/assets/image (10).png>)

Then click the New pull request button:

![](<../.gitbook/assets/image (154).png>)

Then click the "compare across forks" link:

![](<../.gitbook/assets/image (98).png>)

Then click the "head fork" dropdown button:

![](<../.gitbook/assets/image (123).png>)

Then find your fork in the list and click it:

![](<../.gitbook/assets/image (141).png>)

Then click the Create pull request button:

![](<../.gitbook/assets/image (1).png>)

Almost there! Now fill out the PR form. Give it a sensible title and an (optional) description:

![](<../.gitbook/assets/image (56).png>)

And finally click the Create pull request button at the bottom of the form:

![](<../.gitbook/assets/image (61).png>)

That's it! You created your PR!

![](<../.gitbook/assets/image (101).png>)

## Advanced

### Git Branching <a href="#git-branching" id="git-branching"></a>

You have been using git to track the changes you make to your exercises project. Each time you commit, you save a copy of your files.

![](<../.gitbook/assets/image (119).png>)

When you create a new branch, you create a separate line of commits.

![](<../.gitbook/assets/image (18).png>)

With branches, you can work on two copies of your project and switch back and forth.

![](<../.gitbook/assets/image (33).png>)

Complete exercise 9 from the [exercise project](https://github.com/Migracode-Barcelona/html-css-git-exercises) to learn how to use git branches.

> If you want to go deeper, read this article on [how git branching works](https://www.atlassian.com/git/tutorials/using-branches).

### Git Merging <a href="#git-merging" id="git-merging"></a>

Last week you used Git to create a branch so that you could work on two different copies of your project at the same time.

![](<../.gitbook/assets/image (145).png>)

This week you will learn how to merge your changes in one branch back to your master branch.

![](<../.gitbook/assets/image (43).png>)

Complete exercise 18 from the [exercise project](https://github.com/Migracode-Barcelona/html-css-git-exercises).

### Git Merge Conflicts <a href="#git-merge-conflicts" id="git-merge-conflicts"></a>

Last week you used Git to merge your changes from one branch back into your master branch.

![](<../.gitbook/assets/image (12).png>)

Sometimes Git can not automatically merge one branch into another, because each branch has modified the same line of code. Git does not know which version of the line is the correct one. When this happens, we have a "merge conflict".

![](<../.gitbook/assets/image (150).png>)

As a developer, you have to tell Git which version of the line of code is correct.

Complete exercise 28 from week 3 of the [HTML, CSS and Git Exercises](https://github.com/Migracode-Barcelona/html-css-git-exercises) to learn how to resolve a merge conflict.

[https://www.atlassian.com/git/tutorials/using-branches/merge-conflicts](https://www.atlassian.com/git/tutorials/using-branches/merge-conflicts)

### Git Conflicts <a href="#git-conflicts" id="git-conflicts"></a>

As a professional, you'll usually need to work alongside other coders to build an app or website. We use version control to coordinate changes and manage any conflicts that arise. [Git](https://git-scm.com/) is a version control system which helps us merge code that we've been working on separately into one common codebase.

To manage conflicts, we will need a common code base in which all changes are coordinated. When working on our own, we'll make our changes in `branches` to keep the code separate. Then we'll learn how to refresh your individual `branch` with the common code base, and prepare your changes to be merged.

> Exercise: Get together in pairs and select a "leader". The leader should fork [this repository](https://github.com/CodeYourFuture/first-git-conflict) to their GitHub account. The other person should then fork the leader's repository. Both students should then clone their own personal forks locally.

Now that you have the project set up on your computer, you need a place to safely make changes without effecting the common code base. To do this, we'll navigate to our project in the Terminal and create a new branch:

```
cd <your-project-directory>
git checkout -b my-first-branch
```

When you commit changes on this branch, your changes will be saved separately from the common code base. This way both team members can make changes at the same time.

> Exercise: Add your name and a sentence about yourself to the `index.html` file. Then `git add` and `git commit` to commit to your personal branch.

Now you have two branches: `master` and `my-first-branch`. These branches have _diverged_, which means you have changes in one that don't appear in the other. You can check this by running `git checkout master`, then looking at your `index.html` file.

When you're done, run `git checkout my-first-branch` to go back to the branch with your changes. Git saves your changes in both branches and lets you switch between them. That's why we call it "version control". It saves different versions so you can switch between them.

Right now, your new branch only exists on your computer. Let's push it up to GitHub so you can see it in your profile.

```
git checkout my-first-branch
git push -u origin my-first-branch
```

Now both students in each pair, the "leader" and the other student, should have branches with changes. Now let's try to merge these changes together into the "leader's" master branch.

> Exercise: Browse to the "leader's" GitHub repository and open a new Pull Request. The Pull Request should ask to merge your `my-first-branch` branch into the "leader's" `master` branch. Ask a mentor for help if you have trouble figuring out how to issue a Pull Request. When both students have issued a Pull Request to the correct place, merge _one_ of them but not the other.

Congrats, you've merged one student's changes with the common code base in the `master` branch. If you check the other Pull Request, you'll see you have a problem. It can't be merged automatically because there's a conflict. Why?

Conflicts emerge whenever the same file has been edited, and git can't determine what changes should be kept and what changes should be discarded. A human -- that's you -- needs to step in and sort it out. To help us, git writes into our code so we can see where it is confused. Here's an example of a merge conflict in our code:

```
<<<<<<<  HEAD
+   <h2>Mozafar</h2>
+   <p>I am a mentor at CodeYourFuture.</p>
=======
-   <h2>Daniel</h2>
-   <p>I like to ride bikes</p>
>>>>>>> my-first-branch
```

To resolve a conflict, we decide which lines to keep and which lines to remove. When we're done, we remove the extra lines that git added (`<<<<< HEAD`, `========` and `>>>>>>>`).

Let's see how we can resolve this conflict with your branches. First we need to fetch the latest changes from the leader's `master` branch. If you're the **leader**, just do:

```
git checkout master
git pull
```

If you're the **other student**, you need to set up the remote and pull from that master:

```
git checkout master
git remote add upstream <your-leaders-git-repository-url>
git pull upstream master
```

Now everyone's `master` branch should include the Pull Request that was merged. Whichever student still needs to get their Pull Request merged can bring those changes into their branch like this:

```
git checkout my-first-branch
git merge master
```

You probably received a **merge conflict**.

> Exercise: Follow the steps we discussed before about how to resolve a merge conflict by editing the file. Make sure both students changes are included in the final version. When you're done, use `git add`, `git commit` and `git push` to share your changes with GitHub. If everything has gone correctly, you can now merge the Pull Request.

Now everyone can sync their changes. If you're the **leader**, just do:

```
git checkout master
git pull
```

If you're the **other student**, do this:

```
git checkout master
git pull upstream master
```

> Exercise: As a group, discuss why the `git pull` command is different for the **leader** and the **other student**.
>
> Exercise: Try to do the pull requests again, but this time switch the pull requests so that the other student must manage the merge conflict.

If you're feeling confused, don't worry. Version control is one of the most difficult things you'll learn and we'll be going over it again and again and again.

### Merging and advanced Git commands <a href="#merging-and-advanced-git-commands" id="merging-and-advanced-git-commands"></a>

* `git fetch` //fetch latest changes from origin and all branches (no merge)
* `git pull` //fetch latest changes from origin and all branches (with merge)
* `git merge`

Branches:

* `git branch test` //creates a new local branch
* `git checkout test` //move to branch test
* `git checkout master` //move to branch master
* `git checkout -b test` //create a new local branch and move into it
* `git push origin test` //push the branch and all commits to the server
* `git branch -d test` //remove a local branch
* `git checkout -b test origin/test`
* `git fetch --all` //to get all branches from server

