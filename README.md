
Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ touch my-file.txt

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git add my-file.txt

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git commit -a -a "keep my save file"                                                                                                    
fatal: paths 'keep my save file ...' with -a does not make sense

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git commit -a -m "keep my save file"
[main 04d674f] keep my save file
 2 files changed, 3 deletions(-)
 delete mode 100644 app.html    
 create mode 100644 my-file.txt

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git push -u origin --force
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git push -u origin --force main
Enumerating objects: 21, done.
Counting objects: 100% (21/21), done.
Delta compression using up to 2 threads
Compressing objects: 100% (18/18), done.
Writing objects: 100% (21/21), 1.93 KiB | 132.00 KiB/s, done.
Total 21 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), done.
To https://github.com/jeremiech/the-gym-repos-dedicated.git
 + 9180637...04d674f main -> main (forced update)
branch 'main' set up to track 'origin/main'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git branch dev

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git branch test

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git switch dev
Switched to branch 'dev'

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git swicth dev
git: 'swicth' is not a git command. See 'git --help'.

The most similar command is
        switch

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git swicth test
git: 'swicth' is not a git command. See 'git --help'.

The most similar command is
        switch

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git branch -d test
Deleted branch test (was 04d674f).

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git mv my-file.txt index.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ touch home.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git status 
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    my-file.txt -> index.html


Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git add home.html
The following paths are ignored by one of your .gitignore files:
home.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    my-file.txt -> index.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html


Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git add home.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git stash push home.html
Saved working directory and index state WIP on dev: 04d674f keep my save file

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ touch about.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git add about.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git stash push about.html
Saved working directory and index state WIP on dev: 04d674f keep my save file

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git stash status
fatal: unknown subcommand: status

