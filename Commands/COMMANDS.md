GIT COMMANDS - :keyboard:
==========================


### HELP - :question:

> Commands that will bring information about other commands and the git itself


| Command | Description |
| ------- | ----------- |
| `$ git --version` | Shows the git version |
| `$ git help <command name>` | Shows the details about a specific command |
| `$ git <command name> -h` | Shows the concise details 

---

### SETUP - :hammer_and_wrench:

> Commands that will help to configure the user information used across all the local repositories

| Command | Description |
| ------- | ----------- |
| `$ git config [--local | --global | --system] <key> [<value>]` | The configuration can be done locally, globally or for the system |
| `$ git config --global user.name "Yuri Serrano"` | Configure the name of the Git user |
| `$ git config --global user.email "yurijserrano@gmail.com"` | Configure the e-mail of the Git user |
| `$ git config <key>` | Returns a predefined value of the configuration  |
| `$ git config user.name` | Returns the Git user name |
| `$ git config user.email` | Returns the Git user e-mail|
| `$ git config --global core.editor "code --wait"` | Define visual studio code as the default text editor|
| `$ git config --global core.editor "atom --wait"` | Define atom as the default text editor|
| `$ git config --global core.editor "subl -n -w"`  | Define sublime as the default text editor|
| `$ git config --global color.ui auto"`  | Set automatic command line coloring for Git for easy reviewing|

---

### INIT - :file_folder:

> Commands that will help initializing and cloning repositories

| Command | Description |
| ------- | ----------- |
| `$ git init` | Initialize (create) a repository |
| `$ git clone <URL> [local project name]` | Create a local copy of the remote repository specified [I] |
| `$ git $ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY` | Create a local copy of the remote repository specified [II] |
| `$ git clone $ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY <project_name>` | Create a local copy of the remote repository specified [III] |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of the remote repository specified [IV] |
| `git clone ssh://git@github.com/[username]/[repository-name].git [Local-Project-Name]` | Create a local copy of the remote repository specified [V]|

---

### STAGE & SNAPSHOT - :camera:

> Commands that will help to create snapshots and handle with the working directory and staging area

| Command | Description |
| ------- | ----------- |
about a specific command|
| `$ git status` | Shows the status of the files in the working tree and staging area (Show which unstaged files have changed)|
| `$ git status --short` | Shows the status of the local repository (just critical changes) |
| `$ git status -s (-s means short status)` | Shows the status of the files in the working tree and staging area |
| `$ git add <filename|folder>` | Add a file or folder to the staging area [I] |
| `$ git add filename.txt` | Add a file to the staging area [II] |
| `$ git add filename/` | Add a folder to the staging area [III] |
| `$ git add -A` | Add all files |
| `$ git add .` | Add all untracked or modified files |
| `$ git add -u` | Add all modified or delete files |
| `$ git restore <filename>` | Unstage changes/Restore files that  were staged but they have not been committed yet. |
| `$ git restore <filename>` | Unstage changes/Restore file that was staged but it has not been committed yet. |
| `$ git restore .` | Unstage changes/Restore files that were staged but they have not been committed yet. |
| `$ git commit -m <commit message>` | Create a commit passing a short message to describe it (create a snapshot of the current project) [I] |
| `$ git commit -m "Add filename.txt"` | Create a commit passing a short message to describe it (create a snapshot of the current project) [II] |
| `$ git commit -am "message"` | Add/commit all changes from all tracked files (no untracked files) in one go |
| `$ git commit -a -m "message"` | Add/commit all changes from all tracked files (no untracked files) in one go |
| `$ git commit --amend -m <message>` | Amend a previous commit [I] |
| `$ git commit --amend -m "add fileC.txt"` | Amend a previous commit [II] |
| `$ git commit --amend --no-edit` | Amends a commit without changing its commit message. |
| `$ git rm -r <file|folder>` | Remove a file or folder |
| `$ git cherry-pick <commit_id>` | Copy the commit of another branch to the current branch |


---

### BRANCH & MERGE - :deciduous_tree:

> Commands that will help to isolate the work in branches,  changing context, and integrating changes

