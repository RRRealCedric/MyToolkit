

## 1. 基本命令与帮助文档
date ； cal ； bc

热键：ctrl+c中断输出 ctrl+d终止输入 shift+pageUp/Down

--help ； man/info + command 

man -f （即 whatis [指令或数据]）
man -k （即apropos[指令或数据]）搜寻特定指令/文件的说明文件

nano编辑器

观察系统的使用状态：
who 查看在线用户; netstat -a 查看网络联机状态; ps -aux 查看后台运行的程序

关机(使用管理工具systemctl)：shutdown ; reboot ； halt ; poweroff

## 2. 文件权限与目录配置  

文件所有者、群组、其他人、root

su - 切换root身份
exit 回到原来身份
ls -al 即list

文件类型：
d：表示目录
-：文件
l：连接文档（link file），类似快捷方式
b：装置文件里面的可供存储的接口设备（可随机存取装置）
c：装置文件里面的串行端口设备、例如键盘、鼠标（一次性读取装置）
s: 数据接口文件，通常被用在网络上的数据承接。启动程序监听客户端的请求，客户端透过这个 socket 来进行数据的沟通 最常在 /run 或 /tmp 这个目录中
p: 数据传送文件，FIFO 也是一种特殊的文件类型，主要目的在解决多个程序同时存取一个文件所造成的并发错误问题， 是 first-in-first-out 的缩写
权限：
![markdown-img-paste-20191007223016266.7d73d35c.png](../../../../AppData/Local/Temp/markdown-img-paste-20191007223016266.7d73d35c.png)

r = 4
w = 2
x = 1

chgrp：改变文件所属群组 组名必须在/etc/group
chown：改变文件拥有者   用户名必须在/etc/passwd
chmod：改变文件的权限、SUID、SGID、SBIT 等等的特性

拷贝文件：cp 来源文件 目标文件

文件扩展名：
.sh：脚本或批处理文件（scripts），因为是使用 shell 写成的，所以扩展名就编程 .sh
Z、.tar、.tar.gz、.zip、.tgz：经过打包的压缩文件。不同的压缩软件压缩的扩展名不同如，gunzip、tar
.html、.php：网页相关文件

目录配置 FHS
![markdown-img-paste-20191011231944885.3bb53b61.png](../../../../AppData/Local/Temp/markdown-img-paste-20191011231944885.3bb53b61.png)

文件路径：
绝对路径：由根目录开始写起的文件或目录，例如 /home/mrcode/.bashrc
相对路径：开头不是 / 则是相对路径，例如： ./home/mrcode
.：代表当前目录，也可以使用 ./ 来表示
..：代表上一层目录，也可以使用 ../ 来表示


