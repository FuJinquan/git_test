# git_test

### 目录
* [1.基本命令](#1)
* [2.本地同一个项目同时提交到github和gitlab上](#2)

<h4 id='1'>1.基本命令</h4>

* **git add**
* **git status (-s)**
* **git diff**
* **git commit**
* **git rm (-f)**  (强制删除)
* **git log (--pretty=oneline)**     (查看提交历史)
* **git remote**(列出远程服务器列表)
* **git remote add \<remoteGitName> <url>** (添加一个新的远程git仓库)
* **git mv (-f)**(重命名/删除文件)
* **git tag -a \<tag_name> -m \<commit message> <后期提交标签，加上指定的校验和(部分)就可以>**(添加标签注释信息) 
     git push \<remoteGitName> <tag_name>
* **git config --global alias.<别名> <基本命令>** (全局设置别名)
* **git branch**(添加/查看分支)
* **git checkout** (切换到所选分支)
* **git checkout -b \<newBranchName>**(合并上面两个命令)
* **git branch -d**(删除所选分支)

<h4 id='2'>2.本地同一个项目同时提交到github和gitlab上</h4>

* **git pull origin master --allow-unrelated-histories**
* **git pull --rebase origin master**(常用，pull过程中遇见产生冲突的文件时，先修改或者删除相应文件使冲突消弭，然后git rebase --continue,随后正常push)
* [参考博客](https://www.cnblogs.com/kungfupan/p/9967531.html)
>github和gitlab自动生成的README.md文件会产生conflict
>>` CONFLICT (add/add): Merge conflict in README.md
Auto-merging README.md
&#160;error: Failed to merge in the changes.
Patch failed at 0001 Initial commit
hint: Use 'git am --show-current-patch' to see the failed patch
Resolve all conflicts manually, mark them as resolved with
"git add/rm <conflicted_files>", then run "git rebase --continue".
You can instead skip this commit: run "git rebase --skip".
To abort and get back to the state before "git rebase", run "git rebase --abort".
fujinquan@fujinquandeMacBook-Pro test % git rebase --continue
README.md: needs merge
You must edit all merge conflicts and then
mark them as resolved using git add `