| Command | Description |
| ------- | ----------- |
| `$ git branch` | See a list of branches (the asterisk denotes the current branch) |
| `$ git branch -l` | View current branch you are on |
| `$ git branch -a` | See local and remote branches |
| `$ git branch -r` | See remote branches |
| `$ git branch --all` | Display local and tracking branch names |
| `$ git branch <name>` | Create a branch |
| `$ git switch -c <branch_name>` | Create a branch with a specific name |
| `$ git switch <branch_name>` | Switch for a specific branch |
| `$ git switch @{-1}` | Switch for the previous branch |
| `$ git checkout <branch|commit>` | Checkout a branch or commit |
| `$ git checkout -` | Switch to the branch last checked out |
| `$ git checkout -- <filename>` | Discard changes to a file [I] |
| `$ git checkout -- filename.txt` | Discard changes to a file [II] |
| `$ git checkout -- .` | Discard changes to all files |
| `$ git checkout <commit_id> -- <filename>` | Restore file from a custom commit (in current branch) [I]|
| `$ git checkout 6eb715d -- index.html` | Restore file from a custom commit (in current branch) [II]|
| `$ git checkout -b <branch_name>` | Create and checkout a branch |
| `$ git checkout -b <branch name> origin/<branch name>` | Clone a remote branch and switch to it |
| `$ git branch -m <old branch name> <new branch name>` | Rename a local branch |
| `$ git branch -d <branch_name>` | Delete a local branch |
| `$ git branch -D <branch_name>` | Delete a local branch even when it's not fully merged |
| `$ git merge <branch_name>` | Merge the specified branch’s history into the current one |
| `$ git merge <source_branch> <target_branch>` | Merge a branch into a target branch |
| `$ git merge --abort` | Cancel a merge process |
| `$ git merge --ff-only <branch_name>` | Merge the specified branch’s history into the current one (only if fast forward) |
| `$ git merge --no-ff <branch_name>` | Merge the specified branch’s history into the current one (force a new commit) |
| `$ git merge --squash <branch_name>` | Squash-merge a feature branch (as one commit) |

---

### INSPECT & COMPARE & CHANGES- :open_book:

> Commands that will help examining logs, diffs and object information


| Command | Description |
| ------- | ----------- |
| `$ git show <commit_id>` | Show a specific commit|
| `$ git show HEAD` | Show the current commit|
| `$ git log` | Show the commit history for the currently active branch|
| `$ git log --oneline` | Shows condensed version of the commits history|
| `$ git log --oneline -1` | Shows the last commit|
| `$ git log --oneline -2` | Shows the last two commits in a condensed form|
| `$ git log --oneline --graph` | Shows commit history as a graph|
| `$ git log --all --decorate --oneline --graph` | Shows commit history as a graph|
| `$ git log --all` | See a combined log of all local and tracking branches|
| `$ git log origin/master --oneline` | See the commits of the remote branch [I]|
| `$ git log origin --oneline` | See the commits of the remote branch [II]|
| `$ git log branchB..branchA` | Show the commits on branchA that are not on branchB|
| `$ git log --stat -M` | Show all commit logs with indication of any paths that moved TEMPORARY COMMITS |
| `$ git log --follow <file>` | Show the commits that changed file, even across renames |
| `$ git rm <filename>` | Delete the file from project and stage the removal for commit |
| `$ git mv <existing_path> <new_path>` | Change an existing file path and stage the move |
| `$ git diff` | Diff of what is changed but not staged (list unstaged changes to files)|
| `$ git diff --staged` | Diff of what is staged but not yet commited |
| `$ git diff <filename>` | Diff of what is changed but not staged [I]|
| `$ git diff filename.txt` | Diff of what is changed but not staged [II] |
| `$ git diff --cached <filename>` | Diff of what is staged but not yet commited [I]|
| `$ git diff --cached filename.txt` | Diff of what is staged but not yet commited [II]|
| `$ git diff branchB...branchA` | Show the diff of what is in branchA that is not in branchB|

---

### SHARE & UPDATE - :satellite:

