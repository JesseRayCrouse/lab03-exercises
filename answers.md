# Lab 3 Answers

## Part 1: Git

### 1.1. List the contents of the lab03-exercises repo immediately after initialization
```
jesseraycrouse@Jesses-MacBook-Pro lab03-exercises % ls -la
total 0
drwxr-xr-x   3 jesseraycrouse  staff   96 Sep  4 10:24 .
drwxr-xr-x   7 jesseraycrouse  staff  224 Sep  4 10:20 ..
drwxr-xr-x  10 jesseraycrouse  staff  320 Sep  4 10:24 .git


```

### 1.2. Paste the output of your `git status` command
```
jesseraycrouse@Jesses-MacBook-Pro lab03-exercises % git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	README.md

nothing added to commit but untracked files present (use "git add" to track)

```

### 1.3. Paste the output of the state of your repository after committing your README.md file
```
jesseraycrouse@Jesses-MacBook-Pro lab03-exercises % git commit -m "Adding README to the new repository."
[main (root-commit) f85038f] Adding README to the new repository.
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md

```

### 1.4. Copy your `git log` output
```
jesseraycrouse@Jesses-MacBook-Pro lab03-exercises % git log
commit f85038f67eb01ee5c5a562a4f98d249436aef2a2 (HEAD -> main)
Author: Jesse <jcrouse10903@gmail.com>
Date:   Thu Sep 4 11:23:35 2025 -0400

    Adding README to the new repository.


```

### 1.5. Copy your `git diff` output
```
jesseraycrouse@Jesses-MacBook-Pro lab03-exercises % git diff
diff --git a/README.md b/README.md
index e69de29..78edd23 100644
--- a/README.md
+++ b/README.md
@@ -0,0 +1,17 @@
+def find_duplicates(nums):
+       seen = set()
+       duplicates = set()
+       for num in nums:
+               if num in seen:
+                       duplicates.add(num)
+               else:
+                       seen.add(num)
+       return list(duplicates)
+
+list = [1, 3, 5, 7, 1, 2, 9, 2, 3]
+
+duplicates = find_duplicates(list)
+
+print("Original list: " + str(list))
+
+print("Duplicate Integers: " + str(duplicates))

```


### 1.6. Reflection

We've learned 6 git subcommands now. Describe each of them in your own words in the section below:

* git init - this git command creates and initializes a new git repository.
* git status - this git command spits out the current status of files and changes in your current repository.
* git add - this git command adds any changes to the stage for comitting changes.
* git commit - this git command pushes any staged changes onto the repository.
* git log - this command spits out any recent changes and commits that were made to your current repository.
* git diff - this command shows you any differences in the current files in your directory. 


### 1.7. Practice: Find All Duplicates (Java)
Make sure you implement the `FindDuplicates.java` class as specified in the instructions (with the nested loops implementation).
 - DONE!
## Part 2: GitHub

### 2.1. Practice: Find All Duplicates (Python)
Make sure you implement the `find_duplicates.py` file as specified in the instructions (with the nested loops implementation).
 - DONE!

## Part 3: Branching

### 3.1. Implement the More Efficient Version of the "Find Duplicates" problem
Implement the more efficient Version of the "Find Duplicates" problem using a dictionary (or hashmap) data structure instead of nested loops. You may do this in either your Python file or in the Java file that you’ve already made. Do this by adding a second function/method to your Java/Python file with a slightly different name.


### 3.2. Link to Repo
Please make sure that the new repo that you made today on GitHub is public, and paste a link to it below.

```bash
https://github.com/JesseRayCrouse/lab03-exercises/tree/one-set
```

### 3.3. What do the three "Merge pull request" options mean? 
Describe each of them in your own words.
Create a merge commit - this is the standard merge commit, in which everything from the branch is then merged with main.
Squash and merge - this is similar to the standard merge commit, but it squashes every commit in the pull request into a single commit before merging with main.
Rebase and merge - this option of merging puts the branch you want to merge on top of the main branch, without a merge commit. This way won't work if you have any merge conflicts, which are a pain.
