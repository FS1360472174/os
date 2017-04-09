#linux 常用命令#

1. cat

	显示整个文件 cat filename
	
	创建文件 cat > filename
	
	合并文件 cat file1 file2 > file


2. 重启网络服务
	ｓｅｒｖｉｃｅ　ｎｅｔｗｏｒｋ　ｒｅｓｔａｒｔ

3. 远程copy 文件
	scp 原路径 目标路径
	scp root@169.53.174.168:/opt/cloudantrebal
	
	复制文件夹： cp **-r** dir1 dir2


4. 查看cpu 信息
	lscpu


5. --查看文件系统的磁盘空间占用情况
df

6. 查找文件路径
	find / -name haproxy.cfg
	find -name chatmessage*
	以**开头的文件
7. 查找磁盘大小
	df -lh
	
	du -h >fs.log
	生成日志
	
	du -h -s /srv 查看文件夹大小
	查看大文件
	find . -type f -size +800M
	查找大文件夹
	du -h --max-depth=1
	
	durep -x -hs 5000M  /srv |less 查看大文件

8. 查看操作系统版本
head -n 1 /etc/issue
查看内存信息：cat /proc/meminfo 
9. 查看内核版本
uname -a

10. 查看所有的环境变量
env

11. sudo

		-b
		在后台执行指令。
		-h
		显示帮助。
		-k
		结束密码的有效期限，也就是下次再执行sudo时便需要输入密码。
		-l
		列出目前用户可执行与无法执行的指令。
		-s<shell>
		执行指定的shell。
		-u<user>
		以指定的用户作为新的身份。若不加上此参数，则预设以root作为新的身份。
		-v
		延长密码有效期限5分钟。
		-V
		显示版本信息


12. linux 查看端口占用
netstat -apn| grep 8080

13. linux 查看服务器时间
date




15. ls -al filename 
du -sh
查看文件大小

16. 更换jdk 版本
update-alternatives --config java 

17. redhat 安装软件
	yum install **
	
	.tar 
	解包：tar xvf FileName.tar
	打包：tar cvf FileName.tar DirName
	（注：tar是打包，不是压缩！）
	———————————————
	.gz
	解压1：gunzip FileName.gz
	解压2：gzip -d FileName.gz
	压缩：gzip FileName
	.tar.gz 和 .tgz
	解压：tar zxvf FileName.tar.gz
	压缩：tar zcvf FileName.tar.gz DirName
	———————————————
	.bz2
	解压1：bzip2 -d FileName.bz2
	解压2：bunzip2 FileName.bz2
	压缩： bzip2 -z FileName
	.tar.bz2
	解压：tar jxvf FileName.tar.bz2
	压缩：tar jcvf FileName.tar.bz2 DirName
	———————————————
	.bz
	解压1：bzip2 -d FileName.bz
	解压2：bunzip2 FileName.bz
	压缩：未知
	.tar.bz
	解压：tar jxvf FileName.tar.bz
	压缩：未知
	———————————————
	.Z
	解压：uncompress FileName.Z
	压缩：compress FileName
	.tar.Z
	解压：tar Zxvf FileName.tar.Z
	压缩：tar Zcvf FileName.tar.Z DirName
	———————————————
	.zip
	解压：unzip FileName.zip
	压缩：zip FileName.zip DirName
	———————————————
	.rar
	解压：rar x FileName.rar
	压缩：rar a FileName.rar DirName
	———————————————
	.lha
	解压：lha -e FileName.lha
	压缩：lha -a FileName.lha FileName
	———————————————
	.rpm
	解包：rpm2cpio FileName.rpm | cpio -div


18. 解压缩
zip  -qr apache.zip /root/apache
zip  -r fileName.zip  文件夹名

19. 设置开机自启动
chkconfig ** on

20. kill pid 
如果进程杀不掉
kill -9 pid

21. 测ｄｉｓｋ速度
dd if=/dev/zero of=./largefile bs=1M count=1024

22. ｕｎｌｏｃｋ　屏幕
	ｌｏｇｉｎｃｔｌ　ｌｉｓｔ－ｓｅｓｓｉｏｎｓ
	ｌｏｇｉｎｃｔｌ　ｕｎｌｏｃｋ－ｓｅｓｓｉｏｎ　＄ｓｅｓｓｉｏｎｉｄ

	使用ctrl+c

23. 查看磁盘是不是ssd
	cat /sys/block/sda/queue/rotational
	返回 0, 就是 SSD

	或者ｌsscsi

24. 查看文件夹在哪个分区
df /file_dir

25. 设置环境变量
修改 /etc/profile
source /etc/profile
COLLECTD_DOCKER_TASK=collectdTask
COLLECTD_DOCKER_APP=collectdApp
export COLLECTD_DOCKER_TASK
export COLLECTD_DOCKER_APP
重新登录即可

ps -efla 


