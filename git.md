# GIT

### Introduction

* Git is distributed version control system
* It's kind of repository which keep track of the file which is been added or updated
* Distributed version control system means multiple developer or team can work in same repository or code base i.e **collaboration**. Collaboration means we as a developer can update same file at same time

`Git is local repository. Project created on github or gitlab is called remote repository`

### Commands

|commands | description |
|---------|-------------|
|git init .| It will initialize empty git repository in folder(Its a hidden folder)|
|git add| File is been added at stagging area|
|git commit -m "message" | Save add the changes in the repository with a message|
|git remote add origin <repo_link>| Add file to remote repository while pushing for first time|
|git push origin branch_name| Push the commited file form local to remote repository|
|git log | Display all the commit history|
|git show commit_id | It show what was been updated or modified in that commit |
|git diff | Use to show the changes before commiting |
|git status | It display the state of the working directory and the staging area |
|git branch| will display number of branches created and will also point on which branch you currently are. |
|git branch branch_name | will create a new branch |
|git branch <branch_name> -D or -d | to delete the branch |
|git checkout branch_name | It is used to switch from one branch to another branch |
|git checkout -- filename | It is also use to revert the changes. If multiple file are deleted use (git checkout --)|
|git pull origin branch_name | use to pull from remote server|

```
Note:- You cant push the code if remote server is ahead. So you will first need to pull and then push 
```


  