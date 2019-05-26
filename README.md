The best way to undo previous changes to the source code repository is to learn how to revert a git commit.

By Cameron McKenzie

In the name of simplicity, this git revert example will start off with a completely clean repository. Create five HTML files, and perform a git commit with each one. To keep track of the commit history, each commit will include the commit number along with the count of the number of files in the working tree.
```
$ echo 'alice' > alpha.html
$ git add alpha.html && git commit -m "1st git commit: 1 file"
```
```
$ echo 'becky' > beta.html
$ git add beta.html && git commit -m "2nd git commit: 2 files"
```
```
$ echo 'callie' > charlie.html
$ git add charlie.html && git commit -m "3rd git commit: 3 files"
```
```
$ echo 'diana' > delta.html
$ git add delta.html && git commit -m "4th git commit: 4 files"
```
```
$ echo 'ellen' > edison.html
$ git add edison.html && git commit -m "5th git commit: 5 files"
```
```
$ git push 
```
To recap this git revert example, we have created five HTML files and executed a commit for each one. We can look at the history if we invoke the git reflog command
```
$ git reflog
76ee08d (HEAD -> master) HEAD@{0}: commit: 5th git commit: 5 files
6c6cb47 HEAD@{1}: commit: 4th git commit: 4 files
0b181ce HEAD@{2}: commit: 3rd git commit: 3 files
8fe9301 HEAD@{3}: commit: 2nd git commit: 2 files
d04567e HEAD@{4}: commit: 1st git commit: 1 file
652d5a9 (origin/master) HEAD@{5}: commit (initial): Adding README.md
```
How to revert git commit 0b181ce?
```
$ git revert 0b181ce
$ echo 'charlotte' > charlie.html
$ git add charlie.html && git commit -m "7rd git commit: 3 files"
$ git push
```
