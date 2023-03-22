# Git and GitHub Practice Session

## Assignment

In this project, we’ll walk through the basic Git workflow that you will use in all your projects.

**Create the Repository**

1. Create a new repository by clicking the button shown in the screenshot below.

![](<../../../../.gitbook/assets/image (91).png>)

&#x20;**2.** Give your repository the name “git\_test” in the repository name input field, and create the repository by clicking the green “Create repository” button at the bottom of the page.

**3.** This will redirect you to your new repository on GitHub. To copy this repository onto your local machine, select the HTTPS option and copy the line next to it.

![](<../../../../.gitbook/assets/image (196).png>)

**4.** In the command line on your local machine, navigate to where you want to store this project, and then clone your repository on GitHub onto your computer with `git clone` followed by the URL you copied in the last step. The full command should look similar to `git clone https://github.com/USER-NAME/REPOSITORY-NAME.git`.

**Note:** In the image below SSH link is used instead of HTTPS which is not important for us at this point. You can continue with HTTPS link.

![](<../../../../.gitbook/assets/image (158).png>)

**5.** That’s it! You have successfully connected the repository you created on GitHub to your local machine. To test this, you can `cd` into the new **git\_test** folder that was downloaded and then enter `git remote -v` in your command line. This will display the URL of the repository you created in GitHub, which is the remote for your local copy. You may have also noticed the word **origin** at the start of the `git remote -v` output, which is the name of your remote connection. The name “origin” is both the default and the convention for the remote repository, but it could have just as easily been named “party-parrot” or “dancing-banana”. (Don’t worry about the details of origin for now; it will come up again near the end of this tutorial.)&#x20;

![](<../../../../.gitbook/assets/image (109).png>)

**Use the Git Workflow**

Create a new file in the `git_test` folder called “README.md” with the command `touch README.md`.

![](<../../../../.gitbook/assets/image (181).png>)

Type `git status` in your terminal. In the output, notice that your README.md file is shown in red, which means that this file is not staged.

![](<../../../../.gitbook/assets/image (100).png>)

Type `git add README.md`. This command adds your README.md file to the staging area in Git. Now, type `git status` again. In the output, notice that your file is now shown in green, which means that this file is now in the staging area.

![](<../../../../.gitbook/assets/image (170).png>)

Type `git commit -m "Add README.md"` and then type `git status` once more. The output should now say, “_nothing to commit, working tree clean_”, indicating that your changes have been committed. Don’t worry about the `upstream is gone` message you may see, this is totally normal and only showing because your cloned repository currently has no branches. It will be resolved once you have followed the rest of the steps in this project.

![](<../../../../.gitbook/assets/image (208).png>)

Type `git log` and look at the output. You should see an entry for your “Add README.md” commit. You will also see details on the author who made the commit and the date and time for when the commit was made.

**Add Another File**

Create a new file in the `git_test` folder called `hello_world.txt`. In the terminal, type `git status`, and notice `hello_world.txt` is not staged.

![](<../../../../.gitbook/assets/image (77).png>)

Open README.md in your text editor of choice and add the text “This is (YourUsername)’s first git project!” and then save the file.

![](<../../../../.gitbook/assets/image (219).png>)

Back in your terminal, type `git status`, and notice that README.md is now shown as modified, and not staged or committed. This is because you made a change to it, and it is already a tracked file.

![](<../../../../.gitbook/assets/image (183).png>)

Add README.md to the staging area with `git add README.md`.

Can you guess what `git status` will output now? README.md will be displayed in green text, while hello\_world.txt will still be in red. This means that only README.md has been added to the staging area.

![](<../../../../.gitbook/assets/image (106).png>)

Now, add hello\_world.txt to the staging area with a slightly different command: `git add .`, where the full stop means to add all files **in the current directory** that are not staged. Then, type `git status` once more, and everything should now be in the staging area. _(Note: You can use `git add -A` to add ALL unstaged files to the staging area within the repository)_

![](<../../../../.gitbook/assets/image (193).png>)

Finally, let’s commit all of the files that are in the staging area and add a descriptive commit message `git commit -m "Add hello_world.txt and edit README.md"`. Then, type `git status` once again, which will output “_nothing to commit_”.

![](<../../../../.gitbook/assets/image (41).png>)

Take one last look at your commit history by typing `git log`. You should now see two entries.

**Push Your Work to GitHub**

Finally, let’s upload your work to the GitHub repository you created at the start of this tutorial.

Type `git push origin main`.

![](<../../../../.gitbook/assets/image (42).png>)

Type `git status` one final time. It should output “_nothing to commit, working tree clean_”.

![](<../../../../.gitbook/assets/image (122).png>)

When you reload the repository on GitHub, you should see the README.md and hello\_world.txt files that you just pushed there from your local machine.

![](<../../../../.gitbook/assets/image (221).png>)

### Conclusion

The main take away from the past lessons is how to use Git and GitHub for your projects. You now have this very powerful skill that will help you immensely when we get into the coding projects. You will be able to share your work with others for code reviews and to get help with your code if you’re stuck.

### Extra Practice

Follow the instructions on this [link](https://github.com/Migracode-Barcelona/learn-git) for more practice.
