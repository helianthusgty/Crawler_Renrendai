Crawler_Renrendai 人人贷使用说明
=================
http://www.we.com/
#一：代码介绍：
一共包含了4个可执行脚本：
##Crawler_renrendai.py:
	【目的】抓取loanId在某一范围的借贷情况，样例对应网页：http://www.we.com/lend/detailPage.action?loanId=1000
	【输入】loanId的起始ID号和结束ID号
	【输出】(1)网页抓取的数据csv文件(2)对于未抓取到数据的loadId会被写入到orderlist文件中。
##OrderCrawler_renrendai.py：
	【目的】批量抓取借贷情况
	【输入】orderlist文件，记录了loanId号，每行一个
	【输出】网页抓取的数据csv文件
##UPCrawler_renrendai.py:
	【目的】抓取U计划的所有借贷情况
	 样例对应网页：http://www.we.com/financeplan/listPlan!detailPlan.action?financePlanId=1
	【输入】无
	【输出】网页抓取的数据csv文件，其中包括基本信息，评论信息，关注列表等信息
##SPCrawler_renrendai.py:
	【目的】抓取薪计划的所有借贷情况，
	 样例对应网页：http://www.we.com/autoinvestplan/listPlan!detailPlan.action?autoInvestPlanId=20026
	【输入】无
	【输出】网页抓取的数据csv文件，其中包括基本信息，评论信息，关注列表等信息
#二：执行脚本
##准备
    确保config.ini存在
    确保datas文件夹存在，进入文件夹后确保UP，SP文件夹存在；若不存在，新建即可。
    若要执行批处理OrderCrawler_renrendai脚本，需确保orderlist文件存在，若不存在新建即可
##直接执行py脚本
需保证系统安装了python3.0的环境
##若想执行.exe脚本
修改setup.py编辑需要转化的脚本，直接执行脚本即可。存储在dist文件内，再回到（1）即可
