# Github使用笔记
---
>https://zhuanlan.zhihu.com/p/28062574

**Add** files to **Repository**

1. **Clone**

  复制**Clone or download**下的URL

  > $ git clone [URL]

2. 将要上传的文件复制**Clone**得到的文件夹中

3. **cd**到该文件夹中

4. **上传文件**

  > $ git add . (添加文件)   
  $ git commit -m "提交信息"   
  $ git push -u origin master




  **Delete** files
  > https://blog.csdn.net/Jarvenman/article/details/78835851

1. **Pull**
> $ git pull origin master

  将远程repository中的项目拉下来
2. 查看文件目录
> $ dir

3. **Delete**
> $ git rm -r cached [file's name]  
$ git commit -m "删除信息"  
$ git push -u origin master
4. **Update**
>在本地修改文件  
使用**add**方法添加到github
5. **errors**

> **$ git push -u origin master**  
To https://github.com/Demokun/hello-world.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/Demokun/hello-world.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

  解决方法：
  > $ git pull origin master    
  $ git push -u origin master
