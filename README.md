# Mastery of Github
My all time git reference doc of Github

"Commands will only work when they are called upon in the designated directory."

### How to clone a repository onto a machine
cd ~/Path/to/file
git clone <url>             //Copied the repository into the path of a directory.
E.g. [      git clone https://github.com/ggiande/MacPuTTYPort.git      ]

### How to add files into an existing repository
```
cd ~/Path/of/local/repository

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

### Link a directory to a repository
1. Make an EMPTY repository on Github first
2. On a terminal run the following commands

This deletes .git if previously initialized in this directory
```
WINDOWS: rd .git /S/Q
MACOSX: rmdir -r .git /S/Q              // ./S/Q doesn't always work so it may not be needed.
```

```
<!-- Initiates an empty git tracking repository in our local directory -->
git init

<!-- Stages all unknown/modified files for commiting -->
git add .

<!-- Commits our staged files and annotates a description of the commit -->
git commit -m "First commit."

<!-- Addes a new remote origin, linking to a git repo -->
git remote add origin <url>

<!--  -->
git push -u origin main   //should work if repository is EMPTY
    OR
git push -f origin master       //if repository not empty, this will overwrite EVERYTHING and only push the things under .add
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

Author: Giancarlo Garcia Deleon