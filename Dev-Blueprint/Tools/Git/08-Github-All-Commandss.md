# GitHub All Commands
This section provides a comprehensive list of commonly used Git commands for interacting with GitHub repositories. These commands cover a range of tasks, from cloning repositories to managing branches and handling pull requests.
## Table of Contents
- [Cloning a Repository](#cloning-a-repository)
- [Creating a New Repository](#creating-a-new-repository)
- [Forking a Repository](#forking-a-repository)
- [Creating and Managing Branches](#creating-and-managing-branches)
- [Committing Changes](#committing-changes)
- [Pushing Changes](#pushing-changes)
- [Creating Pull Requests](#creating-pull-requests)
- [Merging Pull Requests](#merging-pull-requests)
## Cloning a Repository
To clone a GitHub repository to your local machine, use the following command:
```bash 
git clone <repository-url>
```
This command creates a local copy of the repository on your machine.
## Creating a New Repository
To create a new repository on GitHub, you typically do this through the GitHub web interface. After creating the repository, you can initialize it locally with:
```bash
git init
git remote add origin <repository-url>
```
## Forking a Repository
To fork a repository on GitHub, navigate to the repository page and click the "Fork" button. This creates a copy of the repository under your GitHub account. You can then clone your forked repository using:
```bash 
git clone <your-forked-repository-url>
```
## Creating and Managing Branches
To create a new branch, use:
```bash
git checkout -b <branch-name>
```
To switch between branches, use:
```bash
git checkout <branch-name>
```
To see all branches, use:
```bash
git branch
```
## Committing Changes
To commit changes to your local repository, first stage the changes:
```bash
git add <file-or-directory>
```
Then commit the changes with a message:
```bash
git commit -m "Your commit message"
```
## Pushing Changes
To push your local commits to the remote GitHub repository, use:
```bash
git push origin <branch-name>
```
## Creating Pull Requests
After pushing your changes to a branch on GitHub, you can create a pull request (PR) through the GitHub web interface. Navigate to your repository, switch to the branch with your changes, and click the "New pull request" button.
## Merging Pull Requests    
Once a pull request has been reviewed and approved, you can merge it into the main branch using the GitHub web interface. Click the "Merge pull request" button on the PR page. Alternatively, you can merge it locally with:
```bash
git checkout main
git pull origin main
git merge <branch-name>
git push origin main
```
By using these commands, you can effectively manage your GitHub repositories and collaborate with others on your projects.

    