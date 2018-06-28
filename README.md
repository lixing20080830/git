# git和github的相关操作

GitHub上README.md排版样式教程
-----
参考资料：https://blog.csdn.net/u012067966/article/details/50736647

解决github打开速度慢的问题，好像没什么效果。
------
修改hosts（HOSTS文件路径：C:\Windows\System32\drivers\etc\hosts）

1.打开Dns检测|Dns查询 - 站长工具
2.在检测输入栏中输入http://github.com官网
3.把检测列表里的TTL值最小的IP输入到hosts里，并对应写上github官网域名。
例如：
192.30.255.112 github.com
192.30.255.113 www.github.com
192.30.255.120 nodeload.github.com
参考资料：https://www.cnblogs.com/yangzhou33/p/8407385.html<br>

git图片显示操作
------
我从网页上点击打开图片的路径:<br>
https://github.com/lixing20080830/BCC/blob/master/images-folder/environment.png<br>
那么添加链接的方式如下:<br>
![image]开头，后面跟着(https://github.com/lixing20080830/BCC/raw/master/images-folder/environment.png)<br>
将点击打开图片的路径中的blob修改为raw即可<br>

git命令
------
git init //把这个目录变成Git可以管理的仓库<br>

git add README.md //文件添加到仓库<br>

git add . //不但可以跟单一文件，还可以跟通配符，更可以跟目录。一个点就把当前目录下所有未追踪的文件全部add了<br>

git commit -m "first commit" //把文件提交到仓库<br>

git remote rm origin //删除链接<br>

git remote add origin https://github.com/lixing20080830/dubbodemo.git  //关联远程仓库<br>

git pull origin master // 把本地仓库的变化连接到远程仓库主分支<br>
 
git push -u origin master -f //把本地库的所有内容强行推送到远程库上<br>

git push -u origin master //把本地库的所有内容推送到远程库上<br>

git status //查看整体变更（详细到文件名）<br>

git log //查看历史记录<br>

git clone https://github.com/lixing20080830/zookeeper-learning-notes.git  //从远程库克隆到本地库<br>

git push 每次都需要输入用户名和密码是因为你采用的是 https 方式提交代码，如果采用的是 ssh 方式只需要在版本库中添加用户的
rsa 的key就可以实现提交时无需输入用户名和密码。设置后之后可以用下面方式复制和链接<br>
 
git clone git@github.com:lixing20080830/dubbodemo.git<br>

git remote add origin git@github.com:lixing20080830/dubbodemo.git<br>
 
git 解决fatal: Not a git repository<br>
 
https://blog.csdn.net/u012306714/article/details/52571596<br>
