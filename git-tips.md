git fetch后，查看其他人员的修改记录
git difftool origin
之后可以进入图形化的 对比界面

<<<<<<< HEAD


=======
>>>>>>> a89e834c9b8812b7dcc97412e9f4e4598c74c5de
注：我事先在github上建好了文件夹，安装好git后，在本地项目所在的目录，新建一个 git bash
1 git init()  //初始化本地库
2.git add .   //使用命令 git add .添加到暂存区里面去，不要忘记后面的小数点“.”，意为添加文件夹下的所有文件
3.git commit -m '注释‘  //用命令 git commit告诉Git，把文件提交到仓库。引号内为提交说明
4.git remote add origin 远程库的地址   //关联到远程库
5.git  pull --rebase origin master   //获取远程库与本地同步合并（如果远程库不为空必须做这一步，否则后面的提交会失败）
6.git push -u origin master   //把本地库的内容推送到远程，使用 git push命令，实际上是把当前分支master推送到远程。执行此命令后会要求输入用户名、密码，验证通过后即开始上传。
出错：此时很多人会尝试下面的命令把当前分支代码上传到master分支上。$ git push -u origin master。但依然没能解决问题
错误解析：出现错误的主要原因是github中的README.md文件不在本地代码目录中。可以通过如下命令进行代码合并【注：pull=fetch+merge]
git pull --rebase origin master
7.此时再执行语句 git push -u origin master即可完成代码上传到github

git rebase --abort 退出rebase 状态
git fetch --all 获取所有远程端
git reset --hard origin/master 回退到远程master最新版本
git pull 更新最新代码

