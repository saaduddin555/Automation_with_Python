
git config -l                                                                      =To Know User Info

cat example_commit.txt

git log

diff and patch Cheat Sheet
diff
diff is used to find differences between two files. On its own, it’s a bit hard to use; instead, use it with diff -u to find lines which differ in two files:

diff -u
diff -u is used to compare two files, line by line, and have the differing lines compared side-by-side in the same output. See below:

Example:

~$ cat menu1.txt 
Menu1:

Apples
Bananas
Oranges
Pears

~$ cat menu2.txt 
Menu:

Apples
Bananas
Grapes
Strawberries

~$ diff -u menu1.txt menu2.txt 
--- menu1.txt   2019-12-16 18:46:13.794879924 +0900
+++ menu2.txt   2019-12-16 18:46:42.090995670 +0900
@@ -1,6 +1,6 @@
-Menu1:
+Menu:
 
 Apples
 Bananas
-Oranges
-Pears
+Grapes
+Strawberries

Patch
Patch is useful for applying file differences. See the below example, which compares two files. The comparison is saved as a .diff file, which is then patched to the original file!

~$ cat hello_world.txt 
Hello World
~$ cat hello_world_long.txt 
Hello World

It's a wonderful day!
~$ diff -u hello_world.txt hello_world_long.txt 
--- hello_world.txt     2019-12-16 19:24:12.556102821 +0900
+++ hello_world_long.txt        2019-12-16 19:24:38.944207773 +0900
@@ -1 +1,3 @@
 Hello World
+
+It's a wonderful day!
~$ diff -u hello_world.txt hello_world_long.txt > hello_world.diff
~$ patch < hello_world.diff 
patching file hello_world.txt
~$ cat hello_world.txt 
Hello World

It's a wonderful day!
---

git show <commit_id>                             =TO describe commit id  Taking the commit ID, git show will show information about the commit and its associated patch.


git commit -a

Stages files automatically

git log -p

Produces patch text

git show

Shows various objects

git diff

Is similar to the Linux `diff` command, and can show the differences in various commits

git diff --staged

An alias to --cached, this will show all staged files compared to the named commit

git add -p

Allows a user to interactively review patches to add to the current commit

git mv

Similar to the Linux `mv` command, this moves a file

git rm

Similar to the Linux `rm` command, this deletes, or removes a file


.gitignore files
.gitignore files are used to tell the git tool to intentionally ignore some files in a given Git repository. For example, this can be useful for configuration files or metadata files that a user may not want to check into the master branch. Check out more at: https://git-scm.com/docs/gitignore.

A few common examples of file patterns to exclude can be found here. https://gist.github.com/octocat/9257657
---

Undoing Things:

git checkout                                  It reverts changes to modified files before they are staged.

git reset head <file_name>                    It reverse the changes in staging area what we have added with git add command.

git reset -p                                  Uses specific what we to reset the changes


Amending Commits:

The Missing files are ammended in to that recent commit or which we have missed to commit the file using amend option











Git Revert Cheat :

git checkout                         is effectively used to switch branches.

git reset         basically resets the repo, throwing away some changes. It’s somewhat difficult to understand, so reading the examples in the documentation may be a bit more useful.

There are some other useful articles online, which discuss more aggressive approaches to resetting the repo.

git commit --amend                    is used to make changes to commits after-the-fact, which can be useful for making notes about a given commit.

git revert                            makes a new commit which effectively rolls back a previous commit. It’s a bit like an undo command.

There are a few ways you can rollback commits in Git.












































































