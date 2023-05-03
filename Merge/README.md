
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

