###### tags:`Git`

# Git branch

## History
- Knowing add, commit and push to remote repository, we could see our operation history in the log
  
  ```{git}
  git log
  ```
  
- It is reasonable to return the older version file when we regret our commit.

## Switch Head
- Head is your status now. In normal situation, head follows your master of newest version.
  
  ![](https://i.imgur.com/FWRTlqA.png)

- change your head into the former version

  ```{git}
  git checkout <commit SHA-1>
  ```
  
  commit SHA-1 is the value behind the commit word.
  
- Now, the log becomes

  ![](https://i.imgur.com/WKBdIB4.png)

- return to master status
  
  ```{git}
  git checkout master
  ```
## Branch  

- master is the default name of git branch

- As usual, we create many branches to control many different version of your file.

### Develop New Function
- For example, if we want to test new function without making effect on files in the folder.
  
  First, we create a branch.
  
  ```{git}
  git branch <branch name>
  ```
  
  Second, we set to the branch
  
  ```{git}
  git checkout <new branch name>
  ```
  
  Third, add file and commit.
  
  ![](https://i.imgur.com/4f76Kk5.png)
  
  head follows branch cat instead of master.
  
  Branch upstream/master indicates your remote repository

### Confirm and Merge

- Now, you are satisfied with your new function and confirm it exert smoothly. You want your branch master could catch up your branch cat.

- Merge could make master the newest version. 
  
  Need to switch to branch master first.
  
  ```{git}
  git checkout master
  git merge <new branch name>
  ```
  
- Fast forward - head combines to the branch we have more committed so that master catches up the newest version.

### Fast forward error

- When we develop the new branch, the branch master continue to commit.
  ![](https://i.imgur.com/BAfSGuQ.png)

- This situation will increase a commit to merge the branch dev into the branch master. And, it doesn't call "fast-forward".

  ![](https://i.imgur.com/3hTs6SU.png)
 
- Once one file are edited in two branches, it results in conflict. There are two solutions. First, edit the file and commit again. Second, reverse to the former version.

### More practice 