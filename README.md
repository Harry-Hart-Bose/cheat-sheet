# cheat-sheet
A few git commands worth remembering

# Configuration Settings

## set up git to push only local branch by default:
git config --global push.default simple

## other settings
git config --global user.name "Mona Lisa"
git config --global user.email "email@example.com"

# Miscellaneous commands

## Transplant a branch onto another
git rebase --onto dest-branch branch-off-point current-devel-branch

## Add remote repository as destination
git remote add origin <git repository url>
git push --set-upstream origin master

## color-coded git branch list
git for-each-ref --sort=committerdate refs/heads/ --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(color:red)%(objectname:short)%(color:reset) - %(contents:subject) - %(authorname) (%(color:green)%(committerdate:relative)%(color:reset))'

## list branches which contain a particular commit
git branch -r --contains <commit> # includes remote branches, as well
git branch --contains <commit>

## set upstream tracking branch:
git branch --set-upstream-to=origin/<put your upstream branch name here> improve-systemstate-gtest

## to get rid of warnings that submodule contains changes:
git submodule update

## Git reset demystified
https://git-scm.com/book/en/v2/Git-Tools-Reset-Demystified
