# Summary

##  查看xx进程启动的精确时间和启动后所流逝的时间
ps -eo pid,lstart,etime,cmd | grep 
## 常用方式1
ps aux | grep 
## 常用方式2
ps elf | grep 




# Usage

https://www.cnblogs.com/weifeng1463/p/8807849.html

然后再来看下ps aux的输出结果，其首行如下，说明了输出的各列：

USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND 

我们可以看到START和TIME列，通过 man 其说明如下：

bsdstart    START     time the command started.   If the process was started less than 24 hours ago, the output format is " HH:MM",  else it is " Mmm:SS" (where Mmm is the three letters of the month).  See also lstart, start, start_time, and stime.  bsdtime     TIME      accumulated cpu time, user + system.   The display format is usually "MMM:SS",  but can be shifted to the right if the process used more than 999 minutes of cpu time.  

START 是命令启动的时间，如果在 24 小时之内启动的，则输出格式为”HH:MM”（小时：分钟），

否则就是”Mmm:SS”（月份英语单词前 3 个字母：一月的第几号？[SS 这里面怎么理解？为什么有冒号呢？输出并没冒号]） 可以知道，这里并不能直接看出 24 小时之前启动的命令的精确启动时间。

TIME 是累积的 CPU 时间（user+system），显示格式通常是”MMM:SS”。（分钟：秒） 可以看出，这里并不是指从命令启动开始到现在所花的时间。

\-----------------------------------------------------

查看 nginx 进程启动的精确时间和启动后所流逝的时间：

[root@iZ25p102vo3Z ~]# ps -eo pid,lstart,etime,cmd | grep nginx 16968 Fri Mar  4 16:04:27 2016 41-21:14:04 nginx: master process /usr/sbin/nginx 17826 Fri Mar  4 22:53:51 2016 41-14:24:40 nginx: worker process 18312 Fri Apr 15 13:18:31 2016       00:00 grep --color=auto nginx