usage: git stash list [<options>]
   or: git stash show [<options>] [<stash>]
   or: git stash drop [-q|--quiet] [<stash>]
   or: git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
   or: git stash branch <branchname> [<stash>]
   or: git stash clear
   or: git stash [push [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [-m|--message <message>]
                 [--pathspec-from-file=<file> [--pathspec-file-nul]]
                 [--] [<pathspec>...]]
   or: git stash save [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [<message>]


Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git stash list
stash@{0}: WIP on dev: 04d674f keep my save file
stash@{1}: WIP on dev: 04d674f keep my save file

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git stash pop stash@\{1\}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html
        renamed:    my-file.txt -> index.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Dropped stash@{1} (eae52837a2607deff810160e482dce3feec0d92c)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git stash pop stash@\{0\}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    my-file.txt -> about.html
        new file:   home.html
        new file:   index.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Dropped stash@{0} (f5f01cd130e8da8e9d23c0e9be75d56fb78fe4f2)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ touch team.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    my-file.txt -> about.html
        new file:   home.html
        new file:   index.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html


Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git add team.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git stash list

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git stash push team.html
Saved working directory and index state WIP on dev: 04d674f keep my save file

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git stash list
stash@{0}: WIP on dev: 04d674f keep my save file

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    my-file.txt -> about.html
        new file:   home.html
        new file:   index.html
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore

Dropped stash@{0} (2c76b62b5f419df50430a0a313971012af8ed104)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    my-file.txt -> about.html
        new file:   home.html
        new file:   index.html
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore


Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git log --oneline
04d674f (HEAD -> dev, origin/main, main) keep my save file
81773a7 add merged change
9d973bb update app.html file
9a2fba1 update app.html file
07d2699 this app has ammend
2b08e46 add app modified file
599575b save the changed file for index

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    my-file.txt -> about.html
        new file:   home.html
        new file:   index.html
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore


Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    my-file.txt -> about.html
        new file:   home.html
        new file:   index.html
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore
        modified:   team.html


Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ gti add team.html
bash: gti: command not found

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git add team.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        renamed:    my-file.txt -> about.html
        new file:   home.html
        new file:   index.html
        new file:   team.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   .gitignore


Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git commit -a -m "save the created team file"
[dev 51b0a52] save the created team file
 5 files changed, 3 insertions(+), 1 deletion(-)
 rename my-file.txt => about.html (100%)
 create mode 100644 home.html
 create mode 100644 index.html
 create mode 100644 team.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git log --oneline
51b0a52 (HEAD -> dev) save the created team file
04d674f (origin/main, main) keep my save file
81773a7 add merged change
9d973bb update app.html file
9a2fba1 update app.html file
07d2699 this app has ammend
2b08e46 add app modified file
599575b save the changed file for index

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git reset 04d674f
Unstaged changes after reset:
M       .gitignore
D       my-file.txt

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git log --oneline
04d674f (HEAD -> dev, origin/main, main) keep my save file
81773a7 add merged change
9d973bb update app.html file
9a2fba1 update app.html file
07d2699 this app has ammend
2b08e46 add app modified file
599575b save the changed file for index

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git branch ft/bundle-2

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ touch services.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git add services.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git pull origin main
From https://github.com/jeremiech/the-gym-repos-dedicated
 * branch            main       -> FETCH_HEAD
Already up to date.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git merge main
Already up to date.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git branch ft/service-redesign

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git add services.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git commit -a -m "modify the service file" --amend
[dev ba79d31] modify the service file
 Date: Thu May 18 17:44:14 2023 +0200
 3 files changed, 3 insertions(+), 4 deletions(-)
 delete mode 100644 app.html
 create mode 100644 services.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git push origin -u ft/service-redesign
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/jeremiech/the-gym-repos-dedicated/pull/new/ft/service-redesign
remote:
To https://github.com/jeremiech/the-gym-repos-dedicated.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git branch 
* dev
  ft/bundle-2
  ft/service-redesign
  main

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (dev)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git diff main ft/service-redesign

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git diff --staged

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git diff

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git merge main
Already up to date.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git stash pop
No stash entries found.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git log --oneline
04d674f (HEAD -> main, origin/main, origin/ft/service-redesign, ft/service-redesign, ft/bundle-2) keep my save file
81773a7 add merged change
9d973bb update app.html file
9a2fba1 update app.html file
07d2699 this app has ammend
2b08e46 add app modified file
599575b save the changed file for index

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git status 
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        index.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git switch ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git branch 
  dev
  ft/bundle-2
* ft/service-redesign
  main

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git switch ft/bundle-2
Switched to branch 'ft/bundle-2'

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/bundle-2)
$ git log --oneline
04d674f (HEAD -> ft/bundle-2, origin/main, origin/ft/service-redesign, main, ft/service-redesign) keep my save file
81773a7 add merged change
9d973bb update app.html file
9a2fba1 update app.html file
07d2699 this app has ammend
2b08e46 add app modified file
599575b save the changed file for index

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/bundle-2)
$ git diff 04d674f

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/bundle-2)
$ git branch 
  dev
* ft/bundle-2
  ft/service-redesign
  main

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/bundle-2)
$ git switch ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git add index.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git commit -a -m "saved the index file" 
[main e862868] saved the index file
 1 file changed, 12 insertions(+)
 create mode 100644 index.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git switch ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git merge main
Updating 04d674f..e862868
Fast-forward
 index.html | 12 ++++++++++++
 1 file changed, 12 insertions(+)
 create mode 100644 index.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git status 
On branch ft/service-redesign
Your branch is ahead of 'origin/ft/service-redesign' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git commit "add my merged file "
error: pathspec 'add my merged file ' did not match any file(s) known to git

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git commit -m "add my merged file "
On branch ft/service-redesign
Your branch is ahead of 'origin/ft/service-redesign' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git commit -m "add my merged file"
On branch ft/service-redesign
Your branch is ahead of 'origin/ft/service-redesign' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git push origin -u ft/service-redesign
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 493 bytes | 82.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/jeremiech/the-gym-repos-dedicated.git
   04d674f..e862868  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git branch ft/team-page

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ touch team.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/service-redesign)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/team-page)
$ git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/team-page)
$ git add team.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/team-page)
$ git commit -a -m  "cached the team file"
[ft/team-page dbf76aa] cached the team file
 1 file changed, 12 insertions(+)
 create mode 100644 team.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/team-page)
