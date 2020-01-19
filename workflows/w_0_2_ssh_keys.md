# Workflow 0.2: SSH Setup 

### Purpose
With SSH authentication you don't need to enter your credentials (GitHub username and password each time you push a commit to the remote).   

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

## Mac & Windows Users
### Step 2 (for both Mac and Windows users):  Add `ssh` key to GitHub
- go to your [GitHub account](https://github.com/) (create one if you don't have one, and save your user name and password somewhere easily accessible for you.)
- click on your avatar/profile picture (upper right of screen)
- go to `Settings`
- on left of screen, select `SSH and GPG keys`
- Select <kbd> New SSH key </kbd>
- for "Title":  entitle it  "GitHub key"
- for "Key":  paste key from clipboard here
- click <kbd> Add SSH key </kbd>
- save, exit, confirm GitHub password as requested


