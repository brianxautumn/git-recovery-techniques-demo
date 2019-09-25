# Fixing things in git

## Step 1 Identify how far you got!
![git](/git.png)

### You accidentally added files to staging
`git reset <filename>`
This will not undo your changes, it just removes them from staging area

### You want to get rid of your changes
`git reset --hard`

`git reset --hard HEAD`

This is for when you do not want to keep your changes, and want to go back to the last commit you were at.

### Reset specific files
`git checkout -- <filename>`  
`git checkout HEAD -- <filename>`  
This allows you to reset specific files back to the `HEAD`

### Reset all files 
`git checkout -- . (or directory)`  
`git checkout HEAD -- . (or directory)`  
This will allow you to checkout what an entire directory looked like at the given snapshot or hash. This is useful for going back to a specific commit and making it a new one. This is a good approach if the files have already been pushed.

### Revert a commit 
`git revert <commit id>` 
This will allow you to apply the opposite commit to undo something. If already pushed, this is a very good approach.