> Commands that will help retrieving updates from another repository and updating local repos

| Command | Description |
| ------- | ----------- |
| `$ git push --set-upstream origin <branch>` | Push a local branch for the first time (Also create the remote branch)|
| `$ git push -u origin <branch>` | Push a local branch for the first time (Also create the remote branch) |
| `$ git push origin branchB:branchB` | Push a local branch to the remote branch of same name |
| `$ git push origin :<remote_branch>` | Push a local branch to the remote branch of same name |
| `$ git push -d origin <branch_name>` | Delete a remote branch on origin |
| `$ git push --delete origin <branch_name>` | Delete a remote branch on origin |
| `$ git push origin <local_branch>:<remote_branch>` | Delete a remote branch on origin |
| `$ git reset --hard HEAD~1 && git push -f origin master` | Undo last push |
| `$ git pull` | Fetch and merge any commits from the tracking remote branch |
| `$ git pull --rebase` | Fetch the changes made on remote branch  and avoid merging them, by rebasing your commits on top of the them|
| `$ git tag -a <tag_name> <commit_hash> -m <message>` | Create a tag [I] |
| `$ git tag -a v1.0.0 9fceb02 -m "Initial release"` | Create a tag [II] |
| `$ git tag -d v1.0.0` | Delete a tag locally |
| `$ git tag --delete v1.0.0` | Delete a tag locally |
| `$ git tag --delete v1.0.0` | Delete a tag locally |
| `$ git push  <REMOTE_NAME> <TAG_NAME> ` | Push a single tag remotely [I]|
| `$ git push origin YuriTag ` | Push a single tag remotely [II]|
| `$ git push origin YuriTag ` | Push a single tag remotely [II]|
| `$ git push origin refs/tags/YuriTag ` | Push a single tag remotely [III] (Avoid branch name and tag name collision)|
| `$ git push --tags` | Send all the tags for the remote repository |
| `$ git push origin :refs/tags/<tagname>` | Delete a tag remotely |
| `$ git push origin :refs/tags/v1.0.0` | Delete a tag remotely |
| `$ git tag` | List the tags of the repository |
| `$ git tag -n` | List the tags of the repository with an extensive description of each one of them |
| `$ git tag -l <pattern>` | List the tags that match a certain pattern [I] |
| `$ git tag -l v1*` | List the tags that match a certain pattern [II] |
| `$ git tag --sort=committerdate` | List and sort the tags by their latest Git activity |
| `$ git tag --sort=committerdate -l <pattern>` | List and sort the tags by their latest Git activity using a pattern |
| `$ git tag --sort=committerdate -l v1*` | List and sort the tags by their latest Git activity using a pattern |
| `$ git ls-remote --tags <remote>` | List remote tags [I]|
| `$ git ls-remote --tags origin` | List remote tags [II]|
| `$ git fetch --tags` | Fetch tags from your remote repository |
| `$ git fetch --all --tags` | Fetch all tags from your remote repository |
| `$ git ls-remote` | List references in a remote repository |
| `$ git remote prune origin` | Clean up deleted remote branches |
| `$ git remote add <name> <url>` | Add a remote repository to a local git repository [I] |
| `$ git remote add origin https://github.com/user/repo.git` | Add a remote repository to a local git repository [II] |
| `$ git remote add origin ssh://github.com/user/repo.git` | Add a remote repository to a local git repository [III] |
| `$ git remote set-url origin https://github.com/USERNAME/REPOSITORY.git` | Change a remote's URL|
| `$ git remote rename origin destination` | Change remote name from 'origin' to 'destination'|
| `$ git remote rm <name>` | Remove a remote URL from your repository. [I]|
| `$ git remote rm destination` | Remove a remote URL from your repository. [II]|
| `$ git remote --verbose` | Shows the information about remote repositories associated with the local repository [I]|
| `$ git remote -v` | Shows the information about remote repositories associated with the local repository [II]|
| `$ git remote set-head <remote> <branch>` | Change the default remote tracking branch |


---

### REWRITE HISTORY - :hourglass_flowing_sand:	

