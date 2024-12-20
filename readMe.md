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

## Git bundle1 - Exercise2

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
$ git stash
Saved working directory and index state WIP on main: 2377b92 updated readMe

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git stash list
stash@{0}: WIP on main: 2377b92 updated readMe


HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ touch about.html

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
$ git reset --hard
HEAD is now at 5a26a96 added about.html and home.html


```

## Git bundle2 - Exercise1

```bash

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/bundle-2)
$ touch services.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/bundle-2)
$ git add services.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/bundle-2)
$ git commit -m "added servces page"
[ft/bundle-2 3703bc6] added servces page
 1 file changed, 9 insertions(+)
 create mode 100644 services.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/bundle-2)
$  git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 423 bytes | 211.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: This repository moved. Please use the new location:
remote:   https://github.com/mpragmas/TheGym-Git-exercises-.git
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/mpragmas/TheGym-Git-exercises-/pull/new/ft/bundle-2
remote:
To https://github.com/mpragmas/bundle-1---exercise-1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/bundle-2|MERGING)
$ git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 2 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git pull
Updating 3d78b2b..6347fe8
Fast-forward
 services.html | 9 +++++++++
 1 file changed, 9 insertions(+)
 create mode 100644 services.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1023 bytes | 341.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote: https://github.com/mpragmas/TheGym-Git-exercises-.git
To https://github.com/mpragmas/bundle-1---exercise-1.git
6347fe8..765d57d main -> main

```

## Git bundle2 - Exercise2

```bash

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)heGym/git/1/1 (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.  heGym/git/1/1 (main)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$  git pull
Already up to date.

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign)
$ git add --all


HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign)
$ git commit -m "added service list"
[ft/service-redesign 91dab6f] added service list
 1 file changed, 4 insertions(+), 1 deletion(-)


HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches
without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.



HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign)
$  git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 343 bytes | 68.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.bjects.
remote: This repository moved. Please use the new location:   t
remote:   https://github.com/mpragmas/TheGym-Git-exercises-.git                                                             Hub by visiting:
remote:                                                       /pull/new/ft/service-redesign
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/mpragmas/TheGym-Git-exercises-n/pull/new/ft/service-redesign                                 e-redesign'.
remote:
To https://github.com/mpragmas/bundle-1---exercise-1.git      ft/service-redesign)
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git add --all

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git commit -m "added old service list"
[main 6dec671] added old service list
 1 file changed, 6 insertions(+), 1 deletion(-)

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 352 bytes | 352.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/mpragmas/TheGym-Git-exercises-.git
To https://github.com/mpragmas/bundle-1---exercise-1.git
   73d0751..6dec671  main -> main

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (main)
$ git checkout  ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
Merge branch 'main' into ft/service-redesign

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign|MERGING)
$ git add services.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign|MERGING)
$ git commit
[ft/service-redesign e94d80e] Merge branch 'main' into ft/service-redesign

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign)
$ git diff main
diff --git a/services.html b/services.html
diff --git a/services.html b/services.html
index c081bc5..a30432f 100644
--- a/services.html
+++ b/services.html
@@ -6,7 +6,6 @@
     <title>Services Page</title>
   </head>
   <body>
-
     <h1>New Services</h1>
     <ul>
       <li>Booking</li>
@@ -18,6 +17,5 @@
       <li>Services 1</li>
       <li>Services 2</li>
     </ol>
Merge branch 'main' into ft/service-redesign

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign|MERGING)
$ git add --all services.html

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign|MERGING)
$ git commit
[ft/service-redesign 68d5ae4] Merge branch 'main' into ft/service-redesign

HP@DESKTOP-4982QG7 MINGW64 ~/Documents/lesson/TheGym/git/1/1 (ft/service-redesign)
$ git push
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 555 bytes | 277.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: This repository moved. Please use the new location:
remote:   https://github.com/mpragmas/TheGym-Git-exercises-.git
To https://github.com/mpragmas/bundle-1---exercise-1.git
   285fb34..68d5ae4  ft/service-redesign -> ft/service-redesign

```
