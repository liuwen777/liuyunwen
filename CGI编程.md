># CGI 编程  
  >>## CGI 的概念
      CGI(Common Gateway Interface) 是WWW技术中最重要的技术之一，有着不可替代的重要地位。  
         CGI是外部应用程序（CGI程序）与WEB服务器之间的接口标准，是在CGI程序和Web服务器之间传递信息的过程。
         
   >>## CGI 的基本使用
      1.int atoi(const char *nptr)：功能：将一个字符串转换成对应的数字，比如：“1234” ==》 1234。
      2.int fprintf(FILE *stream, const char *format, ...)：功能： 将格式化的语句输出到指定的流，
        举例：fprintf(stdin, "helloworld\n")  等价于 printf("helloworld\n")。
      3.MYSQL *mysql_init(MYSQL *mysql):功能：初始化函数，参数为NULL即可，接收返回值,  失败，NULL。
      4.MYSQL *mysql_real_connect(MYSQL *mysql, const char *host, const char *user, const char *passwd, const char *db,  
        unsigned int port, const char *unix_socket, unsigned long client_flag)：功能：连接mysql服务器
