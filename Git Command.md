[Git E-Boot](https://git-scm.com/book/en "Link")

# [git commit]
1. Commit 簽名
   
   > $ git commit --amend
   
2. 修改最近一次的commit，修改後的commit hash會改變
   
   > $ git commit --signoff
   
# [git reset]
用於退回到某筆 commit 

1. 保留working tree，所有實體檔案不會異動。Cache directory local repository 一致。 
   
   >$ git reset --soft <commit id>
   
2. Work directory / Cache directory / Local repository 會被重置至某筆commit 內容。
   > $ git reset --hard <commit id>

4. 可搭配 **git reflog**，查詢所有branch上某個想回覆的commit id
5. 只有cache directory會被改變
   > $ git reset --mixed <commit id>

# [git log]
1. 查看最近n筆提交紀錄
   
   > $ git log --oneline -n
   
2. 查看所有訊息版本
   
   > $ git reflog
   
# [git apply]
Apply patch 

1. 只apply 沒有衝突的檔案，如果有衝突不會apply，並顯示有衝突的內容
   
   > $ git apply --reject <patch>
   
2. 檢查patch有沒有衝突，並不會apply
   
   > $ git apply --check <patch>

# [git format-patch]
Create patch

1. 從root到指定commit的patch
   
   > $ git format-patch --root
   
2. 最近n筆commit的patch
   
   > $ git format-patch -n

# [git rebase]
1. 將新branch(new) 挪到主branch(master)後
   
2. 修改某筆commit
   
   > $ git rebase -i  (列出commit 列表，找出要修改的commit，把pick改為edit)
   > $ git add <file>
   > $ git commit --amend
   > $ git rebase --continue
   
# [git branch]

1. 建立新branch
   
   > $ git branch <branch name> 
   
2. 刪除branch
   
   > $ git branch -d <branch name>
   
3. 根據tag 建立branch 
   
   > $ git branch <new branch> <tag>
   
4. 根據commit 建立branch 
   
   > $ git checkout -b <new branch> <commit id>

# [git merge]

# [git stash]
1. 將修改狀態暫存起來
   
   > $ git stash 
   >  
   > $ git stash -u (untrack檔案 需要 -u)

2. 查看stash紀錄，最新的stash，數字較小
   
   > $ git stash pop <stash @{#}>

3. 捨棄stash 紀錄
   
   > $ git stash drop  <stash @{#}>
   
# [git config]
git相關設定，git config --global 的操作會被寫入~/.gitconfig

1. 設定user name / user email，用來記錄專案版本由哪個開發者發佈，commit後無法修改
   
   > $ git config --global user.name  <user name>
   > $ git config --global user.email <user email>
   
2. 查看config
   
   > $ git config -l

# [git pull]
Align local repository to remote repository
> $ git pull <remote name> <branch name> --rebase


