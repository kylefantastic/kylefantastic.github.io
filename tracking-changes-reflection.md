#1.5 Tracking Changes

How does tracking and adding changes make developers' lives easier?

When developers are working on a project, there could be hundreds of different changes that occur.  Some may be huge, but others may just be working out a bug, or altering a minor element of the code.  Without a manageable method of keeping track of these changes, going back to check what happened and when, would be an insurmountable task (someone would need to write some software to make it easier).  That's what makes the git version control software so useful.

What is a commit?

This makes developers' lives easier by automatically tracking those changes and allowing them to collect them all in one grouping called a commit.  A commit takes the total of all recent changes that a developer wants to lump together as a larger sum(adding, deleting, debugging, renaming, et cetera), for the developer to submit to a repository like GitHub.

What are the best practices for commit messages?

When a sufficient amount of changes have been made to constitute a commit, the developer would do so by using the git add command.  Add is the first stage in committing because it takes the "snapshot" of changes that you will commit and the command, git commit will actually record/commit those changes to the repo.  If you simply use git add it will prompt you to fill out a commit message which will include a brief message and summary of changes to commit.  Tim Pope has a great guide for commit messages that embody the industry standard.  First of all it should start with a brief (50 characters or less) description on changes, then a summary that could be a paragraph or two that goes into more detail.  When describing the changes that are going to be committed, it is good practice to use the imperative to decribe what the change does-i.e. "Update transfer protocol" as opposed to "Updates (or updated) transfer protocol"  There a few reasons for this seemingly unnatural choice of tense in commits, but the best explanation I could find was that you want to think of the change as an action.  In other words, think of it completing the phrase "This change will________."

What does the HEAD^ argument mean?

The HEAD^ argument is the last commit.  HEAD is the commit you are currently on and HEAD followed by a number represents how many commits you go back to.  HEAD-3 is the third commit back from the present.

What are the 3 stages of a git change and how do you move a file from one stage to the other?

Before a file is changed it will show a clean git status.  That is the first stage of a git change, the blank stage if you like.  If you type git status it should read "nothing to commit, working directory clean".  The next stage will be when a change has been made, the current git status would then read "untracked files" with a summary of changes and a summary, but nothing added to commit.  Then when the files are added we find ourselves at tht third and final stage of a change.  When the changes are committed, it returns to the clean working directory.

Write a handy cheatsheet of the commands you need to commit your changes?

-make changes
-git add to add the changes
-git commit to commit the changes

What is a pull request and how do you create and merge one?

When the changes are committed, it is time for a pull request, wherein the developer submits the changes to the repository.  Firstly you need to be working on a branch separate from the master.  To do this you can enter git checkout - b followed by the new branch name.  This will ensure you are working on a branch separate from the master branch.  After making changes and committing the mas described above, you will then need to enter git push origin followed by the branch name and this will automatically update the GitHub profile to make the pull request.  Just click the button on your page and it will initiate.  One thing you may need to do at this point is search for your fork by name.  If there are too many forks, then you will have to change the url directly to access your pull request by typing your profile in the address instead of the base fork.  Once you have done this you simply merge the branch into the master and it will be incorporated.  Once it is merged it is good practice to delete the old branch since it is now a part of the master.  The point of all this is that the pull requests, let the developers review the changes before merging.  Without this process there could be too many things changing without proper oversight which could lead to bugs in your master branch, which is a bad thing.

Why are pull requests preferred when working with teams?

When you are working with a team of programmers, this oversight becomes invaluable.  If a developer introduces changes that complicate the project, or don't work with the code that another developer has changed, the pull request is like insurance to be sure there are no prblems with the changes.  Without the pull requests, changes could be flying in from all over the place without a way of knowing what changes were being applied at what stage.