# Mastery of Github
My all time git reference document

"Commands will only work when they are called upon in the designated directory."
### .gitignore
Creates the file to ignore designated files/extensions from being published.
```
<!-- Create a .gitignore file in a repo -->
touch .gitignore
start .gitignore
```
### How to clone a repository onto a machine
```
cd ./Path/to/directory/of/choice

<!-- Paste the url of the repository to clone the repo into the directory -->
git clone <url>
```

### How to add files into an existing repository
```
cd ~/Path/of/local/repository
<!-- Create an empty git repository in this directory -->
git init

<!-- Syncs the filename up to our machine -->
git add <filename>          

<!-- Stages all files on the branch for commiting -->
git add .          

<!-- Adds a commit messages to staged changes  -->
git commit -m "Brief Description" 

<!-- Pushes our code up to our git remote -->
git push               

<!-- Pulls everything from the repository's server that is new into our branch -->
    OPTIONALLY
git pull                 //pulls everything from the repository that is new | Updating
```
### How to remove git init from ANY directory
```
<!-- These terminal commands delete .git if previously initialized in this directory -->
WINDOWS: rm -r -f .git/
MACOSX: rmdir -r .git/
```
### Link a directory to a repository
1. Make an EMPTY repository on your prefered git hosted site
2. On a terminal run the following commands
```
<!-- Initiates an empty git tracking repository in our local directory -->
git init

<!-- Stages all unknown/modified files for commiting -->
git add .

<!-- Commits our staged files and annotates a description of the commit -->
git commit -m "First commit."

<!-- Addes a new remote origin, linking to a git repo -->
git remote add origin <url>

<!-- Pushes our commit to the remote -->
git push -u origin main
```
## Branching
A branch on git is simply a lightweight movable pointer to one of the repositorie's commits.
### Create new branches
```
<!-- Creates a new branch given a name -->
git branch name

<!-- Changes to a branch given a name -->
git checkout name

<!-- Creates a new branch given a name and changes to a branch given a name -->
git checkout -b name

<!-- Shows all branches related to the repository -->
git branch -r 

```
Understanding Branching

### git repository of subfolders
If subfolder is from another repository, we must remove .git/ from the directory. We do so by running ```rm -r -f .git/``` Make note that ```-f``` forces for these changes to occur. 

Author: Giancarlo Garcia Deleon
