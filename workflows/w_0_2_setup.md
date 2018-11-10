
# Workflow 0.2: Setup

#### This is your checklist:
- [ ] Set up `ssh` keys
- [ ] Add `ssh` key to GitHub
- [ ] Configure user
- [ ] Set up working directory

## Mac Users

### Step 1:  Setup `ssh` keys (generate a key pair)
- ssh = secure shell

#### Step 1a:  We begin by going to our home directory (in terminal)
<kbd> cd ~ </kbd>  
<kbd> pwd </kbd>

>my example
```bash
cd ~
pwd
/Users/reshamashaikh
```

#### Step 1b:  Go to `.ssh` directory
<kbd> cd .ssh </kbd>  

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
	- <kbd> mkdir .ssh </kbd>  
- if you are not in your home directory:
	- <kbd> mkdir ~/.ssh </kbd>  


#### Step 1c: Generate `id_rsa` keypair files if needed
- **Note:**  these `id_rsa` files contain a special password for your computer to be connect to network services (Ex:  GitHub, AWS).
- Check to see if these files exist by typing <kbd> ls -alt</kbd>
- If you do not have these two files (`id_rsa` and `id_rsa.pub`), create them by typing:  
	- <kbd> ssh-keygen</kbd>
	- Hit  <kbd> enter  </kbd> **3 times**

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

#### Step 1d: Copy `ssh` key to clipboard using `pbcopy` command
<kbd> pbcopy < ~/.ssh/id_rsa.pub </kbd>  

Verify the key has been copied to the clipboard by printing the contents at your terminal:  
<kbd> pbpaste </kbd>  

## Windows Users
### Step 1:  [How to Create SSH Keys with PuTTY on Windows](https://www.digitalocean.com/docs/droplets/how-to/add-ssh-keys/create-with-putty/)


---
## Step 2:  Add `ssh` key to GitHub
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
## Step 3:  Configure user (on local computer)
### Configure user name and email (lets Git know who you are)
<kbd> git config --global user.name "First Last"  </kbd>  
<kbd> git config --global user.email "myname@email.com"  </kbd>  

To verify these additions, type:  
<kbd> git config --list  </kbd>  

### Configure (terminal) editor of choice
<kbd> git config --global core.editor "nano -w"  </kbd> 

Other editor options can be found in [Setting Up Git](http://swcarpentry.github.io/git-novice/02-setup/)

---
## Step 4: Create Your Working Directory for Git Repos
Navigate to your home directory where you want to create a directory for the git work.   
<kbd> cd ~ </kbd>  

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
