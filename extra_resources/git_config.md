# Git Config Commands

---

[Generate a new ssh key and add it to ssh agent](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

---

### Help / print all `git` commands 
`git`  
`git help`  

### Configure user name and email 
`git config --global user.name "First Last"`  
`git config --global user.email "myname@email.com"`  

### Cache GitHub password when using HTTPS
can use a credential helper to tell Git to remember your GitHub username and password every time it talks to GitHub.

Mac:  
`git config --global credential.helper osxkeychain`  (`osxkeychain helper` is required), 

### Set default editor
`git config --global core.editor "nano"`

---

## View list of configuration settings
`git config --list`

### Global Configuration File
#### Edit config file
```bash
nano /Users/reshamashaikh/.gitconfig
```

>my example  

```text

[filter "media"]
        required = true
        clean = git media clean %f
        smudge = git media smudge %f
[user]
        name = reshamas
        email = rs2715@gmail.com
        password = 123456789
[reshama]
        name = reshama
        email = rs2715@stern.nyu.edu
[push]
        default = simple
[core]
        editor = nano
        
```
