# Branching in Git 
Branching is a powerful feature in Git that allows you to create separate lines of development within a repository. This enables multiple developers to work on different features or bug fixes simultaneously without interfering with each other's work.
## Creating a Branch
To create a new branch in Git, use the following command:
```bash
git branch <branch-name>
```
This command creates a new branch called `<branch-name>` based on the current branch.
## Switching Between Branches
To switch to a different branch, use the `git checkout` command:
```bash
git checkout <branch-name>
```
This command updates your working directory to reflect the state of the specified branch.
## Creating and Switching to a New Branch
You can create and switch to a new branch in a single command using the `-b`
option:
```bash
git checkout -b <branch-name>
```
This command creates a new branch called `<branch-name>` and switches to it immediately.
## Merging Branches
Once you have completed your work on a branch, you can merge it back into another branch (
usually the main branch) using the `git merge` command:
```bash
git checkout main
git merge <branch-name>
```
This command switches to the `main` branch and merges the changes from `<branch-name>` into it.
## Deleting a Branch
After merging a branch, you may want to delete it to keep your repository clean. Use the following command to delete a branch:
```bash
git branch -d <branch-name>
```
This command deletes the specified branch. If the branch has not been merged, you can use the `-D` option to force deletion:
```bash
git branch -D <branch-name>
```
## Viewing Branches
To view all branches in your repository, use the following command:
```bash
git branch
```
This command lists all branches, with the current branch highlighted with an asterisk (*).
## Additional Resources
- [Git Branching Documentation](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)
- [Atlassian Git Branching Guide](https://www.atlassian.com/git/tutorials/using-branches)
- [Git Branching Strategies](https://nvie.com/posts/a-successful-git-branching-model/)
Feel free to explore these resources to deepen your understanding of branching in Git!

