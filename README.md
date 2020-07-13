# CSS
学习笔记


1. 架构介绍	
	大前端，后台，硬件
2. 开发环境
	1) 编辑器
		sublime
		vscode (*)
	2) 浏览器
		firefox 			火狐
		google chrome 谷歌
		opera 				欧朋

3. 部署环境 (购买阿里云)
	linux (文件操作，vi)
		1)	虚拟机 
		2)	云服务器 9.5元/月 
			阿里云 	
				轻量应用服务器 	半年
				区域 	华东（上海）
				系统镜像
				ubuntu16.04

				重置root密码

			外网ip 
			root账号	:	root
			root密码	: 

	gitee（码云，国产版的github）/github
		注册账号

4. html
	1) 超文本标记语言
		超级文本 （txt 字符类型）
			文本、图片、视频、音频、超链接...
		标记 （xml）
			<div>hello world</div>
			<h1>你好，世界</h1>

			div 标记"hello world" 为一个普通的块元素的内容
			h1 	标记 "你好，世界"为一个以及标题的元素的内容
		语言
			标记语言
				xml
				html
			编程语言
				c、java 	强类型编程语言
				js、php	弱类型的编程语言
	2) 结构
		<!Doctype html5>
		<html>
			<head>
				<meta />
				<link />
			</head>
			<body>
				<div>
					<span>hello</span>
				</div>
				<img/>
				<h1></h1>
			</body>
		</html>

					html
		head					body
	meta 	link	div 	img 	h1
							span
	3) 语法
		html由多个标签（元素）组成，标签可以嵌套，树型结构

		元素：
			双标签元素
				<标签 属性名=属性值 属性名=属性值 >
					子标签/内容
				</标签>

				标签名，属性名不区分大小写（编程习惯要区分）
				属性值区分大小写，并且可以用引号引起来

				属性:
					核心属性：绝大多数标签都具有的属性
						title 	提示
						id 			唯一标识
						class 	分类标识
						style 	内置样式
					自有属性：只有某些特定的标签才具有的属性
						a 		href 、target
						img 	src、alt、width、height

				<div title="hello" id="one"> hello world </div>
				<div> 
					<span> hello world </span> 
				</div>

			单标签元素
				<标签 />

			注释
				<!-- 注释内容 -->

5. 代码放哪里？
	512G 固态 （默认不分区）
	c:/
		windows
		program files
		program files(x86)
		...
		users
			admin
			licy
				图片
				视频
				收藏
				桌面 
	d:/briup/
		1-html
			day01

		2-css
		3-linux
		4-js

6. hello world
	1） 编写代码
		hello.html
	2） 运行代码
		浏览器

7. 块元素
	语义化

	作用：
		搭建网页结构
	特点：
		1) 独占一行空间
		2) 默认宽度为100%
		3) 高度由子元素或内容决定
		4) 可以通过css指定其宽度
	举例说明
		了解原有特性，去除样式，添加自己的样式
		
		div 	无意义的块元素（不知道使用哪个标签的时候就是使用div）
		html
		body
		h1~h6 标题
		p
		ul>li
		ol>li
		dl>dt,dd
		
		H5新增的语义化标签
		article


8. 行内元素	
	作用：填充
	特点：
		与其他行内元素共享一行空间
		不能通过css为其指定宽高
		宽高由自身决定，内容的容器
	标签
		span 
		a
			href:
				相对地址
					山西省太原市尖草坪区xxx号3栋202
					隔壁的201
				绝对地址
					山西省太原市尖草坪区xxx号3栋201
			target
		img
		video
			controls
			autoplay
		audio
		H5过期的语义化标签
		strong 、i、 em

9. 功能元素
	table 【border width cellspacing】
		caption
		thead
			tr
				td/th 【rowspan 、colspan】
		tbody
			tr
				td/th
		tfoot		
	form
		input
			单行文本框 	 type="text"
			密码框 			type="password"
			单选按钮		type="radio"
			复选框 			type="checkbox"
			附件按钮 		type="file"
		select
		textarea
		button
		username:男
		password:123321
		gender:male

		application/x-www-form-urlencoded
			username=0BX0NW@password=123321&gender=male
		multipart/form-data
			只要表单元素中包含<input type="file">，只能为它

	iframe
		src

===================
css
1. 介绍
	层叠样式表
		结构		前凸后翘 		html
		装饰 		化妆 				css
		内涵		谈吐 				js	
2. 语法
	1) 在html中如何引入css
		1. 将css规则直接填写在style属性中
		2. 将样式嵌入到style标签
		3. 将样式写在.css文件中，再通过link将这个文件引入到html中

	2) 语法组成
		选择器 {
			属性:值;
			属性:值;
		}

		ul {
			margin:0;
			padding:0;
			list-style:none;
		}

		<ul class="nav">
			<li></li>
			<li></li>
			<li></li>
		</ul>
		<ul>
			<li></li>
		</ul>

