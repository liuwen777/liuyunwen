># Git 相关内容
>>## Git 的介绍和安装
 >>>### Git 的介绍  
 
      1.版本控制（Revision control）是维护工程蓝图的标准作法，能追踪工程蓝图从诞生一直到定案的过程。
      2.版本控制也是一种软件工程技巧，借此能在软件开发的过程中，确保由不同人所编辑的同一代码文件案都得到同步。  
      
 >>>### Git 的安装
      1.安装命令：$ sudo apt-get install git。  
      
>>## Git 的基本命令  
 
 >>>### 创建版本库  
      
   1. 新建一个目录：mkdir file；
   2. 切换到此目录下，将目录创建成 Git 仓库：git init；
   3. 在此目录下，用ls -al 命令可看到有 .git 的隐藏文件，则可知道仓库创建成功；
   4. 在此目录下创建一个文件(touch demo),编辑此文件（vim demo）,看一下目录下文件的状态（git status       
      把文件加到仓库中去, 只有加到仓库中了, 才可能看一下文件的变化，加到仓库的命令：git add demo，加入后
      可查看状态 
   5.查看完后进行提交，(git commit),输入完后回车会进入到一个页面，可以输入此次修改的名字和操作的内容。 
     然后再次查看状态（git status），两次查看的结果是不一样的。
         
       
 >>>### 配置用户信息  
      
   1.git config --global user.name:配置用户名, 这个用户名是你的提交patch的名子。       
   2.git config --global user.email：配置用户邮箱。         
   3.git config --global core.editor vim：配置编辑提交信息的编辑器, 我们熟悉的编辑器是vim. 使用这个去编辑提交信息,  
     最好把每一次提交信息填写的全面。  
   4.git log：此命令可以查看一下我们提交的信息。      
 >>>### 恢复删除的文件  
    1.rm file：删除文件命令，然后用 ls 查看该文件是否存在。       
    2.git status：查看删除文件后仓库的状态。        
    3.git checkout file：恢复文件，注意：没有将这个文件提交到仓库里, 我们是没有办法将它恢复的。       
    4.git status：恢复后再次查看仓库的状态。        
 >>>### 版本回退  

   1.概念：什么叫版本, 一次提交就相当于一个版本. 如果更准确的说是提交的回退. 每一次提交都会将修改的状态提交到仓库中保存着, 这些信息都保存那里呢?都保存在.git的目录下。       
    2.git reset --hard commitID：回退到上次提交的版本的命令。注意：使用这个命令后,再使用git log命令不会查看到所有log的相关信息，但可以用下面的命令查看信息。提示信息如：        
    3.git reflog：查看后一次提交的CommitID       
      
 >>>### 从仓库中删除文件
    1.git rm filename：进行删除操作，但是并没有真正从仓库中删除。       
    2.git commit：提交后真正将文件从仓库中删除。 
      
 >>>### 从版本库中忽略文件
    1.touch .gitignore:此命令可以将在我们的仓库目录里产生的三方的临时垃圾文件存放起来。
      
 >>>### 版本对比
    1.git diff commitID1 commitID2:对比的命令。
      
 >>>### patch 相关内容
    1.概念：patch多指补丁的意思, 在这里更多的指程序有一些bug, 需要我们进行fixed, 那fixed源码文件就是patch，patch实际上是保存两个文件的差异。
    2.git format-patch -p1：生成patch 的命令，1代表的是数字，可以随意更改。       
    3.git am patch-name：git 打patch。  
      
     
 
 

 
 


 
 
 
 
 
 


 

 
 
 



 

 

 



         
