# Summary

##  url 
https://www.runoob.com/python3/python3-date-time.html
## 输出时间

```
time.strftime("%Y-%m-%d %H:%M:%S", time.localtime())  # '2019-11-04 09:10:48'
```

## 毫秒字符串

```
datetime.datetime.now().strftime('%Y-%m-%d %H:%M:%S.%f')  # '2019-11-04 09:12:14.947580'
```

## 时间判断
```
local_time = datetime.datetime.now()
if local_time.weekday() in range(0, 5) and (local_time.hour in (11,) and local_time.minute in (30,)) or \
                (local_time.hour in (14,) and local_time.minute in (0, 30)):  # 0 是 星期一, range(0,5)=[0,1,2,3,4]，即周一到周五
```


# Usage

xxxx