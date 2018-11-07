# Workflow 1:  Make Update and Undo Changes

---

## Step 1:  create a repo (on GitHub)
- Click on `+` next to your profile picture
- Select `New Repository`
- Repository name:  `my_favorites`
- Description (optional):  `My Favorites`
- `Public` repos are free
- Check box for `Initialize this repository with a README` :white_check_mark: :heavy_exclamation_mark:
- Select green button `Create repository`

## Step 3: Let's "clone" (or copy) the repo from GitHub to our terminal

>my example  
```text
https://github.com/reshamas/my_favorites.git
```

## Step 4:  go to working directory (your local terminal)
Go to your working directory  
>my example
```bash
cd /Users/reshamashaikh/ds/gitsample
```


## Step 5:  clone the repo  
<kbd> git clone <url_name> </kbd> 
>my example
```bash
git clone https://github.com/reshamas/my_favorites.git
```
```bash
% git clone https://github.com/reshamas/my_favorites.git
Cloning into 'my_favorites'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done
```

## Step 6:  `cd` into the repo
<kbd> cd <repo_name> </kbd>
>my example
```bash
cd my_favorites
```

## Step 7:  create a file: fruit.txt
```txt
apple
banana
pear
```

## Step 8:  add the file
```bash
git add fruit.txt
```