> Commands that will help rewriting branches, updating commits and clearing history

| Command | Description |
| ------- | ----------- |
| `$ git rebase <branch_name>` | Apply any commits of current branch ahead of specified one |
| `$ git rebase -i HEAD~N` | Squash commits for a specific number|
| `$ git rebase --abort` | Cancel Rebase|
| `$ git rebase --continue` | Continue Rebase|
| `$ git reset --soft HEAD~1` | Undo your most recent commit and put those changes back into staging, so you don't lose any work |
| `$ git reset --soft HEAD^` | Undo previous commit, put changes in staging |
| `$ git reset --hard HEAD~1` | Will completely delete the commit and throw away any changes |
| `$ git reset --hard HEAD^` | Undo last commit and all changes |
| `$ git reset --hard HEAD^^` | Undo two (^^) last commits and all changes |
| `$ git reset --hard <commit_id>` | Clear staging area, rewrite working tree from specified commit |
| `$ git reset <filename>` | Unstage file |
| `$ git reset HEAD <filename>` | Unstage file |
| `$ git reset HEAD~` | Undo commit |
| `$ git reset --soft HEAD~3 && git commit -m "write a new commit message from scratch for all the commits you just squashed"` | Squash last 3 commits |
| `$ git merge-base my-branch master` | Return the hash of the commit that is a common ancestor between the two branches |
| `$ git rebase --interactive ${HASH}` | Squash the commits using the hash id of the commit provided by the command merge-base |
| `$ git revert <commit_id>` | Go back to a specific commit [I]|
| `$ git revert 073791e` | Go back to a specific commit [II]|
| `$ git reset --soft <commit_id>` | Soft reset (move HEAD only; neither staging nor working dir is changed) [I]|
| `$ git reset --soft 073791e` | Soft reset (move HEAD only; neither staging nor working dir is changed) [II]|
| `$ git reset --mixed <commit_id>` | Mixed reset (move HEAD and change staging to match repo; does not affect working dir) [I]|
| `$ git reset --mixed 073791e` | Mixed reset (move HEAD and change staging to match repo; does not affect working dir) [II]|
| `$ git reset --hard <commit_id>` | Hard reset (move HEAD and change staging dir and working dir to match repo) [I]|
| `$ git reset --hard 073791e` | Hard reset (move HEAD and change staging dir and working dir to match repo) [II]|
| `$ git reset` | Unstage all files|
| `$ git reset -- <filename>` | Unstage the file [I]|
| `$ git reset -- README` | Unstage the file [II]|
| `$ git reflog` |  Record of all commits that are or were referenced in the repository at any time (pruned after 90 days)|
| `$ git reflog delete master@{2}` | Delete a specific entry of the reflog|


---

### TEMPORARY COMMITS - :stopwatch:

> Commands that will help temporarily store modified, tracked files in order to change branches

| Command | Description |
| ------- | ----------- |
| `$ git stash` | Save modified and staged changes |
| `$ git stash pop` | Unstash changes and bring them back into your working directory from the top of stash stack  |
| `$ git stash pop stash@{0}` | Unstash changes of a specific stash and bring them back into your working directory from the top of stash stack  |
| `$ git stash apply` | Unstash changes without popping them off the stack from the top of stack (Apply these stashed changes multiple times) |
| `$ git stash list` | List stack-order of stashed file changes |
| `$ git stash apply stash@{3}` | Apply a specific stash from the list of stashes |
| `$ git stash drop` | Discard the changes from top of stash stack |
| `$ git stash list -p` | See all edits done on previous stashes points |
| `$ git stash show` | To show files changed in the last stash |
| `$ git stash show -p` | To view the content of the most recent stash |
| `$ git stash show stash@{0}` | Show stash stats |
| `$ git stash show -p stash@{1}` | Show stash changes |
| `$ git stash save "message"` | Add a message with the stash |
| `$ git stash clear` | To clear all of stashes at once |
| `$ git stash branch <new_branch>` | Create branch from stash|
| `$ git stash drop stash@{0}` | Delete custom stash item|
| `$ git stash save "Message"` | Include in the stash|