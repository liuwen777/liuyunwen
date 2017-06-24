# CGI 编程  

 ## 安装相关软件
      1.Apache安装
           1)	根目录执行命令：sudo apt-get update          
           2)	根目录执行命令：sudo apt-get install tasksel          
           3)	根目录执行命令：sudo tasksel     
        2	Apache开启CGI  
         1)	在apache中开启cgi支持，执行命令：  
              Sudo ln -s /etc/apache2/mods-available/  
              cgi.load /etc/apache2/mods-enabled/cgi.load  
         2)	重启 apache 服务器，执行命令：service apache2 restart  
         3)	需要运行的cgi文件的存放路径，执行命令：sudo /usr/lib/cgi-bin  
         4)	修改目录权限  
              执行命令：sudo mkdir /usr/lib/cgi-bin/sx  
              执行命令：sudo chmod 777 /usr/lib/cgi-bin/sx  
        3	 安装MySQL的C语言库  
          切换到根目录，更新源，执行命令：sudo apt-get update  
          进行安装，执行命令：sudo apt-get install libmysqlclient-dev    
         4	atom及其插件的安装  
         1)	安装atom，执行命令：sudo dpkg -i atom-amd64.deb  
   
   ## CGI 的概念  
        CGI(Common Gateway Interface) 是WWW技术中最重要的技术之一，有着不可替代的重要地位。    
        CGI是外部应用程序（CGI程序）与WEB服务器之间的接口标准，是在CGI程序和Web服务器之间传递信息的过程。  
         
    ## CGI 的基本函数  
        1)	获取表单数据：  
              cgiFormResultType cgiFormString(char *name, char *result, int max);  
              参数：name, 指定要获取的表单项的名字  
              result,将获得的数据存储到result中  
              max， 指定最多读取的字符个数  
              举例：cgiFormString("name", result,  16);可以获得最多16个字符并且保存于result中  
        2)	int fprintf(FILE *stream, const char *format, ...);  
            功能： 将格式化的语句输出到指定的流  
            fprintf(stdin, "helloworld\n") 等价于 printf("helloworld\n);  
        3)	转换函数  
             int atoi(const char *nptr);//功能：将一个字符串转换成对应的数字，比如：“1234” ==》 1234  
        4)	MYSQL *mysql_init(MYSQL *mysql)  
             功能：初始化函数，参数为NULL即可，接收返回值。失败，NULL  
        5)	MYSQL *mysql_real_connect(MYSQL *mysql, const char *host, const char *user, const char *passwd, const char *db,                    unsigned int port, const char *unix_socket, unsigned long client_flag)   
             功能：连接mysql服务器,失败，NULL   
        6)	 void mysql_close(MYSQL *mysql)  
             功能：关闭服务器连接  
        7)	int mysql_real_query(MYSQL *mysql, const char *stmt_str, unsigned long length)  
             功能：执行sql语句，sql语句不能以“；”结尾  
             成功，0,失败， 非0  
        8)	int mysql_query(MYSQL *mysql, const char *stmt_str)  
             功能：执行sql语句，sql语句不能以“；”结尾  
        9)	void mysql_free_result(MYSQL_RES *result)  
              功能：释放空间  
       10)	MYSQL_RES *mysql_store_result(MYSQL *mysql)  
              功能：存储 mysql_query()  或者  mysql_read_query() 的数据  
              失败， NULL,是一个不会导致任何伤害或性能降低的返回函数。  
       11)	unsigned int mysql_num_fields(MYSQL_RES *result)     
              功能：返回集合中列的个数，返回的是表中的属性列。  
       12)	MYSQL_FIELD *mysql_fetch_field(MYSQL_RES *result)  
              功能：返回集合中列的定义。  
       13)	MYSQL_ROW mysql_fetch_row(MYSQL_RES *result)  
             功能：返回集合中的一行， 结束或者错误返回NULL, 检索一个结果集合的下一行。当在mysql_store_result()之后使用时，    
             如果没有更多的行可检索时，mysql_fetch_row()返回NULL。  
       14)	unsigned long *mysql_fetch_lengths(MYSQL_RES *result)  
             功能：返回当前行中每一个字段值的长度。  

     