3. 选择器
	1) 核心选择器
		标签选择器		
			div {}
			ul {}
			dl {}
		类选择器
			.nav {}
		id选择器
			#id {}
		组合选择器
			body , ul {}
		并且选择器
			ul.nav {}
		普遍选择器
			*
	2) 层次选择器
		父子选择器 
			父 > 子
			.nav > li { }
			#wrapper > * {}
			.right_nav > li {}
		后代选择器
			父   后
			.right_nav li {}
		下一个兄弟选择器
			selector + selector
		之后所有兄弟选择器
			selector ~ selector

	3) 伪类选择器【过滤器】
		:first-child
		:last-child
		:nth-child(参数)
			参数：数字,表达式(2n ,2n+1),关键字(odd、even)
	4) 伪元素选择器【过滤器】
		::after
		ul.nav::after {
			display:"block"	
		}

		<ul class="nav">
			<li></li>
			<li></li>
		</ul>
	5) 属性选择器【过滤器】
		[name] 						选择具有name属性的元素
		[name=username]		选择具有name属性,并且属性值为username的元素
		[name^=u]					选择具有name属性,并且属性值以u开头的的元素
		[name$=u]					选择具有name属性,并且属性值以u结尾的的元素
		[name*=u]					选择具有name属性,并且属性值包含u的的元素
4. 优先级
	特权
		!important
	权值
		1000	style属性		
		100		#id
		10		.class 、伪类
		1			元素
	顺序
5. 盒子模型
	针对于块元素讨论盒子模型
	1) 基本概念
		外边距 	margin
			margin-top
			margin-right
			margin-bottom
			margin-left
			margin 	
		边框		border
			border-top
				border-top-color
				border-top-style
					solid
					dotted
					dashed
					double
				border-top-width
			border-right
				border-right-color
				border-right-style
				border-right-width
			border-bottom
				border-bottom-color
				border-bottom-style
				border-bottom-width
			border-left
				border-left-color
				border-left-style
				border-left-width
			border
				border:1px solid #ccc;
				是border-top，border-right，boder-bottom，border-left的速写形式
		内边距 	padding
			padding-top
			padding-right
			padding-bottom
			padding-left
			padding 	速写
				5px
				0 5px 						上下0,左右5px
				0 5px 10px 				上0 	左右5px 	下10px
				0 5px 10px 20px 	上右下左
		宽 			width
		高			height
	2. 盒子模型
		1) 怪异盒模型（IE8-）jquery - 银行
			box-sizing:border-box;
			盒子所占的宽度 = width （包含了border + padding + 内容实际宽）
		2) 传统盒子（firefox）	
			box-sizing:content-box;
			盒子所占的宽度 = border + padding + width 	

6 浮动布局
	层次关系
	1. float:left
		1) 块元素脱离默认文档流
			1. 默认宽度为0
			2. 失去了对父元素支撑的能力 【伪元素】
		2) 在浮动流中，多个浮动元素在一行中显示，当这一行容纳不下，会自动换行


	2. 案例



















--------------------- 找工作 -----------------------
1) 撰写简历
	个人介绍
		太原理工大学			本科
		gitee地址:			
		个人网站地址:	
		个人博客地址:
			归纳 整理 演绎【学习能力】
	职业技能
		1. 熟练掌握html/css/js , 能根据设计图重构页面
		2. 熟练使用 linux
		3. 熟悉vue技术栈...
		4. 熟练使用git/svn 版本控制工具
		...
	项目经验
		团队项目 - gitee /github (4个人) - 4个
		项目介绍：
		角色：
		开发周期：
		项目预览地址
			1. 看点精选（资讯发布）公众号 
			2. 滴滴打车，家政服务预约平台（餐馆点餐预约）
				消息队列 rabitMQ
			3. 监控设备
			4. 电商辅助平台（刷单）
2) 投简历
	一年以上工作经验
    
3) 面试
	实验室 、自学
	实习 8k
4) 谈薪资
5) offer


=================================
1. 阿里云服务器如何上传文件
	1) ip root 密码
	2) 常用命令
		ssh 用于远程登录阿里云
		> ssh 用户名@ip
		> ssh root@121.199.29.84

		scp 用于本地文件与阿里云进行传递
		> scp 本地文件路径 用户名@ip:上传在linux中的哪个路径
		> scp ./a.txt root@121.199.29.84:/opt
2. 如何将我们的网页部署到apache
	1) 安装apache
		121.199.29.84
		=>
		http://121.199.29.84:80/index.html

		# apt-get install apache2
		安装好之后直接启动

	2) 将网页部署到apache的部署目录
		默认的部署目录位于 
			/var/www/html

		http://121.199.29.84/index.html
			=》/var/www/html/index.html

		http://121.199.29.84/1-hello.html
			=》/var/www/html/1-hello.html

		http://121.199.29.84/cms/a.html
			=》/var/www/html/cms/a.html



















	
















