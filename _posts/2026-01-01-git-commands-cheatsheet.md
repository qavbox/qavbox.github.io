---
title: "Git Commands Cheatsheet"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - GIT
  - readability
  - standard
---

# **Git Commands Cheatsheet**

GitHub is one of the popular code repositories and also used as a version control tool. Git provides various commands to perform operations like pushing code to a remote repo, pulling code (from somebody else or from the central repo), and many other tasks.

Here we will list out the most commonly used Git commands.

---

## **Git Username or Email Setup**

```
//Global setup
git config --global user.name "YourUserName"
git config --global user.email "name@email.com"

//to set the username locally
git config user.name "AnyUserName" 

//to get the user name
git config user.name  //will give you the user name associated currently

//to reset user name and email
git config --global --unset user.name
git config --global --unset user.email
git config --global --unset user.password
```

Note : 

If you are MAC user then you can open KeyChain Access Application from finder and then look for your account listed there. Just click on it and update your password. Now give a try and things will fall in place.

If you are on Windows 10 with Git Remove/update related Credentials stored in Windows Credentials – >>Control Panel\All Control Panel Items\Credential Manager

If you are using multiple github accounts, then best option is to use github desktop [available for mac and windows OS], install and clone a repo or browse for an existing repo, this will ask username and password to authenticate separately for each repo.

## **Clone the Code**
```bash
git clone <repository-url>
```

---

## **Pull the Latest Code**
```bash
git pull
```
- Applies remote repository changes to the local repository.
- Equivalent to:
```bash
git pull = git fetch + git merge
```

---

## **Fetch Changes**
```bash
git fetch
```
- Informs the local repository that there are new changes in the remote repository **without applying/merging them**.

---

## **Push Local Project to Git (First Time)**
1. Create a repo on GitHub.
2. On local drive, add files.
3. Navigate to the project directory in the command prompt.

---

## **Push Local Changes to Git**
- For a new local branch:
```bash
git push origin <branch-name>
```
- Ensure:
```bash
git remote -v
```
shows:
```
git@github.com:userName/repoName
```
Else, set the URL explicitly.

---

### **Cancel Local Git Repo**
```bash
rm -rf .git
```

---

### **Stage & Unstage Files**
- Stage all changes:
```bash
git add .
```
- Unstage a specific file:
```bash
git reset <fileName>
```
- Unstage all files:
```bash
git reset
```

---

### **Undo Changes**
```bash
git checkout <filename_with_path>
```
- To undo any local changes.

---

## **Git Stash Commands**
*(Add stash examples if needed)*

---

## **Branch Commands**
- Delete a branch:
```bash
git branch -d <branch-name>
```
- List branches:
```bash
git branch
```

---

## **Check Associated Remote Repo**
```bash
git remote -v
```

---

## **.gitignore**
- Ignore files and folders from being pushed to remote repo.
- For more ways to ignore files or extensions, refer:  
[Atlassian Gitignore Guide](https://www.atlassian.com/git/tutorials/saving-changes/gitignore)

---

## **Change or Remove Remote URL**
- Change remote URL:
```bash
git remote set-url origin git://new.url.here
```
- Remove current remote:
```bash
git remote remove origin
```
