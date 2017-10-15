# linux tools#

1. 抓包
wireshark
yum install wireshark-*


2. 测试网络带宽
	qperf
	
	ｑｐｅｒｆ　启动作为ｓｅｒｖｅｒ
	qperf 10.232.64.yyy tcp_bw tcp_lat conf　／／测量到机器的带宽
	
	http://blog.yufeng.info/archives/2234

3. 带宽控制工具dummynet

http://blog.csdn.net/fs1360472174/article/details/51340368


4. 进程控制supervisor

http://blog.csdn.net/xyang81/article/details/51555473

supervisor status 查看状态，
如果修改了配置文件，或者增加了进程，可以使用 supervisorctl update来生效
