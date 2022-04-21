###### tags:`Git`
# 更新 Github 上文件

- github 點 code 可看到連接網址
  ![](https://i.imgur.com/GpEet0E.png)

- 連接到 github 的 Repository 使用
    ```{git}
    git remote add upstream https://github.com/.../test.git
    ```
    upstream is the name you define
- 會出現錯誤 fatal: Not a git repository (or any of the parent directories): .git
  
  因為沒有初始化資料夾 要有 git 檔在裡面 先
  
  ```{git}
  git init
  ```
  
- sync：update file 

- examine your remote path
  
  ```{git}
  git push -u <var> master
  ```

- add file to stage
  
  why we add file?
  
  Before we use add command, Git can defect your file but not track it.
  
  These files are called untracked.
  
  Add file to track status
  ```{git}
  git add files(--all)
  ```
  
- commit file
  
  Now, our files are under tracking.
  
  We will see the "changes to commit" on the screen
  
  Then use commit to confirm a new version.
  
  This status of files are ready to upload to github.
  
  ```{git}
  git commit -m 'version detail'
  ```
  
- push file to github
  
  ```{git}
  git push upstream master
  ```