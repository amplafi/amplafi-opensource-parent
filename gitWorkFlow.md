## Working from forked repo##
* Create a fork and working copy on local machine.
   * Clone the fork  
   <div> git clone [ssh address to repo] </div>
   * Move into the git directory  
   <div> cd [git project directory] </div>
   * Add the upstream link  
   <div> git remote add upstream [the read-only git address to repo that was forked from] </div>

## Work-flow (process to use when making changes)##
* Update your master branch fork with upstream changes.  
   <div> git pull  
   git pull origin master  
   git push
   </div>
* Create a branch to work on and switch to that branch  
   <div> git checkout -b [branch name] </div>
* Make changes to files and commit to this branch.
* To check for conflicts
   * First bring your master branch up to date with these commands.  
      <div> git checkout master  
      git pull  
      git pull upstream master  
      git push
      </div>
   * Then merge the changes.  
      <div> git checkout [branch name]  
      merge master
      </div>

###When your changes are ready###
* Update your master branch, and rebase your topic branch.  
   <div> git checkout [branch name]  
   git pull upstream master  
   git -i rebase master </div>
   * At this point you can clean up your commits by squashing, editing or deleting them.
   * One reason you might want to squash commits is if there were many small commits that accomplish one task
   this way the history is easier to read for the person who is to review your code.
* If there are conflicts, fix the conflicts and git add them before --continue.  
   <div> First resolve conflicts  
   git add [fileName with conflicts]  
   git rebase --continue </div>
* When changes are complete then merge to master and push.  
   <div> git checkout master  
   git merge [branch name] </div>
* Finally delete your working branch  
   <div> git branch -d [branch name] </div>

### Notes###

* Some people like to work from branches that are public. If you work from public 
branches then rebasing is not advised (since your history is public rebasing can 
break someone else's project). Instead of rebasing just preform the merge into your master branch.
* Working with remote branches.
   * To make a remote branch  
   <div> git checkout -b dev_event_cbs master  
   git push origin -u dev_event_cbs </div>
   * Then to delete the remote branch (after merging, or after the pull request has been accepted)  
   <div>git checkout master  
   git pull upstream master  
   git push  
   git branch -D dev_event_cbs  
   git push origin --delete dev_event_cbs </div>

### Further Reading###
[Git reference](http://gitref.org/)  
[Pro git book - Professional Version Control](http://progit.org/)

### References###
[Avoiding Git Disasters: A Gory Story](http://www.randyfay.com/node/89)  
[A Rebase Workflow for Git](http://www.randyfay.com/node/91)  
[A Git Workflow for Agile Teams](http://reinh.com/blog/2009/03/02/a-git-workflow-for-agile-teams.html)  
[A rant from Linus](http://www.mail-archive.com/dri-devel@lists.sourceforge.net/msg39091.html)
