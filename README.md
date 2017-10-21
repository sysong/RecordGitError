# RecordGitError
#使用
1.本地创建文件夹
2.初始化git init
3.使用远程指令git remote add origin git@github.com:sysong/RecordGitError.git
关联
4.本地文件添加完成之后，使用git add README.md 本地库更新
5.git commit -m "first commit" 增加提交文件说明
6.git push -u origin master同步数据


#问题1
提示Permission denied (publickey).
#解决方案
1.重新创建ssh key 	终端指令：	ssh-keygen 
yunsongdeMacBook-Pro:RecordGitError suys$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/suys/.ssh/id_rsa): 
2.打开这个文件vim /Users/suys/.ssh/id_rsa，把里面的所有的内容都拷贝到你的github网站的ssh key里
3.在github的右上角edit your profile 里找到ssh key，然后add ssh key

#问题2
src refspec master does not match any.
#解决方案
引起该错误的原因是，目录中没有文件，空目录是不能提交上去的
touch README
git add README 
git commit -m 'first commit'
git push origin master






