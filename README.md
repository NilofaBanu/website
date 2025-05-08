1.Cloning a Repository
PS C:\Users\dx\Desktop\Task GIT> git clone
fatal: You must specify a repository to clone.

usage: git clone [<options>] [--] <repo> [<dir>]  

PS C:\Users\dx\Desktop\Task GIT> git clone https://github.com/NilofaBanu/website.git
Cloning into 'website'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)

What it does: Downloads the remote GitHub repository to your local machine.

Outcome: Creates a folder named website with all files and history from the remote repo.

2.Checking File Status

PS C:\Users\dx\Desktop\Task GIT\website> git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html
nothing added to commit but untracked files present (use "git add" to track)  

What it does: Shows the current working state of the repo, including:
Untracked files
Staged changes
Clean working tree (if nothing changed)

3. Adding Files to Stage

PS C:\Users\dx\Desktop\Task GIT\website> git add index.html

What it does: Tells Git to include index.html in the next commit.


PS C:\Users\dx\Desktop\Task GIT\website> git add .
What it does: Stages all changed or untracked files in the current directory.


4.Committing Changes

PS C:\Users\dx\Desktop\Task GIT\website> git commit -m "Created new file in branch3"
[gitbranch3 74dd9a1] Created new file in branch3
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 gitbr.txt

 What it does: Commits the staged file(s) with a message explaining the change.

 5.Pushing Changes to Remote

 PS C:\Users\dx\Desktop\Task GIT\website> git push origin main
Enumerating objects: 5, done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1015 bytes | 24.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/NilofaBanu/website.git
   368f497..75032e9  main -> main

   What it does: Pushes your local commits on the main branch to GitHub.

   6. Checking Available Branches

   PS C:\Users\dx\Desktop\Task GIT\website> git branch -a
  remotes/origin/HEAD -> origin/main
  remotes/origin/main
PS C:\Users\dx\Desktop\Task GIT\website> git branch -a
* main
From https://github.com/NilofaBanu/website
 * [new branch]      gitbranch1 -> origin/gitbranch1
PS C:\Users\dx\Desktop\Task GIT\website> git branch -a
* main
  remotes/origin/gitbranch1
  remotes/origin/main

  What it does: Lists all local and remote branches.
 indicates your current branch.
remotes/origin/... are remote tracking branches.

7. Switching Branches

PS C:\Users\dx\Desktop\Task GIT\website> git checkout gitbranch1
Switched to a new branch 'gitbranch1'

What it does: Switches to the branch named gitbranch1.
If the branch doesn't exist locally, it will create and track it from origin/gitbranch1.

8.Creating Commits in a Branch

PS C:\Users\dx\Desktop\Task GIT\website> git add .

PS C:\Users\dx\Desktop\Task GIT\website> git commit -m "Created newfile in gitbranch1"
[gitbranch1 5175a84] Created newfile in gitbranch1
 create mode 100644 new.txt
PS C:\Users\dx\Desktop\Task GIT\website> git push origin gitbranch1
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Writing objects: 100% (3/3), 355 bytes | 71.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/NilofaBanu/website.git
   00a85e6..5175a84  gitbranch1 -> gitbranch1
PS C:\Users\dx\Desktop\Task GIT\website> git checkout main
Your branch is up to date with 'origin/main'.
PS C:\Users\dx\Desktop\Task GIT\website> git checkout gitbranch1
Your branch is up to date with 'origin/gitbranch1'.

What it does:
Stages add .
Commits the file with a message.
Pushes the commit to the remote gitbranch1.

9.Fetching Remote Branches

PS C:\Users\dx\Desktop\Task GIT\website> git fetch origin
From https://github.com/NilofaBanu/website

What it does: Updates your local view of remote branches (without merging anything).

10.Checking Out a New Remote Branch

PS C:\Users\dx\Desktop\Task GIT\website> git checkout gitbranch3
branch 'gitbranch3' set up to track 'origin/gitbranch3'.
  gitbranch1
  gitbranch2
* gitbranch3
  main
  remotes/origin/gitbranch1
  remotes/origin/gitbranch2
  remotes/origin/gitbranch3
  remotes/origin/main

  What it does: Switches to a remote branch (origin/gitbranch2), creates a local branch, and sets it to track the remote.

