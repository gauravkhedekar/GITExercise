# Branching Exercise

1. Make a new folder called `Patronus`
2. Make a new git repo inside the folder (make sure you're not in an existing repo)
3. Create a new file called `patronus.txt` (leave it empty for now)
4. Add and commit the empty file, with the message "add empty patronus file"
5. Immediately make a new branch called `harry` and another branch called `snape` (both based on the master branch)
6. Move to the `harry` branch using the "new" command to change branches.
7. In the `patronus.txt` file, add the following:
    
    ```
    HARRY'S PATRONUS
    
       /|       |\
    `__\\       //__'
       ||      ||
     \__`\     |'__/
       `_\\   //_'
       _.,:---;,._
       \_:     :_/
         |@. .@|
         |     |
         ,\.-./ \
         ;;`-'   `---__________-----.-.
         ;;;                         \_\
         ';;;                         |
          ;    |                      ;
           \   \     \        |      /
            \_, \    /        \     |\
              |';|  |,,,,,,,,/ \    \ \_
              |  |  |           \   /   |
              \  \  |           |  / \  |
               | || |           | |   | |
               | || |           | |   | |
               | || |           | |   | |
               |_||_|           |_|   |_|
              /_//_/           /_/   /_/
    ```
    
8. Add and commit the changes, with the commit message "add harry's stag patronus"
9. Move over to the `snape` branch using the "older" command to change branches.
10.  Put the following text in  the `patronus.txt` file:
    
    ```
    SNAPE'S PATRONUS
                       .     _,
                       |`\__/ /
                       \  . .(
                        | __T|
                       /   |
          _.---======='    |
         //               {}
        `|      ,   ,     {}
         \      /___;    ,'
          ) ,-;`    `\  //
         | / (        ;||
         ||`\\        |||
         ||  \\       |||
         )\   )\      )||
         `"   `"      `""
    ```
    
11. Add and commit the changes on the `snape` branch with the commit message "add snape's doe patronus"
12. Next, create a new branch based upon the `snape` branch called `lily`
13. Move to the `lily` branch
14. Edit the `patronus.txt` file so that it says `LILY'S PATRONUS` at the top instead of
`SNAPE'S PATRONUS` (leave the doe ascii-art alone)
15. Add and commit the change with the message "add lily's doe patronus"
16. Run a git command to list all branches (you should see 4)
17. **Bonus:** delete the `snape` branch (poor Snape)


# ANSWER

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (master)
$ touch patronus.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (master)
$ git add patronus.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (master)
$ git commit -m "add empty patronus file"
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (master)
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (master)
$ git branch harry

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (master)
$ git branch snape

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (master)
$ git checkout harry
Switched to branch 'harry'

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (harry)
$ vi patronus.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (harry)
$ git add patronus.txt
warning: in the working copy of 'Patronus/patronus.txt', LF will be replaced by CRLF the next time Git touches it

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (harry)
$ git commit -m "add harry's stag patronus"
[harry 5c62484] add harry's stag patronus
 1 file changed, 26 insertions(+)

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (harry)
$ git checkout snape
Switched to branch 'snape'

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (snape)
$ vi patronus.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (snape)
$ git add patronus.txt
warning: in the working copy of 'Patronus/patronus.txt', LF will be replaced by CRLF the next time Git touches it

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (snape)
$ git commit -m "add snape's doe patronus"
[snape c86fbed] add snape's doe patronus
 1 file changed, 16 insertions(+)

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (snape)
$ git branch lily

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (snape)
$ git checkout lily
Switched to branch 'lily'

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (lily)
$ vi patronus.txt

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (lily)
$ git add patronus.txt
warning: in the working copy of 'Patronus/patronus.txt', LF will be replaced by CRLF the next time Git touches it

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (lily)
$ git commit -m "add lily's doe patronus"
[lily 0873681] add lily's doe patronus
 1 file changed, 1 insertion(+), 1 deletion(-)

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (lily)
$ git branch
  harry
* lily
  master
  snape

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (lily)
$ git branch --delete snape
Deleted branch snape (was c86fbed).

91986@LAPTOP-A9NL7THK MINGW64 ~/Documents/GITExercise/Patronus (lily)
$ git branch
  harry
* lily
  master

