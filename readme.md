# Token = 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

# -- Configure Git With Username and Email

1.  git config --global user.name "Bhushan kumar"
2.  git config --global user.email "godwaha2003@gmail.com"

3.  git config --list OR git config user.name and git config user.email

--> For exist press -> (q)

# command :-> ls -la

- total 9
- drwxr-xr-x 1 My PC 197121 0 Jul 30 10:03 ./
- drwxr-xr-x 1 My PC 197121 0 Jul 30 09:22 ../
- drwxr-xr-x 1 My PC 197121 0 Jul 30 10:03 .git/

# command :-> git status

- It tell us which file or folder not add yet
- Shows in Red color

# command :-> git add .

- Now it shows filder or folder which is now added
- Shows in Green color

# command :- git commit -m "First v1 commit"

- [master (root-commit) 5a264bc] First v1 commit
- 1 file changed, 19 insertions(+)
- create mode 100644 readme.md

Yaha hamma dekhna koo mila kii ham jis Branch par hai voo Master branch hai

- [master (root-commit) 5a264bc]

# command :- git branch

- It used to check we are on which branch
- - master

# command :- git log

    It is used to check which user done commit and what

- commit 5a264bcccda70d81daa96d4839350185ef578d17 (HEAD -> master)
- Author: Bhushan kumar <godwaha2003@gmail.com>
- Date: Wed Jul 30 10:13:03 2025 +0530

  First v1 commit

# ------------ Practice Session -------------------

We changes some lines in our code ok

1. we used command :-> git status

- On branch master
- Changes not staged for commit:
- (use "git add <file>..." to update what will be committed)
- (use "git restore <file>..." to discard changes in working directory)
- modified: readme.md

Here "modified: readme.md" this was written in red text

Which shows us that readme.md file meh kuch modify kiya gaya hai.

2.  we used command :-> git diff

It is used to check which lines we changes or newly write or modified

3.  git add .

4.  command :-> git commit -m "commit V2"

    - [master 7365675] commit V2
    - 1 file changed, 48 insertions(+), 1 deletion(-)

5.  command :-> git log

- commit 7365675ad0c4b1c5f3c0727eb55f9a0a38e1157f (HEAD -> master)
- Author: Bhushan kumar <godwaha2003@gmail.com>
- Date: Wed Jul 30 10:36:48 2025 +0530
  commit V2

- commit 5a264bcccda70d81daa96d4839350185ef578d17
- Author: Bhushan kumar <godwaha2003@gmail.com>
- Date: Wed Jul 30 10:13:03 2025 +0530

  First v1 commit

# ------------ Practice Session End -------------------

# command :-> git show 5a264bcccda70d81daa96d4839350185ef578d17:readme.md

- Ishme hamma agar yeah dekha hai kii mera phela commit meh code
  kya tha toh hum ish command ka use karraga

- ishme git show (id):fileName

- Jish commit koo dekna hai ushkii id and ushka under
  jis file koo check karna hai ushka fileName

# command checkout

1.  command :-> git checkout 5a264bcccda70d81daa96d4839350185ef578d17 -- readme.md
2.  command :-> git checkout 5a264bcccda70d81daa96d4839350185ef578d17 -- \*

if we want to see the code of any version in our vs code File we use these commands

- If we want to see any version specific file we use command 1.
- But If we want to see all files of any version we use command 2.

3. command :-> git checkout master -- \*

- if we want to go again our working code that we worked in present we use this command

NOTE :-> All changes sees us in Files not in Terminal Ok

# ----------- Negative test cases ---------------

# CASE-A command :-> git restore

1. For all, command :-> git restore .
2. For indivdual, command :-> git restore

Suppose we made an mistake in any file of code and want again back code that was last committed , You can restore that code using these commands

# CASE-B  

 - - Added wrong files, by command -> git add .

- Suppose we made some changes and run command "git add ." , Further we see that
  the changes we made some of them are incorrect (Stagging area bolte hai ishe)

  - But we fire the command -> git add .

  - Now in this condition we Revert this command by using

  command :-> git restored --staged .

  - Ish command seh hogga yeah joh files stagging area meh challa gayi thi voh
    wappis aa jaya gi
  - Then hum wapis "git restore ." command ka use karke apna previous version par
    aa jaya geah

# CASE-B prctice session

1.  command :-> git add .

2.  command :-> git status

    (Shows in Green Color)

    - On branch master
    - Changes to be committed:
      (use "git restore --staged <file>..." to unstage)
      modified: readme.md

3.  command :-> git restore --staged .

4.  command :-> git status

    (Shows in REd Color again )

    - On branch master
    - Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git restore <file>..." to discard changes in working directory)
      modified: readme.md

    - no changes added to commit (use "git add" and/or "git commit -a")

    - NOTE :- If shows in green color means it is staged , but shows in red color
      means not staged or t=return fro the staged area

    - IMPORTANT NOTE :- NOW WE CAN AGAIN REACH TO OUR LAST VERSION USING
      COMMAND :-> git restore .

# CASE-C ( TIMELINE -> 40.14 )

# CASE-D 
 - commit wrong files 