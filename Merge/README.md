
# Git Merging Exercise

This exercise is a little bit different.  Rather than following my exact instructions step by step, I'd like for you to come up with your own scenarios that meet my requirements.

Start by creating a new repo.  Make a file or two in the repo for you to work on.

If you need some inspiration...I'll be working in a file called `greetings.txt` It will contain greetings in different languages.

## Part 1: Fast Forward Merge

**Your goal is to generate a fast forward merge. Demonstrate that you understand how FF merges work by creating one on your own!**

Make a new branch. Do some work in the repo such that when you merge the new branch into master, it results in a fast forward merge.  Merge that branch into master and see if you were right!






ANSWER for FASTFORWARD:


91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise (master)
$ mkdir Merge

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise (master)
$ cd Merge/

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ touch groceries.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ vi groceries.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git add groceries.txt
warning: in the working copy of 'Merge/groceries.txt', LF will be replaced by CRLF the next time Git touches it

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git commit -m "added 2 vegies"
[master b9b2951] added 2 vegies
 1 file changed, 3 insertions(+)
 create mode 100644 Merge/groceries.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git log
commit b9b2951c7e63fca836da8ca3c36e003f57eba677 (HEAD -> master)
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Wed May 3 16:23:17 2023 +0530

    added 2 vegies

commit bb1fc040be726766c88078774ed53bd417769170 (origin/master)
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Mon May 1 12:55:03 2023 +0530

    adding folders

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git switch -c icecreams
Switched to a new branch 'icecreams'

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ ls -lrt
total 1
-rw-r--r-- 1 91986 197609 15 May  3 16:22 groceries.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ vi groceries.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ vi groceries_icecream.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git add groceries_icecream.txt
warning: in the working copy of 'Merge/groceries_icecream.txt', LF will be replaced by CRLF the next time Git touches it

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git commit -m "added icecreams"
[icecreams 9b6cef4] added icecreams
 1 file changed, 2 insertions(+)
 create mode 100644 Merge/groceries_icecream.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git log
commit 9b6cef46ac9343e3b1f8567aa169f5ed7237a9e4 (HEAD -> icecreams)
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Wed May 3 16:24:57 2023 +0530

    added icecreams

commit b9b2951c7e63fca836da8ca3c36e003f57eba677 (master)
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Wed May 3 16:23:17 2023 +0530

    added 2 vegies

commit bb1fc040be726766c88078774ed53bd417769170 (origin/master)
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Mon May 1 12:55:03 2023 +0530

    adding folders

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ vi groceries.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git add groceries.txt
warning: in the working copy of 'Merge/groceries.txt', LF will be replaced by CRLF the next time Git touches it

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git commit -m "added curry leaves"
[icecreams 6820944] added curry leaves
 1 file changed, 1 insertion(+), 1 deletion(-)

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git log
commit 68209440c1ac77a0a4266642fc0fdc1a72365422 (HEAD -> icecreams)
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Wed May 3 16:25:51 2023 +0530

    added curry leaves

commit 9b6cef46ac9343e3b1f8567aa169f5ed7237a9e4
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Wed May 3 16:24:57 2023 +0530

    added icecreams

commit b9b2951c7e63fca836da8ca3c36e003f57eba677 (master)
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Wed May 3 16:23:17 2023 +0530

    added 2 vegies

commit bb1fc040be726766c88078774ed53bd417769170 (origin/master)
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Mon May 1 12:55:03 2023 +0530

    adding folders

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git switch master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ cat groceries.txt
tomato
potato


91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git merge icecreams
Updating b9b2951..6820944
Fast-forward
 Merge/groceries.txt          | 2 +-
 Merge/groceries_icecream.txt | 2 ++
 2 files changed, 3 insertions(+), 1 deletion(-)
 create mode 100644 Merge/groceries_icecream.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ cat groceries.txt
tomato
potato
curry leaves

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ cat groceries_icecream.txt.txt
cat: groceries_icecream.txt.txt: No such file or directory

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ cat groceries_icecream.txt
Amul
Rajbhog




## Part 2: Merge Commit (No Conflicts)

Your goal is to generate a merge commit with NO MERGE CONFLICTS.

Create a new branch. Make some changes to the repo such that when you merge the new branch into master, it results in a merge commit.  The merge should not result in any conflicts. Merge that branch into master and see if you were right!

# ANSWER

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ vi testMergeWithoutCOnflic.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git add testMergeWithoutCOnflic.txt
warning: in the working copy of 'Merge/testMergeWithoutCOnflic.txt', LF will be replaced by CRLF the next time Git touches it

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git commit -m "added some lines in new testMergeWithoutCOnflic.txt"
[master 7aca749] added some lines in new testMergeWithoutCOnflic.txt
 1 file changed, 1 insertion(+)

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git log
commit 7aca7493faf2f196bd4c85edff7327035fe7ef65 (HEAD -> master)
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Wed May 3 17:22:34 2023 +0530

    added some lines in new testMergeWithoutCOnflic.txt

