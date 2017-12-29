this is a readme.txt file


Git pull 强制覆盖本地文件
	git fetch --all  
	git reset --hard origin/master 
	git pull
参考：https://ruby-china.org/topics/2494



Git强制覆盖master分支 	
http://blog.csdn.net/CrazyZhang1990/article/details/77978722
原创 2017年09月14日 11:54:40

一、操作步骤

1.1 git push origin develop:master -f
把本地的 develop 分支强制(-f)推送到远程 master
但是上面操作，本地的 master 分支还是旧的，通常来说应该在本地做好修改再去 push 到远端，所以我推荐如下操作

1.2  git checkout master 
切换到旧的分支

1.3 git reset --hard develop  
 将本地的旧分支 master 重置成 develop

1.4 git push origin master --force 
 再推送到远程仓库
