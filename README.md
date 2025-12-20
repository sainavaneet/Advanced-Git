# My repository


```bash


git init

git add . # git add (specific file)

git commit -m "Initial Commit"

git push -u origin main # Branch name :)


git status # To check the status of the git repo

```




### create a new branch 



```bash

git branch -m master main


git push -u origin main 



```

Ok lets say we created and made changes in the branch if we ever `-m or -u` before commiting or pushing to the remote

we dont need to use `-u or -m` always we can directly use `git push/commit origin main`




```

# Lets say if we want to delet the branch that we created before 


## first lets change the default branch from master -) main then

git push orgin --delete master



```



### verify the git branch



```
git branch 

git status


## the output will look like this 

On branch main
Your branch is up to date with 'origin/main'.

```


## Now i want to create a new branch with checkout 

	This is basically we do because we directly checkout to that particulary branch without doing `git checkout {branch name}`

```

git checkout -b features/notes

# edit some files here 

git add . 


git commit -m "updated"


git push origin -u features/notes

```


## To See the list of branches that are available in local and remote 


```
git branch -a

```

## We can Delet branches 

```

git branch -D [branch name ] # this is for the branches that are not fully published or fully merged

git branch -d [branch name ] this is for the general purpouse ( we can delete any branch like this)

```


## Stash 

stash is used to save changes temporory so that we can use them again or save them in any branch we wanted

- stash is default only for the tracked files "basically commited or git added files"


- Before pushing into the remote ( we can just stash them and then save them any where we wanted)

main command is 
```

git stash 


```
TO save the stashed files to the repo 


- when we do this it will disappear from the stash history 
```

git stash pop 

```
if we want to apply insted of pop the stash we can just use `git stash apply`



To make available in the stash history we use `git stash apply` insted of `pop`


OR 

We can apply particular stash history by using `git stash apply stash@{0}`



### Stash untracked files or not commited files

```

git stash -a

```


### Check the stashed list

```

git stash list



# The output will be like this 

stash@{0}: On features/notes :WIP: README update

```
if we want to apply particular stash we can use `git stash apply stash@{0}`


### We can also publish stash as a new branch 

```

git stash branch features/stashed-files stash@{0}


```


# Cherry-Pick 


So this is basically we can take specific commit from other branches and can modify into the current branch 

```
git cherry-pick [hash id] # hash id can be available by git log --oneline

```

Now lets say we cherry-pick it 

and then 
```
git add . 

git push origin -u main 


```


# Revert changes

first lets check what all the changes that i had been to the current branch

by using `git log --oneline`

```
git reset --hard origin/main

```

basically this brings the repo to one commit previously so what ever we had done the changes it will be gone 



# Git `Tags`


Tags are basically to add versions for branch 


we can create a tag by using 

```

git tag -a v1.0 -m "Version 1"

```

## We can Check all the git tags


```

git tag

```

# Git Merge


Merge is basically that merges all the commits from the other branch to the current branch were ever we wanted the merge to be 


```
git merge {main} # this will bring all the commits from the main branch to the current branch that we are working on

```

### Merge conflicts 


If we get any merge conflicts we need to manulally remove thoes confilct markers and edit them 

the important thing is we need to add thoes files again by using `git add` otherwise the merge doesn't work.




# Git rebase 


Git rebase is basically used to rebase the entire commits from one branch to another branch

lets say if we are working on different branch and want to get all the changes from the current branch to the main branch we basiclly do :

```
git rebase {main} # if we want our currrent changes to come to the main branch then we need to do this 

```

If there are any conflicts during the rebase we need to solve them manully and then add them again `git add`

then if we can't push them to the git hub we should use `git push --force-with-lease`
