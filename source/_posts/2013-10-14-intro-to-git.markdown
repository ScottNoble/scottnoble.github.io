---
layout: post
title: "Intro to Git"
date: 2013-10-14 17:51
comments: true
categories: 
---
In class we are learning to use Git and Github.
Git is a version control system or as a newbie to coding might think of it
Git is a "super fancy track changes"

Git has three "areas" that operate locally

The first is the working directory.
This is where you make changes to your file.

To create a working directory and initialize git for this directory you type
the following into the terminal:

```
mkdir practice
cd practice
git init
```

Now you can create files within this directory

```
echo "Hello World" > README
```
if you check the git status of your working directory you will see something like this

```
# On branch master
#
# Initial commit
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#	README
nothing added to commit but untracked files present (use "git add" to track)
```
Now you can move your Untracked file(s) to "the staging area" by running:

```
git add README
```
staging a file is like taking a snapshot of that file
Now, if you check git status you will see something like this:

```
# On branch master
#
# Initial commit
#
# Changes to be committed:
#   (use "git rm --cached <file>..." to unstage)
#
#	new file:   README
#
```
Now the file is tracked and ready to be committed.
You can either commit this or you can wait to commit multiple file changes
A hint would be that you might want to wait and commit multiple file changes if the changes are logically linked.

The next step is to commit the change to the git directory.
This is always accompanied by a comment explaining the changes that have been made.

```
git commit -m "added README file with 'Hello World'"
```
will produce something like this:
```
[master (root-commit) b914adf] added READ file with "Hello World"
 1 file changed, 1 insertion(+)
 create mode 100644 README
```
helpful tip is that if you enter git commit without a comment (because you are just so eager!)
you exit from VIM by pushing esc and typing :q! to return to your command line where you can commit with a comment

finally you can view the change you made by typing
```
git show
```
which will return:
```
commit b914adf636caa68126e86597ac9702735ce1d5fd
Author: Scott Noble <YYYYY@xxx.com>
Date:   Mon Oct 14 18:38:33 2013 -0600

    added READ file with "Hello World"

diff --git a/README b/README
new file mode 100644
index 0000000..557db03
--- /dev/null
+++ b/README
@@ -0,0 +1 @@
+Hello World
```
once you have made more changes you can look at a list of all the changes by entering

```
git log
```
this will return:

```
commit 4fc086902c6a20de6abfe6f56c630862c56e149c
Author: Scott Noble <xxx@yyy.com>
Date:   Mon Oct 14 18:50:21 2013 -0600

    added a line of text to README

commit b914adf636caa68126e86597ac9702735ce1d5fd
Author: Scott Noble <xxx@yyy.com>
Date:   Mon Oct 14 18:38:33 2013 -0600

    added READ file with "Hello World"
```

if you want to look at a specific change in the log you can copy the long code
called a "SHA-1 hash" and enter

```
git show 4fc086902c6a20de6abfe6f56c630862c56e149c
```
This will return the specific details of that individual commit.
If no SHA-1 hash is given with git show it will default to the details of your last commit.

With this knowledge you can track the different versions of your project locally as you make changes