commit 37b5fdaff4126fe431809bd61b963a9219522a41
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Wed May 3 17:20:21 2023 +0530

    added file for merge without conflict

commit d859901c9e53f0e44d2e9434e03a5f1e41ce7a7a
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Wed May 3 16:48:22 2023 +0530

    added nonveg

commit 6920e530524708ddb89e2607e4134a41ec73670b
Author: gauravkhedekar <khedekarg9@gmail.com>
Date:   Wed May 3 16:44:32 2023 +0530

    added some more leaves

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git merge icecreams
Merge made by the 'ort' strategy.
 Merge/testfromicecreams1.txt | 0
 Merge/testfromicecreams2.txt | 0
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Merge/testfromicecreams1.txt
 create mode 100644 Merge/testfromicecreams2.txt


## Part 3: Conflicts!

Your goal is to generate merge a conflict!

Create a new branch.  Make some changes to the repo such that when you merge the new branch into the master branch, it results in a merge conflict. Merge that branch into master and see if you were right! Resolve the conflict!



#ANSWER

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ vi testMergeWithConflict.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git switch icecreams
Switched to branch 'icecreams'

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git switch master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.


91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ less
Missing filename ("less --help" for help)

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ less testMergeWithConflict.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git add testMergeWithConflict.txt
warning: in the working copy of 'Merge/testMergeWithConflict.txt', LF will be replaced by CRLF the next time Git touches it

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   testMergeWithConflict.txt


91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git commit -m "added conflicting file"
[master eb8a04b] added conflicting file
 1 file changed, 1 insertion(+)
 create mode 100644 Merge/testMergeWithConflict.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git switch icecreams
Switched to branch 'icecreams'

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git merge master
Merge made by the 'ort' strategy.
 Merge/README.md                   | 60 +++++++++++++++++++++++++++++++++++++++
 Merge/testMergeWithConflict.txt   |  1 +
 Merge/testMergeWithoutCOnflic.txt |  1 +
 3 files changed, 62 insertions(+)
 create mode 100644 Merge/testMergeWithConflict.txt
 create mode 100644 Merge/testMergeWithoutCOnflic.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ ls -lrt
total 18
-rw-r--r-- 1 91986 197609   15 May  3 16:26 groceries_icecream.txt
-rw-r--r-- 1 91986 197609    9 May  3 16:49 Nonveg.txt
-rw-r--r-- 1 91986 197609   48 May  3 16:49 groceries.txt
-rw-r--r-- 1 91986 197609    0 May  3 17:22 testfromicecreams1.txt
-rw-r--r-- 1 91986 197609    0 May  3 17:22 testfromicecreams2.txt
-rw-r--r-- 1 91986 197609   14 May  3 19:07 new_icecreams.txt
-rw-r--r-- 1 91986 197609   30 May  3 19:07 testMergeWithoutCOnflic.txt
-rw-r--r-- 1 91986 197609   92 May  3 19:07 testMergeWithConflict.txt
-rw-r--r-- 1 91986 197609 8288 May  3 19:07 README.md

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ vi testMergeWithConflict.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git add testMergeWithConflict.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git commit -m "added amount of icecreams in conflicting file"
[icecreams 8068a14] added amount of icecreams in conflicting file
 1 file changed, 1 insertion(+), 1 deletion(-)

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (icecreams)
$ git switch master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)


91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ vi testMergeWithConflict.txt


91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git commit -m "added conflicting msg in testMergeWithConflict.txt"
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   testMergeWithConflict.txt

no changes added to commit (use "git add" and/or "git commit -a")

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git add testMergeWithConflict.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git commit -m "added conflicting msg in testMergeWithConflict.txt"
[master 853e2d2] added conflicting msg in testMergeWithConflict.txt
 1 file changed, 1 insertion(+), 1 deletion(-)

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git merge icecreams
Auto-merging Merge/testMergeWithConflict.txt
CONFLICT (content): Merge conflict in Merge/testMergeWithConflict.txt
Automatic merge failed; fix conflicts and then commit the result.

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master|MERGING)
$ vi testMergeWithConflict.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master|MERGING)
$ git merge icecreams
error: Merging is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master|MERGING)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Changes to be committed:
        new file:   new_icecreams.txt

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   testMergeWithConflict.txt


91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master|MERGING)
$ git add testMergeWithConflict.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master|MERGING)
$ git merge icecreams
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master|MERGING)
$ git commit -m "keeping data from icecreams branch"
[master 59d1ab6] keeping data from icecreams branch

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Merge (master)
$ git merge icecreams
Already up to date.

