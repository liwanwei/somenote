
[TOC]

## PHPMyAdmin修改登录密码 ##
1. 找到WampServer程序安装目录，在apps目录找到phpmyadmin的目录。  
2. 打开phpmyadmin目录里面的config.inc.php文件，找到下面代码：$cfg['Servers'][$i]['password']       = ''
3. 在等号右面的单引号里面输入刚才设置的密码，保存。


##设置wamp自定义网站根目录##
1. 找到并打开wampmanager.ini文件，文件中PHPDemo directory为菜单栏上显示的内容，FileName后面为文件映射路径。

		Type: item; Caption: "PHPDemo directory"; 
		Action: shellexecute; FileName: "H:/PHPDemo"; Glyph: 2  
2. 找到并打开wampmanager.tpl文件，文件中

		[Menu.Left]
		;WAMPMENULEFTSTART
		Type: separator; Caption: "Powered by Alter Way"
		Type: item; Caption: "${w_localhost}"; Action: run; FileName: "${c_navigator}"; Parameters: "http://localhost/"; Glyph: 5
		;WAMPPROJECTSUBMENU
		
		Type: item; Caption: "${w_phpmyadmin}"; Action: run; FileName: "${c_navigator}"; Parameters: "http://localhost/phpmyadmin/"; Glyph: 5
		Type: item; Caption: "PHPDemo directory"; Action: shellexecute; FileName: "H:/PHPDemo"; Glyph: 2
最后一列改为，（改之前长什么样子忘记了，应该是 "${w_web director}）这里改为

		Type: item; Caption: "PHPDemo directory"; Action: shellexecute; FileName: "H:/PHPDemo"; Glyph: 2

3. 重启服务

## Sublime Text 2关闭自动更新 ##

[百度经验]("http://jingyan.baidu.com/article/cdddd41c6ad82553ca00e14e.html")

## Sublime Text 2 licence ##

	----- BEGIN LICENSE 
	Alexander 
	Single User License 
	EA7E-814345 
	51F47F09 4EAB1285 7827EFF0 8B1207DC 
	A76A6EA3 E1A1CA7A DC1F2703 14,897,784 
	8EDC1C82 3F2A58B9 1C0C8B24 67686432 
	281245B3 6233DE5C ADC5C2F9 61FB8A04 
	171B63EF 86BA423F 6AC884FD 3273A7AA 
	5F50A6DB CE7859AE D62D2B37 AEEDD8C2 
	078A8A20 70EEA791 84F48C1E 8ABA7DEB 
	0B3907C0 C9A3523B 0091A045 6F67AED8 
	------ END LICENSE ------

[原文出处]("http://www.litefeel.com/sublime-text-2-license/" )

## 配置SublimeLinter提示“Trailing comma before closing bracket”的问题 ##

注意逗号问题

