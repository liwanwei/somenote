# AJAX #
Asynchronout JavaScript and XML(异步的JavaScript 和 XML)  
预备知识：HTML JS CSS

# 概念介绍 #
- 同步
- 异步 
- XMLHttpRequest对象  
使得可以不重新加载整个页面的情况下实现数据的局部更新


基本步骤  
1. 运行HTML和CSS来实现页面，表达信息；  
2. 运用XMLHttpRequests和web服务器来进行数据的异步交换；  
3. 运用JavaScript操作DOM，实现动态局部刷新；  

具体步骤  
1. 实例一个XMLHttpRequest对象  

	var request = new XMLHttpRequest();  
**NB.**IE5、IE6中不支持，使用前应该判断其是否为IE5、IE6

	var request; 
	if(window.XMLHttpRequest){
			request = new XMLHttpRequest(); 
	}else{
		request = new ActiveObject("Microsoft.XMLHTTP");//IE5、IE6 
	}
## XMLHttpRequest发送请求 ##
- open(method,url,async)
> - method:get/post,大小写都可以；  
> - url:  请求地址，可以使用相对地址，也可以使用绝对地址；  
> - async:ture/false,ture为异步处理，默认；false为同步处理；

- send(string)
>将请求发达服务器，使用get可以不填写string，但是用post要有带参数；

	request.open("POST","creare.php",true);
	request.setRequestHeader("Content-type","application/x-www-form-urlencoded");//告诉服务器我们要发送一个表单；setRequesHeader一定要写在open与send中间，否则会抛出一个异常。
	request.send("name=王二狗&sex=男");

## XMLHttpRequest取得响应 ##
- requestText:获得字符串形式的响应数据
- requestXML:获得XML形式的响应数据
- status和statusText：以数字和文本形式返回HTTP码
- getAllResponseHeader():获得所有的响应报头
- getResponseHeader():查询响应中的某个字段的值


- readyState属性在响应返回成功是得到通知
	- 0：请求未初始化，open还没有调用
	- 1：服务器连接已建立，open已经调用了
	- 2：请求已接受，也就是接收到头信息了
	- 3：请求处理中，也就是接收到响应主体了
	- 4：请求已完成，且响应已就绪，也就是响应完成了  

可以使用onreadstatechange方法监听

	var request = new XMLHttpRequest();  
	request.open("POST","creare.php",true);
	request.setRequestHeader("Content-type","application/x-www-form-urlencoded");  
	//告诉服务器我们要发送一个表单；setRequesHeader一定要写在open与send中间，否则会抛出一个异常。
	request.send("name=王二狗&sex=男");
	
	request.onreadstatechange=function(){
	if(request.readyState ===4 && request.status===200{
		//表示响应完成而且请求成功,做一些事情
	}
	}


XAMMP:www.apachefriends.org/download.html