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
         
         查看完后进行提交，(git commit),输入完后回车会进入到一个页面，可以输入此次修改的名字和操作的内容。
配置用户信息

配置用户名, 这个用户名是你的提交patch的名子,

$ git config --global user.name
1
配置用户邮箱, 这个邮箱最好写你最常用的邮箱, 说不定会有人给你写邮件的, 这个是可能来自世界的任何角落, 可能是任何肤色和眼睛.

$ git config --global user.email
1
配置编辑提交信息的编辑器, 我们熟悉的编辑器是vim. 使用这个去编辑提交信息, 最好把每一次提交信息填写写的全面, 不是为了给别人看, 万一那天自己想回顾一下. 也需要详细的信息.

$ git config --global core.editor vim
1
查看提交信息
我现在把仓库里的README这个文件给删除了. 然后再使用ls命令查看文件, 看看这个文件是否还存在.
版本回退

什么叫版本, 一次提交就相当于一个版本. 如果更准确的说是提交的回退. 每一次提交都会将修改的状态提交到仓库中保存着, 这些信息都保存那里呢?都保存在.git的目录下.

如果想回退到上次提交的版本, 那么需要使用git reset命令.

$ git reset --hard commitID
1
注意: 使用这个命令后,再使用git log命令不会查看到所有log的相关信息, 那么我们没有办法获取到后一个提交的CommitID.

$ git log
1
在这里我们需要使用git reflog命令查看后一次提交的CommitID, 如果已经有了后一次提交的CommitID, 那么我们需要使用git reset命令恢复到前面提交版本.

$ git reflog
1
从仓库中删除文件

如果将文件从仓库中删除这个文件, 需要使用git rm.

$ git rm filename
1
这只是做了删除操作, 但没有真正的从仓库中删除, 我们只要将删除再做一次提交到仓库.

$ git commit
1
从版本库中忽略文件

如果在我们的仓库目录里会产生三方的临时垃圾文件或是

$ touch .gitignore

版本之间对比

$ git diff

$ git diff commitID1 commitID2

什么是patch

patch多指补丁的意思, 在这里更多的指程序有一些bug, 需要我们进行fixed, 那fixed源码文件就是patch.

patch实际上是保存两个文件的差异.

git生成patch

$ git format-patch -p1
1
git 打patch

$ git am patch-name
1




$ rm README
$ ls
$ ls -al
123
文件已经被删除了, 这是我们使用linux基本命令去查看文件是不是还存在这个目录中.现在我们使用git去查看一下现在仓库是什么状态

$ git status
1
发现这个文件是误删了, 我们想把它恢复回来, 现在我们有办法吗? 如果没有将这个文件提交到仓库里, 我们是没有办法将它恢复的.

$ git checkout README
1
然后我们再用ls查看一下文件是否存在.

$ ls -al
1
再查看git仓库是状态

$ git status
1
说明, 只要将文件提交到git仓库中



         
