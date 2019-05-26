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
