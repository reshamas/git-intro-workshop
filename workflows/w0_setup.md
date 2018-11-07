
# Workflow 0: Setup


## Step 1:  Setup `ssh` keys (generate a key pair)
- ssh = secure shell
- (Note:  Windows users should have Ubuntu installed.)

### Step 1a:  We begin by going to our home directory (in terminal)
```bash
cd ~
pwd
```
>my example
```bash
cd ~
pwd
/Users/reshamashaikh
```

### Step 1b:  Go to `.ssh` directory
```bash
cd .ssh
```
>my example
```bash
pwd
/Users/reshamashaikh
cd .ssh
pwd
/Users/reshamashaikh/.ssh 
```

**Note:**  If you do not have the `.ssh` directory, you can create it
- if you are in your home directory:
	- `mkdir .ssh` 
- if you are not in your home directory:
	- `mkdir ~/.ssh`


### Step 1c: Generate `id_rsa` files if needed
- **Note:**  these `id_rsa` files contain a special password for your computer to be connect to network services (Ex:  GitHub, AWS).
- Check to see if these files exist by typing <kbd> `ls -alt`</kbd>
- If you do not have these two files (`id_rsa` and `id_rsa.pub`), create them by typing:  
	- <kbd> `ssh-keygen`</kbd>
	- Hit  <kbd> `enter`  </kbd> 3 times

>my example
```bash
% pwd 
/Users/reshamashaikh/.ssh
% ls
% ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/reshamashaikh/.ssh/id_rsa): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/reshamashaikh/.ssh/id_rsa.
Your public key has been saved in /Users/reshamashaikh/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:jmDJes1qOzDi8KynXLGQ098JMSRnbIyt0w7vSgEsr2E reshamashaikh@RESHAMAs-MacBook-Pro.local
The key's randomart image is:
+---[RSA 2048]----+
|   .=+           |
|.  .==           |
|.o  +o           |
|..+= oo          |
|.E.+X.  S        |
|+o=o=*oo.        |
|++.*o.+o.        |
|..*.oo           |
|o= o+o           |
+----[SHA256]-----+
% ls
total 16
-rw-------  1   1675 Dec 17 12:20 id_rsa
-rw-r--r--  1    422 Dec 17 12:20 id_rsa.pub
% 
```

## Step 2:  Copy `ssh` key to clipboard using `pbcopy` command
```bash
pbcopy < ~/.ssh/id_rsa
```

Verify the key has been copied to the clipboard by:  
```bash
pbpaste
```


## Step 3:  Connect `ssh` key to GitHub
- go to your [GitHub account](https://github.com/) (create one if you don't have one, and save your user name and password somewhere easily accessible for you.)
- click on your avatar/profile picture (upper right of screen)
- go to `Settings`
- on left of screen, select `SSH and GPG keys`
- Select <kbd> New SSH key </kbd>
- for "Title":  entitle it  "GitHub key"
- for "Key":  paste key from clipboard here
- click <kbd> Add SSH key </kbd>
- save, exit, confirm GitHub password as requested


---
## Step 4:  Configure user (on local computer)
### Configure user name and email (lets Git know who you are)
- `git config --global user.name "First Last"`  
- `git config --global user.email "myname@email.com"` 

To verify these additions, type:  
```bash
git config --list
```

---
### Step 5: Create Your Working Directory for Git Repos
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
