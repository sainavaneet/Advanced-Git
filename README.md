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

```

git stash pop 

```



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
### We can also publish stash as a new branch 
```

git stash branch features/stashed-files stash@{0}


```





































<<<<<<< HEAD
=======
>>>>>>> Stashed changes
>>>>>>> ef17987 (Trying to get the changes from main branch to features/notes branch)
