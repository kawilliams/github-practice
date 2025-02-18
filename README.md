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

