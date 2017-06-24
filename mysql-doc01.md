># 第一天
>>## linux历史、组成和安装  

   >>>- 1.Linux操作系统由Linux内核，一些GNU程序库和工具，命令行shell，图形界面的X Window系统和相应的桌面环境组成。
   >>>- 2.Shell俗称壳，是指“提供使用者使用界面”的软件。它接收用户命令，然后调用相应的应用程序。
    
>>## linux的基本命令(基本文件和目录的操作)  

>>### 文件操作
   >>>- 1.touch  file：新建文件（相当于文档，可以直接用vim编辑）
   >>>- 2.cp file file1：同一目录下复制文件，结果是将 file 文件的内容复制到 file1 中，此时会覆盖原来 file1 中的内容
   >>>- 3.cp file  /home/linux/file1-：不同目录下复制文件，可指明路径
   >>>- 4.mv file   file2：同一目录下移动文件内容，将 file 中的内容复制到  file2 中，并且会将 file 这个文件自动删除
   >>>- 5.mv file  /home/linux/：同一目录下移动文件内容
   >>>- 6.ls -al  ：显示所有的文件或者目录，包括隐藏文件
   >>>- 7.cat  file：读取文件内容mkdir dir
>>### 目录操作
   >>>- 1.mkdir dir：新建一个目录
   >>>- 2.cp dir   dir1  -a：将 dir 目录下的文件复制到 dir1 中
   >>>- 3.mv dir  dir2：-将 dir 移动到 dir2 中
   >>>- 4.rm  dir  -rf：强制删除目录 dir 
   >>>- 5.ls -d  dir：若 dir 目录下有文件，则不能用此命令将删除，可以用上一个命令删除
   >>>- 6.find  ./dir  -name  "filename"：查找文件
   
>>### 文档归档和压缩
   >>>- 1.使用gzip和gunzip对文件进行压缩和解压缩           
   2.使用bzip2和bunzip2对文件进行压缩和解压缩          
   3.使用tar对文件和目录进行压缩和解压缩   
   4.举例如下：    
        gzip  filename          
        bzip2  filename         
        gunzip filename         
        bunzip2  filename         
        tar czvf  file.tar.gz dir
        tar cjvf  file.tar.bz2 dir
        tar cJvf  file.tar.xz  dir
        tar xvf  file.tar.gz
        tar xvf  file.tar.xz
   
   

  
 
 

 


 
   



