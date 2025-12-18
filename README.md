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








































