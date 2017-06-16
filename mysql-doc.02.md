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
      4. 在此目录下创建一个文件(touch demo),编辑此文件（vim demo）,看一下目录下文件的状态（git status）,显示信息如：
        
         把文件加到仓库中去, 只有加到仓库中了, 才可能看一下文件的变化，加到仓库的命令：git add demo，加入后查看的状态信息如：
         
         查看完后进行提交，
init file

new file

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# On branch master
#
# Initial commit
#
# Changes to be committed:
#       new file:   demo.c


         
