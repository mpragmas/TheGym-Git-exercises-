## Git bundle1 - Exercise1

```bash
HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1 (main)
$ mkdir 1

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1 (main)
$ cd 1

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ echo "File" > file2.txt

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ rm file2.txt

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ touch index.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ touch readMe.md

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git init
Initialized empty Git repository in C:/Users/HP/Documents/lesson/TheGym/git/1/1/.git/

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (master)
$ git add .

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (master)
$ git commit -m "first commit"
[master (root-commit) 7711c7d] first commit
 2 files changed, 12 insertions(+)
 create mode 100644 index.html
 create mode 100644 readMe.md

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (master)
$ git branch -M main

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git branch
* main

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git remote add origin https://github.com/mpragmas/bundle-1---exercise-1.git

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 443 bytes | 147.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/mpragmas/bundle-1---exercise-1.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git checkout -b dev
Switched to a new branch 'dev'

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (dev)
$ git checkout -b test
Switched to a new branch 'test'

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (test)
$ git checkout dev
Switched to branch 'dev'

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (dev)
$ git branch
* dev
  main
  test

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (dev)
$ git branch -d test
Deleted branch test (was 7711c7d).

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (dev)
$ git branch
* dev
  main

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (dev)
$
```

## Git bundle1 - Exercise1

```bash
HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git add home.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html


HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash list

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash
Saved working directory and index state WIP on main: 2377b92 updated readMe

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash list
stash@{0}: WIP on main: 2377b92 updated readMe

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped refs/stash@{0} (fc5c595a4092d598050670b1490600234927bc51)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash
Saved working directory and index state WIP on main: 2377b92 updated readMe

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ touch home.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash pop
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped refs/stash@{0} (125fd8622520ca464dea82c7b81ae2944907e453)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ touch about.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash list

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash
Saved working directory and index state WIP on main: 2377b92 updated readMe

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash
No local changes to save

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git add about.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html


HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash
Saved working directory and index state WIP on main: 2377b92 updated readMe

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ touch team.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git add team.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash
Saved working directory and index state WIP on main: 2377b92 updated readMe

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash list
stash@{0}: WIP on main: 2377b92 updated readMe
stash@{1}: WIP on main: 2377b92 updated readMe
stash@{2}: WIP on main: 2377b92 updated readMe

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (26ba51708e6b23086dd7ac99c1a4460912591698)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash list
stash@{0}: WIP on main: 2377b92 updated readMe
stash@{1}: WIP on main: 2377b92 updated readMe

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (34c1fcbc7e2014984dfe00dc061d23063adc4d72)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git add .

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git commit -m "added about.html and home.html"
[main 5a26a96] added about.html and home.html
 2 files changed, 20 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash pop stash@{0}
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (b73688449f894b86df63ecc1a05dc16a769aeed4)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git reset

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git reset --hard
HEAD is now at 5a26a96 added about.html and home.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git reset HEAD

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 527 bytes | 263.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
remote: This repository moved. Please use the new location:
remote:   https://github.com/mpragmas/TheGym-Git-exercises-.git
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 527 bytes | 263.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Enumerating objects: 5, done.
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 527 bytes | 263.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
remote: This repository moved. Please use the new location:
remote:   https://github.com/mpragmas/TheGym-Git-exercises-.git
To https://github.com/mpragmas/bundle-1---exercise-1.git
   2377b92..5a26a96  main -> main

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$

```
