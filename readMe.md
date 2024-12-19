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
