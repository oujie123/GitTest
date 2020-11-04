# GitTest
1. git config core.ignorecase false 关闭忽略大小写
2. git config --list       查看全局配置



ignore文件：https://github.com/github/gitignore



3.在缓存区的文件回到工作区：   git reset HEAD 文件名

4.将文件修改内容在源文件中删除： git checkout -- 文件名



5.创建分支：git checkout -b dev -t origin/master

6.查看分支状态图形化：gitk&

7.修改分支名字：git branch -m dev dev_new

8.删除分支：git branch -D dev_new 

9.变基：git pull --rebase (可能会涉及到很多次合并冲突)

10.提交其他分支代码到远端：git push origin dev:master

11.回滚分支：git revert 远端的hash值  然后git push origin dev:master   远端也没有了



12.提交后发现一个BUG，不知道哪里出现的，先回滚到某一个点：git reset --hard 分支hash值   

​      如果发现没问题，就用git pull -rebase 回到刚刚的分支，重新找一个点reset



13.git merge 分支名    合并某个分支到当前分支

14.git checkout --conflict=diff3 发生冲突的文件名    显示自己的代码和别人的代码哪里冲突了

​      git checkout --ours 文件名    解决冲突全部接受我自己的代码