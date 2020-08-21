# git_test
git命令测试用
## 1.基本命令
* git add
* git status (-s)
* git diff
* git commit 
* git rm (-f)  (强制删除)
* git log (--pretty=oneline)     (查看提交历史)
* git remote(列出远程服务器列表)
* git remote add \<remoteGitName> <url> (添加一个新的远程git仓库)
* git mv (-f)(重命名/删除文件)
* git tag -a \<tag_name> -m \<commit message> <后期提交标签，加上指定的校验和(部分)就可以>(添加标签注释信息) 
     git push \<remoteGitName> <tag_name>
* git config --global alias.<别名> <基本命令> (全局设置别名)
* gitlab使用
* git branch(添加/查看分支)
* git checkout (切换到所选分支)
* git checkout -b \<newBranchName>(合并上面两个命令)
* git branch -d(删除所选分支)
## 2.本地同一个项目同时提交到github和gitlab上
* git pull origin master --allow-unrelated-histories