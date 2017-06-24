># Github 的使用
  ## 添加远程仓库  
 1.如果我们现在本地有一个git仓库, 我们使用remote add 命令将它添加到远程的仓库中,命令如下：     
   git remote add origin https://github.com/liuwen777/stu.git。  
 2.需要将远程的仓库的信息更步到本地，命令如下：git fetch origin。 
  ！[添加仓库](https://github.com/liuwen777/liuyunwen/blob/master/img/%E6%B7%BB%E5%8A%A0%E4%BB%93%E5%BA%93.png)
 
 ## 同步master分支 
   如果我们本地的仓库进行开发, 交进行提交commit. 那么我们本地的仓库和远程的仓库就不能保持同步了.那么我们需要把本地的这次提交也要反映在远程的仓库上. 那    么  我们就需要使用push命令.  $ git push origin master   
 ## 从远程仓库同步 
     clone  
    当我们知道git仓库的地址了(在github上有很多的开源仓库.), 就可以使用下面的命令将源码拉取到本地:$ git clone url   

 ## 拉取源码  
  我们已经拉取源码到本地了, 但是服务器上的git已经更新了, 当我们需要将服务器的源码与本地源友进行同步进时, 需要使用下面的命令：$ git pull
  ！[pull命令](https://github.com/liuwen777/liuyunwen/blob/master/img/pull%20%E5%91%BD%E4%BB%A4.png)