[博客](http://www.liudon.org/1048.html)

## 一段JS代码让Markdown自动生成目录 ##


[一段JS代码让Markdown自动生成目录](http://www.iyanlei.com/markdown_catelog.html)

##一个git page的例子##
[coolwubo](http://www.coolwubo.com/)


## JSON语法 ##

![alt text](/JSON.jpg "JSON语法规则")

## JSON解析 ##
- eval  
较危险，可能执行其他人的恶意代码，一般不用


- JSON.parse

## JSON 格式化检验工具 ##
[http://jsonlint.com/](http://jsonlint.com/ "http://jsonlint.com/")

## 使用jQuery实现ajax##


![alt text](/ajaxinjQuery.jpg)


## 跨域访问 ##

- 通过后台设置代理
- 通过前端解决
	- 前端  

##产品经理的能力##
1. 用户的研究
2. 需求的分析
3. 产品的设计
4. 文档的撰写
5. 产品的运营
6. 数据的分析
7. 沟通协作
8. 项目管理
9. 业务规划
10. 产品规划
11. 产品管理
12. 专业能力

## 产品经理的能力 概括版 ##
1. 用户研究能力
2. 领域知识，相关产品的知识
3. 大局观
4. 准确定位的能力
5. 项目管理的能力
6. 团队协作的能力
7. 逻辑思考的能力
8. 心理学相关的内容

## 产品经理 ‘年龄’层 ##
1. 市场调研
	1. 研究市场，了解用户的需求，发现创新以及改进产品的机会
	2. 真正体验自己的产品，真正了解用户的需求是什么。
	3. 做用户访谈而不是问卷调查，for问卷调查或多或少有自己主观的内容。注意不要引导用户。
	
2. 产品运营及设计
	1. 产品的定义是确定产品要做什么样的事情，如UI、UE，pid？prd？因此产品经理必须掌握基础的交互设计。
3. 项目管理
	1. 协调不同部门人员共同完成产品，确保资源投入，确保产品上线，开发的一些计划
	2. 定期沟通进度，对进度进行判断，判断是否需要增加新的资源或者延期or？？ 
4. 产品？璇姐？界
	1. 吸引的目标市场有哪些，为什么吸引用户，市场宣传的一些合作
	2. 对行业的分析，抓住产品的特点，寻求与其他产品的差异点  
5. 产品市场
	1. 通过各种方法告诉用户产品的信息
	2. 包括flash、ppt、操作手册等
4. 产品生命周期的管理
	1. 理论阶段、成长阶段、初期阶段、成熟阶段、怎么推出怎么衍生出新的内容
	2. 在不同的阶段有不同的打算


## 重中之重：用户需求 ##
互联网思维：以用户为中心

## 为何要创业 ##

## 快速知道自己创业是否可行 ##
1. 看一下天使圈？[创投圈](http://baike.baidu.com/link?url=l4vuUTXmzs2EJnEzhgxCQwuDq8XsGB83DKB8vuOozPZjxVJhoxL1yixU7F4XByv_Scq7ybdtFKHUU6wPRX_0O_ "创投圈百度百科")？[创圈](http://weibo.com/u/2050559574?topnav=1&wvr=6&topsug=1&noscale_head=1#_0 "创圈微博链接")
2. 创意如果只是创意，不要拿来创业

## PM养成的路上有哪些细节习惯的养成##
1. 培养用户思维
2. 日常生活中多思考为什么产品要这样设计  
eg.
	- 麦当劳以及肯德基的门为什么是往外开而不是往里开的？  
	- 接到一个传单，能都一眼看出目标用户是谁，产品的核心功能是什么，与用户交互上面还有哪些不合理的点  


## 互联网产品有什么样的特征，从概念到产品一般要经历什么样的过程 ##
1. ……
1. 更新速度快。竞争激烈，需要根据用户的反馈不断优化。
  
过程
1. 明确的用户群体
2. 明确的商业模式
3. 抓到核心用户的需求点是什么，找到刚需。

## 在线生可以做哪些努力 ##
1. 获得面试的机会-->脸皮要厚，光通过简历，没有好的实习经历，可以去做霸面。为了获得这样的机会就要付出什么，企业会认为你有持之以恒的能力
2. 如果面试-->面试技巧。
	1. 提前了解PM的素质要求
	2. 了解企业的业务
	3. ……
3. 你最常用的产品是什么，该产品有何优缺点，你可以怎样优化？-->卡住了很多人的一道题目。
4. 面试官会根据你的经历提问，你之前如何做用户调研，遇到问题怎么协调，你任务这样行业的用户有什么样的特点，行业竞争对手的对比，竞争对手的产品，优缺点是什么，我方的产品的优缺点是什么？
5. 你的优缺点是什么，各列举三个，据此分析一下你为何适合做一个PM？

##对应届生来说，是拥有BAT的实习经验（非PM）重要还是小公司的PM实习经验重要##
1. 大公司与小公司的优缺点？小公司的产品实践经验更重要，小公司的工作比较全面，而BAT的实习经验，接触的多是某一项单独的工作，如文字审核等等。
2. 但若想获得BAT的offer，还是BAT的实习经验还是比较经验的。HR招聘是可以偷懒说之前BAT已经认可你，我可以偷懒。
3. 还是要尽自己所能，去获取更多的知识。
4. 校招中有优势
	1. 要有好的实习经历。
	2. 对某一行业的产品的深入分析
	3. 建议看一下《精益创业》和《精益创业实战》

## PM所具备的道，如思维能力（批判性、理性分析能力、感性认识等），管理能力（情绪、时间、自我等）如何更快速的培养 ##
1. 建议从用户、定位、功能这三个角度去做分析，会有很快的提升
2. 管理能力可以从一些日常小事入手，例如如何快速读完一本书并提炼出核心点
3. 其实宏观意义上的管理能力更强调对其他人的管理，这一点可以更多地看马斯洛需求理论以及心理学的书




