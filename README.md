# newiii
HOW TO USE GIT
Git & Github:

首先要有git
apt-get install git (Ubuntu)
yum install git-core (Centos)

在要git的目錄中
git init

git使用者設定
git config --global user.name 'orozco'
git config --global user.email 'orozco@hotmail.com'

公鑰匙先放去github:
cat ~/.ssh/id_rsa.pub

嘗試連github:
ssh -T git@github.com

git新增檔案
git add 檔案
git commit (-m "描述")
git更新檔案
git add .
git commit (-a 多行/-m一行'註記')

顯示git狀況
git status

上傳檔案:
先到檔案所在目錄
cd 檔案所在目錄
git commit 要傳的檔案
git remote add origin git@github.com:自己的帳號/repo名稱.git
git push -u origin master

下載repo
建立檔案要放的目錄
cd 到該目錄
git clone https://github.com/帳號/repo.git

如果無法PUSH上去到REPOSITORY, 要先PULL下來做MERGE, 再PUSH上去
git pull origin master
git push -u origin master

如果在PULL下來時,出現fatal: refusing to merge unrelated histories, 必須加入--allow-unrelated-histories
git pull origin master --allow-unrelated-histories
git push -u origin master

檢查git remote
git remote -v

刪除origin
git remote rm origin

