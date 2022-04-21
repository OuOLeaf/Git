###### tags:`Git`

# Git Command

## Set your email and user name

- Why do we leave our personal information

  because it needs to record who have done this update.
  
  Other people could know the former change caused by you.
  ```{git}
  git config --global user.name "your name"
  git config --global user.email "your email"
  ```
- watch what you have done
  ```{git}
  git config --list
  ```
  ![](https://i.imgur.com/UMkXpWc.png)


### init

- We use repository to manage your file in the specified folder and create a repository in your computer is called "local repository"
  
- you should first switch to the folder you want to set to local repository in cmd. 
  ```{git}
  git init
  ```
  
### add

- why we add file?
  
  Before we use add command, Git can defect your file but not track it.
  
  These files are called untracked.
  
  Add file to the staging area and track status
  
  ```{git}
  git add files
  
  git add . (or --all)
  ```
  
- Both new file or modified file would be tracked after input add command.

### status

- watch git status whether the file is untracked or track now.

  ```{git}
  git status
  ```
### commit 
- commit file
  
  Now, our files are under tracking.
  
  We will see the "changes to commit" on the screen
  
  Then use commit to confirm a new version.
  
  This status of files are ready to upload to github.
  
  ```{git}
  git commit -m ''
  ```

### remote

- This section could push data of the local repository to remote one like Github.

- set the remote repository variable
  
  ```{git}
  git remote add <var> <url>
  ```

- watch remote variable

  ```{git}
  git remote  #(only var. name)
  git remove -v  #(var. name and path)
  ```


### clone
- In github, path are seen in "Code" combo box.

  ![](https://i.imgur.com/GpEet0E.png)
  
- pull data from remote repository
  
  switch to your folder and
  
  ```{git}
  git clone <remote repository path>
  ```

### push
- push your data to remote repository
  
  ```{git}
  git push -u <remote var> master:<branch name>
  ```
- push master files to cat branch of github respository
  
  create another branch
  
  and set the repository to the default repository for next use.

### pull

- update data from the remote repository
  
  ```{git}
  git pull <var> <branch>
  git pull
  ```  
- Use this when other people change your file and you need to update yours.
### log

- see log about what you did in details
    
  ```{git}
  git log
  ```
### clean
- watch the files that don't exist in tracking status
  
  ```{git}
  git clean -n
  ```
  
- delete your new files you create after committing
  ```{git}
  git clean -f
  ```

### checkout

- back to your former commit status
  
  ```{git}
  git checkout <specified file>
  git checkout . # all files
  ```

### reset

- back to unstaged status for staged file
  
  ```{git}
  git reset HEAD
  ```

- return two former committed status of your git. You will go to the k - 2 version file.
  ```{git}
  git reset head^^ (=git reset head~~ = git reset head^2)
  git reset head^^ --hard # remove all files don't exist in k-2 version.
  ```
## delete remote variable
- watch remote setting
  ```{git}
  git remote -v
  ```
- delete the lines about remote variable

  ```{git}
  git config -e
  ```
- leave config setting: find the below line of command and text :q in the next line.
  



  
 
  
  

