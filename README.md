# github-practice
GitHub practice for CSC 362

## Start (from the very beginning)
Begin by cloning this repository to your local computer. This code in this repository is located in the cloud at the moment. We want to make a local copy of the repository so that you can practice making edits to this local version, committing the edits to be shared, and then submitting a pull request to merge those edits and actually share them on GitHub.

To do this, first open VS Code to the home page. You can do this through VS Code's interface or through VS Code's command line -- I'll explain the command line. In the upper right corner of VS Code, click the terminal button:
![]()

In the terminal at the bottom of VS Code, type `ls`. This will show you all of the directories and files in your current working directory. Which directory is that? Type `pwd` to see where you are in the computer.

Let's download the repository code to this location on your computer. Back in the GitHub window, click the green "Code" button to access the drop down. Copy that `https://` link.

Back in the VS Code terminal, type:
`git clone` and paste the `https` link that you just copied then hit enter.
Example:
```
# Any line that starts with % is the command you enter (after the %)
% git clone https://github.com/kawilliams/github-practice.git
Cloning into 'github-practice'...
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (4/4), done.
```

Type `cd github-practice` to move into this new directory. If you type `ls` now, you should see the contents of the directory.

## Your Usual Start (once you're working in a repository)
Now that you have a local version of the code, we'll go through your typical workflow of making changes to your "workspace" and then submitting them to the public workspace. When you're working in a repository with a team (1 or more other people), you'll usually follow these steps:

  1. Pull any changes from the main branch, so that your local copy is up to date
  2. Create a new branch with the idea that you're working on
  3. Edit the code in your branch
  4. Commit the changes (meaning, save them in meaningful chunks)
  5. Once you've completed the task or need additional eyes on the changes, you push the changes to the remote repository and create a pull request
  6. The pull request is reviewed by someone on the team
  7. If all looks good, the teammate merges the pull request
  8. You can delete your branch once the changes are merged

### 1. Pull any changes
Start by checking what branch you have checked out to your local machine:
```
% git branch
* main
```
If any other branches exist, you'll see them displayed. Since we're on `main`, let's pull the latest changes from main to make sure our code is up to date:
```
git pull
```

### 2. Create a new branch
Let's make a new branch that is based on `main`. We want to make sure we are currently on `main` (that was step 1 with `git branch`). Since we are, any new branch we make will be based on the branch we are on -- which is what we want. We're going to add a file with your information in it, so call your branch something useful: `add-<name>-info` (where `<name>` is replaced with your first and last name:
```
git checkout -b add-katy-williams-info
```
The `checkout` command tells GitHub to switch to a different branch. The `-b` flag tells GitHub that we are switching to a new branch, and we provide the name of that new branch.

Now if you call `git branch`, you should see your new branch and a star (`*`) indicating we are on that branch.
```
% git branch
* add-katy-williams-info
  main
```

### 3. Edit the code in your branch.
In VS Code, make a new text file and call it `<name>.txt`, where you replace `<name>` with your first and last name.
Add the following content to your file and personlize it to make it yours:
```
My name is ____. I am a sophomore/junior/senior at Davidson College. I'm majoring in ____.

My favorite Dad joke or knock-knock joke is:
__________
```

Save your work.

### 4. Commit your changes.
To publish the changes you made, we need to use the `commit` command. There are two steps to this part: `add` the changed files and then `commit` the change. Think of commit as a benchmark for some work -- you completed an activity that takes a meaningful step forward. You may have several commits that make up a pull request, so commits don't need to solve the *whole* problem, just a meaningful step.

To add the changed files, first do:
```
git add .
```
The `add` command adds any changes to a new commit. If you don't specify which files and simply use the `.`, Git will add all of the changes within your current directory. If you want to specify each individual file, you can by doing `git add katy-williams.txt` if I wanted to only add my `katy-williams.txt` file to the commit.

Once you've added all of your files that contribute to the commit, you should use `commit` and write a useful (but short) message describing what this commit does:
```
git commit -m "Adds my joke file"
```
All together, your output should look like this:
```
git add %                                                                                                                   
 % git add .
 % git commit -m "Adding katy-williams.txt"
[add-katy-williams-info 758ea7c] Adding katy-williams.txt
 1 file changed, 6 insertions(+)
 create mode 100644 katy-williams.txt
```

