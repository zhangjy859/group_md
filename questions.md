# 常见问题
## 服务器/连不上网/下不了数据怎么办？
如果发现服务器网络连接异常，建议先通过下面的命令进行确认
```shell
$ curl -L baidu.com
```
正常情况下会返回百度的重定向页面
```
<html>
<meta http-equiv="refresh" content="0;url=http://www.baidu.com/">
</html>
```
如果你并未看到这一段返回值，则代表服务器网络连接可能存在问题，通常情况下可能是校园网掉线了。
这种情况下请转到 `/public/group_data/software`目录下，这个目录中准备了`NetAuth.py`和`NetAuth.sh`两个程序，你可以任选其一，通过自己的校园网id和密码进行验证后恢复服务器的网络连接，例如:
```
# do not enter []
$ python NetAuth.py [your_std_id] [your_std_passwd]
$ bash NetAuth.sh [your_std_id] [your_std_passwd]
```
大多数情况下，运行上面的脚本后即可以恢复上网
