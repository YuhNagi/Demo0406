
Today id 2017/04/07.
------------------------------

 git多人协作简单流程


合作项目：

1.若是别人的项目先fork.

2.克隆到本地，并创建远程关联仓库。
 
   git clone SSH链接

   git remote add origin git@github.com:用户名/仓库名.git

3.最好是在本地新建个分支用于开发，如dev
 
    git checkout -b dev
  
4.在新分支下修改完成后，保存并提交，再切回master分支
 
    git add .  =>git commit -m '描述信息'

    或者： git commit -am '描述信息'
  
    git checkout master
  
5.在master分支下，把dev合并到master下，并删除dev分支。
 
    git merge dev
  
    git branch -d dev
  
6.最后是激动人心的推送到远程了，可在这之前，要先拉取下最新代码，看是否有别人修改了。
 
    git fetch origin master  拉取

    git merge origin/master  合并，有冲突就解决冲突
  
    git push origin master  最后推送
  
7.如果是别人的项目，不要忘记提Pull Request
  

