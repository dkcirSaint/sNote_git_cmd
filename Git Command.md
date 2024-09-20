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
>  $ git reset --hard <commit id>
4. 可搭配==git reflog==，查詢所有branch上某個想回覆的commit id
5. 只有cache directory會被改變
>  $ git reset --mixed <commit id>

# [git log]
1. 查看最近n筆提交紀錄
   
   > $ git log --oneline -n
   > 
2. 查看所有訊息版本
   
   > $ git reflog
   
# [git apply]
# [git format-patch]
# [git rebase]
# [git branch]
# [git merge]
# [git stash]
# [git config]
# [git pull]