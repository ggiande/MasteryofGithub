# Mastery of Github
My all time git reference doc of Github

"Commands will only work when they are called upon in the designated directory."

### HOW TO CLONE A REPOSITORY ONTO MACHINE
cd ~/Path/to/file
git clone <url>             //Copied the repository into the path of a directory.
E.g. [      git clone https://github.com/ggiande/MacPuTTYPort.git      ]

### HOW TO ADD FILES INTO AN EXISTING REPOSITORY
cd ~/Path/of/local/repository
git add <filename>          //this syncs the filename up to our machine
    OR
git add .           //adds all files onto the branch

git commit -m "Brief Description" //still in machine, not synced up
git push               //pushes up to github.com
    OPTIONALLY
git pull                 //pulls everything from the repository that is new | Updating


### Link a directory to a repository
1. Make an EMPTY repository on Github first
2. On a terminal run the following commands

This deletes .git if previously initialized in this directory
```
WINDOWS: rd .git /S/Q
MACOSX: rmdir -r .git /S/Q              // ./S/Q doesn't always work so it may not be needed.
```
```
git init
git add .
git commit -m "First commit."
git remote add origin <url>

git push -u origin main   //should work if repository is EMPTY
    OR
git push -f origin master       //if repository not empty, this will overwrite EVERYTHING and only push the things under .add
```

## Branching
A branch in Git is simply a lightweight movable pointer to one of the repositories commits.
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