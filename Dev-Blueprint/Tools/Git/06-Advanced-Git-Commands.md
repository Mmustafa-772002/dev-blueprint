# Advanced Git Commands
In this section, we will explore some advanced Git commands that can help you manage your repositories more effectively. These commands are useful for more complex workflows and scenarios that go beyond basic version control.
## Table of Contents
- [Rebasing](#rebasing)
- [Cherry-Picking](#cherry-picking)
- [Stashing Changes](#stashing-changes)
- [Tagging](#tagging)   
- [Bisecting](#bisecting)
## Rebasing 
Rebasing is a powerful way to integrate changes from one branch into another. It allows you to maintain a linear project history. To rebase your current branch onto another branch, use:
```bash
git checkout <feature-branch></feature-branch>
git rebase <target-branch>
``` 
If there are conflicts during the rebase, Git will pause and allow you to resolve them. After resolving conflicts, use:
```bash 
git add <file-with-conflicts>
git rebase --continue
```
To abort a rebase in progress, use:
```bash
git rebase --abort
```
## Cherry-Picking
Cherry-picking allows you to apply a specific commit from one branch to another. This is useful
when you want to incorporate specific changes without merging entire branches. To cherry-pick a commit, use:
```bash
git checkout <target-branch>
git cherry-pick <commit-hash>
```
## Stashing Changes
Stashing is a way to temporarily save changes that are not yet ready to be committed. This is useful when you need to switch branches but want to keep your current work. To stash your changes, use:
```bash 
git stash
```
To apply the stashed changes later, use:
```bash 
git stash apply
```
To view the list of stashed changes, use:
```bash 
git stash list
```
To drop a specific stash, use:
```bash
git stash drop <stash@{index}>
``` 
## Tagging
Tagging is used to mark specific points in your repository's history, often for releases. To create a lightweight tag, use:
```bash
git tag <tag-name>
```
To create an annotated tag, use:
```bash
git tag -a <tag-name> -m "Tag message"
```
To push tags to a remote repository, use:
```bash
git push origin <tag-name>
```
To view all tags, use:
```bash
git tag
```
## Bisecting
Git bisect is a tool that helps you find the commit that introduced a bug by performing a binary search. To start a bisect session, use:
```bash
git bisect start
``` 
Mark the current commit as bad (the one with the bug):
```bash
git bisect bad
```
Mark a known good commit:
```bash
git bisect good <commit-hash>
```
Git will then checkout a commit in the middle of the range. Test this commit and mark it as good or bad:
```bash
git bisect good   # if the commit is good
git bisect bad    # if the commit is bad
```
Repeat this process until Git narrows down the commit that introduced the bug. Once done, reset the bisect session with
```bash
git bisect reset
```
By mastering these advanced Git commands, you can enhance your version control skills and manage complex development workflows more effectively. Happy coding!
