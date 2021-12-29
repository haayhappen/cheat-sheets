## Git

### Basics
Init local repo   
```git init <directory> ```

Clone remote repo   
```git clone <repo>```

Stage (specific) files    
```git add <directory>``` or ```git add .``` to add all

Commit with a message   
```git commit -m "<message>"```
```git commit --amend```

Shows staged, unstaged & untracked changes    
```git status```

Display commit history    
```git log```

Rebase onto commit, tag or branch   
```git rebase <base>```

### Branches

List all branches   
```git branch```

Create branch and checkout <branch>   
```git checkout -b <branch>```
  
Merge <branch> into current branch    
```git merge <branch>```
  
Fetch (all) remote refs   
```git fetch (<remote> <branch>)```
  
Pull remote copy of current branch and merge it directly    
```git pull```
  
  
### Specifics

Set author name for all commits in a specific repo    
  ```git config user.name <name>```
  
Edit the global git config in an editor   
  ```git config --global --edit```
  
Reset changes (optional with working dir) to the most recent commit   
```git reset (--hard)```
  
Reset to a specific commit    
  ```git reset (--hard) <commit>```
  
Interactive rebase current branch onto <base>   
  ```git rebase -i <base>```
