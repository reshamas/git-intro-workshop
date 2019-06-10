# Branches
* Branching means you diverge from the main line of development and continue to do work without changing the main line

### Why use branches?
 * independent line of development
 * think of them as a way to request a brand new working directory, staging area, and project history
 * in Git, branches are a part of your everyday development process. 
    * when you want to add a new feature or fix a bug—no matter how big or how small,  spawn a new branch to encapsulate your changes
    * this makes sure that unstable code is never committed to the main code base
    * it gives you the chance to clean up your feature’s history before merging it into the main branch


---
## Starting out with Branches
### Create a branch
```bash
git branch
git branch reshama_wip
git branch
```

### Switch to working branch
```bash
git checkout reshama_wip
```

---

**Note:  'wip' = 'work in progress'**    

---
## Branch Commands

 * **List branches**  
    `$ git branch`
 * **Create a new branch**  
    `$ git branch reshama_wip`
 * **Navigate between branches**  
    `$ git checkout branchname`
 * **Create and switch to branch** (2 steps in 1 line)  
    `$ git checkout -b testbranch`

 * **Delete a branch** (safe delete; won't delete if there are unmerged changes)  
    `$ git branch -d reshama_wip`
 * **Delete a branch** (force delete; will delete even if branch has unmerged changes)  
    `$ git branch -D reshama_wip`


 * **Rename a branch** (whichever is the current one, be careful)  
    `$ git branch -m newone_wip`
 * **Rename a branch** (can specify oldname and newname)  
    `$ git branch -m <oldname> <newname>`


 * **Back to main branch**  
    `$ git checkout master`
 * **Merge branches** (will merge specified <branchname> into current branch)  
    `$ git merge <branchname>`

---
## Pushing to Branches
`git push <remote_name> <branch_name>`  
Example:    
`git push origin reshama_wip`

---
## Copying from Branches

#### Copy file/folder from one branch to current branch (`master`)

Run this from the branch where you want the file to end up:  
on:  `master` branch
```
git checkout branch_wip myfile.txt
```

#### Copy directory from one branch to current branch (`master`)
on:  `master` branch
```
git checkout branch_wip myfolder/** 
```

---

## Aside: Working Practice
#### Launch notebook from working branch (leave master branch intact)
```bash
~/git_work/data-science-from-scratch  reshama_wip ✔                                498d  
▶ jupyter notebook
```

### Resource for Tutorial
[Helpful Tutorial:  Using Branches on Git](https://www.atlassian.com/git/tutorials/using-branches)  