$ git push origin -u ft/team-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 259 bytes | 86.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/jeremiech/the-gym-repos-dedicated/pull/new/ft/team-page
remote:
To https://github.com/jeremiech/the-gym-repos-dedicated.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git branch ft/contact-page

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (main)
$ git switch ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/team-page)
$ git log --oneline
dbf76aa (HEAD -> ft/team-page, origin/ft/team-page) cached the team file
e862868 (origin/ft/service-redesign, main, ft/service-redesign, ft/contact-page) saved the index file
04d674f (origin/main, ft/bundle-2) keep my save file
81773a7 add merged change
9d973bb update app.html file
9a2fba1 update app.html file
07d2699 this app has ammend
2b08e46 add app modified file
599575b save the changed file for index

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ git cherry-pick 599575b
[ft/contact-page 6545068] save the changed file for index
 Date: Thu May 18 16:42:11 2023 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 app.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ git cherry-pick save the changed file for index
fatal: bad revision 'save'

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ git cherry-pick "save the changed file for index"
fatal: bad revision 'save the changed file for index'

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ touch contact-page.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ git add contact-page.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ git commit -m "cache this page"
[ft/contact-page 2361b3b] cache this page
 1 file changed, 1 insertion(+)
 create mode 100644 contact-page.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ giit push origin -u ft/contact-page
bash: giit: command not found

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ git push origin -u ft/contact-page
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 2 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 572 bytes | 114.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/jeremiech/the-gym-repos-dedicated/pull/new/ft/contact-page
remote:
To https://github.com/jeremiech/the-gym-repos-dedicated.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ git pull origin/ft/contact-page --rebase
fatal: 'origin/ft/contact-page' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ git pull origin ft/contact-page --rebase
From https://github.com/jeremiech/the-gym-repos-dedicated
 * branch            ft/contact-page -> FETCH_HEAD
Already up to date.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/faq-page)
$ touch faq.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/faq-page)
$ git status
On branch ft/faq-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        faq.html

nothing added to commit but untracked files present (use "git add" to track)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/faq-page)
$ git add faq.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/faq-page)
$ git status
On branch ft/faq-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   faq.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html


Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/faq-page)
$ git commit -m "save fac file"
[ft/faq-page 67f88a6] save fac file
 1 file changed, 1 insertion(+)
 create mode 100644 faq.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/faq-page)
$ git push origin -u ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 276 bytes | 55.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/jeremiech/the-gym-repos-dedicated/pull/new/ft/faq-page
remote:
To https://github.com/jeremiech/the-gym-repos-dedicated.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/faq-page)
$ git log --oneline
67f88a6 (HEAD -> ft/faq-page, origin/ft/faq-page) save fac file
2361b3b (origin/ft/contact-page, ft/contact-page) cache this page
6545068 save the changed file for index
e862868 (origin/ft/service-redesign, main, ft/service-redesign) saved the index file
04d674f (origin/main, ft/bundle-2) keep my save file
81773a7 add merged change
9d973bb update app.html file
9a2fba1 update app.html file
07d2699 this app has ammend
2b08e46 add app modified file
599575b save the changed file for index

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/my-private (ft/faq-page)
$
 
 
 ## this is the begging of the quastion four 
 Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git switch ft/team-page
Switched to a new branch 'ft/team-page'
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/team-page)
$ git branch
* ft/team-page
  main

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/team-page)
$ git switch ft/contact-page
Switched to a new branch 'ft/contact-page'
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/contact-page)
$ git switch ft/faq-page
Switched to a new branch 'ft/faq-page'
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/faq-page)
$ git switch ft/service-redesign
Switched to a new branch 'ft/service-redesign'
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/service-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git remote add git-copy https://github.com/jeremiech/the-gym-repos-dedicated.git

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git remote -v
git-copy        https://github.com/jeremiech/the-gym-repos-dedicated.git (fetch)
git-copy        https://github.com/jeremiech/the-gym-repos-dedicated.git (push)
origin  https://github.com/jeremiech/the-gym-repos-dedicated.git (fetch)
origin  https://github.com/jeremiech/the-gym-repos-dedicated.git (push)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git status -s
 M .gitignore
