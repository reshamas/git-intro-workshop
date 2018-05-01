# Set Up

## Step 1:  Let Git Know Who You Are

### Configure user name and email 
`git config --global user.name "First Last"`  
`git config --global user.email "myname@email.com"`  

### Configure editor of choice
`git config --global core.editor "nano -w"` 

Other editor options can be found in [Setting Up Git](http://swcarpentry.github.io/git-novice/02-setup/)

### Configure simple push (do this one time only)
`git config --global push.default simple`

## Step 2. Create a Directory for Git Repos
Navigate to your home directory where you want to create a directory for the git work.  
For me, it is:  `/Users/reshamashaikh`  
<kbd> cd /Users/reshamashaikh </kbd>  

Create the directories:  
<kbd>  mkdir ds  </kbd>  
<kbd>  mkdir ds/gitsample </kbd>  
<kbd>  cd ds/gitsample </kbd>  
<kbd>  pwd </kbd>  
  
>my example
```bash
pwd
/Users/reshamashaikh
```
```bash
mkdir ds
mkdir ds/gitsample
cd ds/gitsample
pwd
/Users/reshamashaikh/ds/gitsample
```


