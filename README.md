# C-log
   Easy and Efficient，Multiple threads And Multiple Handles.

   It offers Logging Levels、IO Buffer、 Backup、LOG Size Control、Stack print、Encrytion(AES-128)、

Compression(lz4)、HashTab(MD5).
   
   这是一个简单、高效和轻量级C语言写的的日志系统，linux下不需要第三方库安装。目前主要是在linux

下编写和测试，通用分支为一个基于Apache的APR(一个C语言跨平台的开源库)编写的跨平台版本，由于精力有

限只基于最简单的日志打印功能进行了改写，仅供参考。
   
   日志系统支持多线程多句柄、印级别控制、IO缓存设置、备份控制、日志文件大小控制、异常退出堆栈

打印、加密(AES-128)、压缩(lz4)和散列校验(MD5)。所有配置和接口都在log.h内。堆栈打印是接收所有

异常退出信号时打印堆栈，输出文件名通过TRACE_PRINT_PATH宏控制，在其信号处理时还对所有日志句柄进

行刷新处理，减少日志丢失可能。详细接口功能可看[这里](https://www.cnblogs.com/prophet-ss/p/8025825.html)
