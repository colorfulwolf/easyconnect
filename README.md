安装后登录闪退须在登录进度过半时执行

`sudo /usr/share/sangfor/EasyConnect/resources/shell/sslservice.sh`


或者保存一下内容为sh文件，在连接前执行。

```
#!/bin/bash
tail -n 0 -f /usr/share/sangfor/EasyConnect/resources/logs/ECAgent.log | grep "\\[Register\\]cms client connect failed" -m 1
sudo /usr/share/sangfor/EasyConnect/resources/shell/sslservice.sh
```
