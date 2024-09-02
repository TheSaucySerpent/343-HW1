Commonly Used Commands Provided By git (used notes from Programming & Utilities):

Basic Local Operations:

git init - initializes a new git repository
git status - displays the state of the working directory and staging area
git add [filename] - add untracked file or stage changes to specified file
git rm [filename] - remove specified file from git repository
git mv [filename] - move or rename file within the git repository
git commit - commit staged changes to the git repository
git log - shows a detailed log of previous commits, allowing you to view the commit history
git diff - shows changes between two inputs (by default the changes between your current working directory and your staging area)
git show [object] - used to view details on blobs, trees, tags, and commits 

Restoring Files:

git restore --staged [filename] - unstages changes but keeps changes in working directory
git restore [filename] - gets rid of changes made to file
git restore --staged --worktree - can use to go back to previous commit (can also use git reset)

Branching:

git branch -a - lists branches
git branch [branchname] - create a new branch
git switch/checkout [branchname] - switch to an existing branch
git switch -c [branchname] - create and go to a new branch
git branch -d [branchname] - delete a branch
git merge [branchname] - merges changes from other branch into current branch

Remotes:

git clone [ssh link] - clones a remote repository
git push - pushes changes to remote repository (may need to use -set-upstream origin or git remote add origin)
git fetch - copies changes from remote repository into your local repository
git merge - copies changes from git fetch into working directory
git pull - equivalent to doing both git fetch + git merge

Merge Conflicts:

git restore --ours [filename] - keep file of current branch (merging into) intact
git restore --theirs [filename] - keep the file being merged in intact
git merge --abort - aborts the merge process

Stashing Changes:

git stash - saves changes to files for later, removing these changes from the working directory (can use -u to stash untracked files instead of only staged/tracked files)
git stash pop - gets the previously stashed changes back

Reverting Commits:

git revert <commit> - does not rewrite history, makes a new "revert" commit
