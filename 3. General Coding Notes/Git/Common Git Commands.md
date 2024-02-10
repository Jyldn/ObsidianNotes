# Terminology
## Pull
To fetch the latest changes from one repository and merge those changes into the one you're working with. When you *pull*, you are bringing the most recent changes from an external repository to the current one.
## Push
To send your current repository changes to another repository. This is how you share your work with others or save it to a remote backup, such as on GitHub. All your local changes are moved to an external repository.
## Pull Request
Inform others working on some repository that you'd like to merge your changes to the one they're working on. To do this, you push your changes to a branch on the project repository and then submit the pull request. This tells people that you'd like them to review the changes you made and consider merging them into some other branch, most commonly the main branch. 

It is like saying: "Please *pull* my changes, those which I have pushed to this branch, into your branch."
## Branch
A branch in Git is like an independent line of development. You can think of them as a way to request a brand new working directory, staging area, and project history. New branches can be created and switched between, and changes can be merged from one branch to another.

## Commit
A commit, or "revision", is an individual change to a file (or set of files). When you make a commit, you're telling Git to record a snapshot of your repository at that point in time. Commits can be thought of as checkpoints in the development process which you can return to later if needed.

## Fork
A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project.

## Fetch
This command downloads commits, files, and refs from a remote repository into your local repo. Fetching is what you do when you want to see what everybody else has been working on.

## Stash
Stashing takes your modified tracked files and saves them on a stack of unfinished changes that you can reapply at any time.
# Commands
- **git commit -am "message"**
  Adds all current files to the commit.
- **git config --global alias.ac "commit -am"**
  Creates an alias. In the example, 'ac' now works as shorthand for 'commit -am'.
  Example: $ git ac "noice"
- **git revert pre-fuckup**
  Revert the project to a previous state.
  Does not remove the original commit from history.