?? home.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git add home.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git status -s
 M .gitignore
A  home.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git commit -m "cache  this home file"
[main 25e5e1b] cache  this home file
 1 file changed, 1 insertion(+)
 create mode 100644 home.html

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git remote -v
git-copy        https://github.com/jeremiech/the-gym-repos-dedicated.git (fetch)
git-copy        https://github.com/jeremiech/the-gym-repos-dedicated.git (push)
origin  https://github.com/jeremiech/the-gym-repos-dedicated.git (fetch)
origin  https://github.com/jeremiech/the-gym-repos-dedicated.git (push)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git remote add both https://github.com/jeremiech/the-gym-repos-dedicated.git

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git remote set-url --add --push both https://github.com/jeremiech/the-gym-repos-dedicated.git

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git remote set-url --add --push both https://github.com/jeremiech/the-gym-repos-dedicated.git

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git push -u both main --force
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 301 bytes | 43.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/jeremiech/the-gym-repos-dedicated.git
   5492052..25e5e1b  main -> main
branch 'main' set up to track 'both/main'.
Everything up-to-date
branch 'main' set up to track 'both/main'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git branch ft/footer

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (main)
$ git checkout ft/footer
Switched to branch 'ft/footer'
M       .gitignore

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/footer)
$ git commit -am "modify home file"
[ft/footer 9bddb4b] modify home file
 2 files changed, 3 insertions(+), 2 deletions(-)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/footer)
$ git commit -am "make new change for home file"
[ft/footer 4e7eda0] make new change for home file
 1 file changed, 4 insertions(+), 1 deletion(-)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/footer)
$ git push origin -u ft/footer --force
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 2 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 638 bytes | 53.00 KiB/s, done.
Total 7 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/jeremiech/the-gym-repos-dedicated/pull/new/ft/footer
remote:
To https://github.com/jeremiech/the-gym-repos-dedicated.git
 * [new branch]      ft/footer -> ft/footer
branch 'ft/footer' set up to track 'origin/ft/footer'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/footer)
$ git branch ft/squashing

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/footer)
$ git switch ft/squashing
Switched to branch 'ft/squashing'

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/squashing)
$ git switch ft/footer
Switched to branch 'ft/footer'
Your branch is up to date with 'origin/ft/footer'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/footer)
$ git commit -am "modify the index file"
[ft/footer d4ea6c2] modify the index file
 1 file changed, 1 insertion(+), 12 deletions(-)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/footer)
$ git switch ft/squashing
Switched to branch 'ft/squashing'

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/squashing)
$ git switch ft/footer
Switched to branch 'ft/footer'
Your branch is ahead of 'origin/ft/footer' by 1 commit.
  (use "git push" to publish your local commits)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/footer)
$ git commit -am "modify home page more " --amend
[ft/footer 6bfa451] modify home page more
 Date: Fri May 19 16:22:37 2023 +0200
 2 files changed, 2 insertions(+), 13 deletions(-)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/footer)
$ git checkout ft/squashing
Switched to branch 'ft/squashing'

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/squashing)
$ git merge ft/footer
Updating 4e7eda0..6bfa451
Fast-forward
 home.html  |  2 +-
 index.html | 13 +------------
 2 files changed, 2 insertions(+), 13 deletions(-)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/squashing)
$ git commit -am "footer changes squashing"
[ft/squashing 02f61e4] footer changes squashing
 1 file changed, 2 insertions(+)

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/squashing)
$ git push -u origin ft/squashing 
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 2 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 771 bytes | 30.00 KiB/s, done.
Total 7 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/jeremiech/the-gym-repos-dedicated/pull/new/ft/squashing
remote:
To https://github.com/jeremiech/the-gym-repos-dedicated.git
 * [new branch]      ft/squashing -> ft/squashing
branch 'ft/squashing' set up to track 'origin/ft/squashing'.

Izere@DESKTOP-9TB6QQ1 MINGW64 ~/Documents/on-firday/the-gym-repos-dedicated (ft/squashing)
$
 
 
 
 
