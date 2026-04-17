# GIT commands

## setup and config

	git config --global user.name   # sets username 

	git config --global user.email   # sets email

## Basic workflow

	git init  # initialize repository a git repository
	
	git add  #  stage the changes 

 	git commit -m "any message"  # saves the staged changes

## Viewing changes

	git status # check status

	git log --oneline # view log history in one line

## Checking out to the existing branch

	git checkout feature

## creating and checking out the branch

	git checkout -b feature-test

## Viewing last commit history details

 	git show

## Wants to reset to particular commit and delete the commit history & should have local changes staged.

    git reset --sotf HEAD~1 # one commit back

## Should not have local changes staged ( Unstaged ), and want to reset to particular commit

    git reset --mixed HEAD~1 # one commit back & unstaged changes

## Should not have local changes at all and reset to particular commit

    git reset --hard HEAD~1 # deletes all the things its gone completely

## Revert to particular commit but keep all the commit history as it is ?

    git revert <commit-id> # this creates new commit and keep all history.

## Additional , what if you resert --hard but want your changes back?

    git reflog # shows all logs and then you can mention the Id in git reset --hard <commit-ID>


## Rebase

        git rebase main  # rebase current branch onto main

        git rebase --continue  # continue after resolving conflict

        git rebase --abort  # cancel rebase


## Stash

        git stash  # save uncommitted changes

        git stash pop  # apply and remove stash

        git stash apply  # apply without removing

        git stash list  # list all stashes


## Cherry-pick

        git cherry-pick <commit-id>  # apply specific commit


## Logs with graph (very important)

        git log --oneline --graph --all  # visualize branch history


## Squash merge

        git merge --squash feature-branch  # combines all commits into one before merge

        git commit -m "feature added"  # required after squash

## Authenticate GitHub CLI with your account (required before using gh)

    gh auth login

## Create a new GitHub repository from terminal

    gh repo create

## List all your GitHub repositories

    gh repo list

## Create a new issue in a repository (for bugs, tasks, tracking)

    gh issue create

## Create a Pull Request from current branch to main (used for code review & merging)

    gh pr create

## Merge a Pull Request directly from terminal (no browser needed)

    gh pr merge

## List GitHub Actions workflow runs (used to check CI/CD status)

    gh run list

