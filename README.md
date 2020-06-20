# How to use git

I'm following Traversy's tutorial on git for beginners:
https://www.youtube.com/watch?v=SWYqp7iY_Tc

### cd
first cd into the local repo folder

### initialises git
git init

### adds all the files
git add .

### commit the changes with a message
git commit -m "tutorial"

### create github repo then run this to initialise
git remote add origin <url of repository>

### push the changes into your repo
git push -u origin master

(not sure what the -u flag does)

### check status/changes
git status

### once you've added your repo, can just run
git push

### clone a repository
copy the link for the repo and cd into the dir you want to copy it then run:

git clone <url>

e.g. for this repo:

git clone https://github.com/abhiyanbeta/gittest.git

### pulling
if another dev makes a change to your repo, you can pull it down by running:

git pull


# Branches

The default branch used is 'master' but you can create new branches. You can view which branch you are currently on by running:

git status

### creating a branch
git branch <name of branch>

### change branches
git checkout <name of branch>

### merge Branches
You can merge your other branch into the main master branch by running:

git merge <name of branch>
