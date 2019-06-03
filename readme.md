##  设计思路

	1、目录索引，文件索引

	2、配置文件
		日志目录： file_dir: '/data/tomcat/tomcat8081/logs' 
		到期时间： expire_time: '7'
		文件大小： file_size: '1'
		正则过滤： file_re: ['log$', 'out$']
		临时目录： file_tmp: '../tmp'}

	3、执行动作
		过滤目录，如果文件大于1G 则置空，否则 压缩7天前文件

	4、文件压缩到tmp 目录下

	5、zabbix 提醒删除文件