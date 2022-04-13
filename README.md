# Git Cheatsheet
#### _How to use git_

This is more of a cheatsheet as a reminder/reference, rather than a tutorial. If you do not understand something, I suggest first checking out the links in the sources at the bottom of this file.

Also, this is a very beginner cheatsheet, since I am only getting started with git myself.

***
### Install git

If you don't have git installed already, install git using [Homebrew](https://brew.sh):

`brew install git`

### Initialising git
Open Terminal and change into the local repo folder using `cd`. Then initialise git:

`git init`

### Adding all files to git
`git add .`

### Commit changes
`git commit -m "message"`

### Create github repo
First create a new github repository and then run the following using the url of the repository:

`git remote add origin <url of repository>`

Where origin is the name of the remote. May be different in your case. 


### Push changes into your repo

`git push -u origin master`

Where origin is the name of the remote. May be different in your case. 


### Pushing changes to repo

`git push`

***

### See which repo you are currently in

`git remote show origin`

Where origin is the name of the remote. May be different in your case. 


### Check status/changes
At any time, you can check which files were modified by running:

`git status`

***

### Clone a repo

Copy the link for the repository from github and `cd` into the directory where you want to copy it. Then run:

`git clone <url of repository>`


### Pulling changes
If another dev makes a change to your repo, or you make changes to your repo online on Github, you can pull it down by running:

`git pull`


# Branches

The default branch used is `master` but you can create new branches. You can view which branch you are currently on by running:

`git status`

### Creating a branch

`git branch <name of branch>`

### Change branches

`git checkout <name of branch>`

### Merge branches
You can merge your other branch into the main master branch by running:

`git merge <name of branch>`

# Ignore

You can specify git to ignore certain files. First create a `.gitignore` file by running:

`touch .gitignore`

Open the file using a text editor and add the full name of the file with it's extension into separate lines of the file.

Then, save the file and publish changes:

`git add .gitignore`
`git commit -m "updated .gitignore"`
`git push`


### Ignoring mac .DS_Store files

For example, I used this method to ignore the very annoying `.DS_Store` file that appears on Mac for some reason.

If you don't have the `.gitignore` file already, you can create and add the file directly:

`echo .DS_Store >> .gitignore`

Then, save the file and publish changes:

`git add .gitignore`
`git commit -m "updated .gitignore"`
`git push`

### Adding a rule later

If you already have a file checked in, and you want to ignore it, Git will not ignore the file if you add a rule later. In those cases, you must untrack the file first.

So if you want add to ignore some directories in your local repository (which already exist) after editing `.gitignore` you want to run this on your root dir:

```
git rm --cached -r .
git add .
```

### Stage
Sometimes you may see: There are no staged changes to commit.
Would you like to stage all your changes and commit them directly?

The stage is files that you mark to commit when you run git add . 
If there are no files that you have marked to be on stage, this message will pop up. 

More details:
https://stackoverflow.com/questions/48545911/there-are-no-staged-changes-to-commit-dialog-box




***

### Sources

1. https://www.youtube.com/watch?v=SWYqp7iY_Tc
1. https://stackoverflow.com/questions/107701/how-can-i-remove-ds-store-files-from-a-git-repository
1. https://stackoverflow.com/questions/1470572/ignoring-any-bin-directory-on-a-git-project
