# Hello!

This is the workshop repository for the Git Gud Quick workshop for Opswerks
Converge 2018.

[Click me](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

# Outline

* Git Gud Quick
	* An interactive quickstart guide to `git`
* Introduction
	* Bad joke time
	* Hi, I'm new here
* Workshop goals
	* From zero to git working
	* Learn how to fork, commit, branch, push, PR, pull
* Expectations and assumptions
	* Comfortable working with a shell
	* A public GitHub account
	* SSH key associated with your GitHub account
	* Not going to talk about other DVCS like Mercurial
* Introduction to Git
	* Written by Linus Torvalds
	* Project first started in 2005
	* Made to replace BitKeeper after relations went bad
	* "I'm an egotistical bastard, so I name all my projects after myself.
	  First Linux, now git."
	  (https://www.pcworld.idg.com.au/article/129776/after_controversy_torvalds_begins_work_git_/)
* Workshop proper
	* Fork me!
		* Log in to GitHub
		* Go to <https://github.com/tsdmgz/git-gud.git>
		* Press fork
		* Explain what happens
	* Let's get started
		* `git clone git@github.com:<username>/git-gud.git`
	* Fork and pull workflow
		* You copy the repository to your account
		* Work on your copy
		* Commit and push to yours
		* File a pull request for integration
	* First commits
		* Create a file with some content something unique like last thing you
		  searched for, or your password
		* `git add <file>`
		* `git commit` and write a commit message
	* Check out this branch
		* `git branch devel`
		* `git branch`
		* `git checkout devel`
		* Make a new file, delete previous, and commit again
		* `git checkout master`
		* Shortcut: `git checkout -b devel`
	* Branches
        * Other states of code, internal fork of your repository
		* Common use cases: master/devel, experimental edits
	* Push!
		* `git checkout devel` && `git push`
		* It failed?
		* `git push --set-upstream origin devel`
	* Creating new branches at remote
		* `--set-upstream` tells git to push and pull local `devel` branch to
		  remote `devel` branch, and create one if necessary
		* Future pushes at this branch do not need `--set-upstream`
		* This push goes to *your* repo
	* Pull requests
		* Go to your fork of `git-gud.git`
		* Base fork: `tsdmgz/git-gud` base: `master` <- head fork:
		  `<username>/git-gud` compare: `devel`
		* > Create pull request
		* Write a title about your pull request
		* Explain why you want this PR merged
	* Social interactions
		* Pull requests is more of a social thing
		* GitHub provides a template on asking someone to include your changes
		  and an easy way of integrating those changes
		* Possible to do outside of GitHub simply by asking someone to pull your
		  changes and integrate it
		* Canonical repositories are "socially accepted" or simply because we
		  say so and we accept it as is, or as business requirements dictate. Or
		  because you're the maintaner of that project (nothing's stopping you
		  from forking and making a new project out of it)
* About commit messages
	* Commit messages
		* 50char or less summary of changes
		* Body for explaining what and why do the change, wrap to 72char
		* How is answered by `git diff`
		* <https://chris.beams.io/posts/git-commit/>
		* Why 50char subject? Mostly because GitHub
		* Vim tip: `:set textwidth=72|set colorcolumn=+1`
		* Emacs/Nano: ¯\_(ツ)_/¯
	* Giving someone direct commit access to a repo
	* `git branch -r`
* Scenarios
    * `git commit --amend`
	* Looking at previous commits
		* `git log`
	* What changed between commits
		* `git diff commitA commitB`
		* Can be tag, branch, even something from reflog
		* If it has a commit ID, it can be diffed
	* Syncing your fork with upstream
		* `git remote add upstream <repo-url>`
		* `git pull upstream devel`
		* `git push origin devel`
	* Partially staging files for commit
		* `git add --patch`
		* `git add --interactive`
	* Reverting a buggy commit
		* `git revert`
		* vs `git reset --hard`
	* Accidentally lost a commit
		* `git reflog`
		* `git checkout <commitHash>`
		* Garbage collection and unreachable commits
* References
	* Writing commit messages: https://chris.beams.io/posts/git-commit/
	* Pro Git: https://git-scm.com/book
    * Linus quote: <https://www.pcworld.idg.com.au/article/129776/after_controversy_torvalds_begins_work_git_/>
    * Spectre logo: 2018, Natascha Eibl, CC0, <https://vividfox.me>
