## Linux time

linux系统获取时间在<time.h>文件中<br>

主要有两个关于时间的定义:time_t 和 struct tm; 
* time_t linux系统时间类型，单位为秒
* struct tm 时间结构体，可以根据time_t解析相应的时间


有关时间的系统调用
```c
    time_t time(time_t*) // returns  the  time  as  the  number of seconds since the Epoch, 1970-01-01 00:00:00 +0000 (UTC).
    char *asctime(const struct tm *tm);
    char *asctime_r(const struct tm *restrict tm, char *restrict buf);

    char *ctime(const time_t *timep);
    char *ctime_r(const time_t *restrict timep, char *restrict buf);

    struct tm *gmtime(const time_t *timep);
    struct tm *gmtime_r(const time_t *restrict timep,
                        struct tm *restrict result);

    struct tm *localtime(const time_t *timep);
    struct tm *localtime_r(const time_t *restrict timep,
                        struct tm *restrict result);

    time_t mktime(struct tm *tm);
```