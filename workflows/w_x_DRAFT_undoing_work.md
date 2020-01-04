# Workflow x:  Advanced

## Advanced Course
- `.gitignore` (create data/ folder, .ipynb, wget a text file)
- undo changes
- add a license
- work with two branches
- use `git diff`
- shell plugins
- `git fetch`
- `git rebase`






---

## Step 1: Let's "clone" a repo from GitHub to our terminal

>my example  
```text
https://github.com/reshamas/git-intro-workshop
```

## Step 2:  go to working directory (your local terminal)
Go to your working directory:  
<kbd> cd ~/Desktop/gitsample </kbd>

>my example
```bash
cd ~/Desktop/gitsample
```


## Step 3:  clone the repo  
<kbd> git clone <url_name> </kbd> 
>my example
```bash
git clone git@github.com:reshamas/git-intro-workshop.git
```
  
## Step 4:  `cd` into the repo
<kbd> cd <repo_name> </kbd>
>my example
```bash
cd my_favorites
```

## Step 5:  create a file: fruit.txt
```txt
apple
banana
pear
```

## Step 6:  add the file
```bash
git add fruit.txt
```
