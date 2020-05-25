Project: sparkify会员用户流失预测

sparkify是一个类似于网易云音乐、QQ音乐等提供数字音乐服务的平台。用户类型有带广告的免费用户、会员用户。会员用户每月支付固定费用免费听歌。任何时候，用户可以自己升级为会员用户或者降级为免费用户。用户的每次操作，例如播放歌曲、点赞、登录、登出、升级、降级等都会产生数据，这些数据包含了能让用户满意并帮助sparkify业务蓬勃发展的关键信息。数据集来源于Udacity，完整的数据集大小为12GB。

本项目基于完整数据集的一个子集，大小为231MB，预测哪些用户从会员降级为免费，或者直接取消服务了。如果在用户离开之前，可以精确识别到这些用户，sparkify可以通过给用户打折或者其他激励方式留住用户，这样就可以挽救数百位的营业额。

运行环境
	Spark 2.4.5
	Scala 2.11
	
数据集
	数据集来源于Udacity， 是完整数据集的一个子集，231MB。各字段含义如下：
	artist: 		string, 歌手
	auth: 			string, 登录状态
	firstName: 		string, 用户名
	gender: 		string, 用户性别
	itemInSession: 	long, 	页面停留时间，单位秒
	lastName: 		string, 用户姓
	length: 		double, 听歌时长，单位秒
	level: 			string, 用户类型，paid或者free
	location: 		string, 地理位置
	method: 		string, 页面请求，PUT or GET
	page:			string, 用户访问页面
	registration: 	long, 	注册时间, 从epoch开始的秒数
	sessionId:		long, 	与服务器会话的ID
	song:			string, 歌曲名称
	status:			long,	页面请求状态码，例如200表示成功返回网页，404表示页面不存在
	ts:				long,	事件发生时间，从epoch开始的秒数
	userAgent:		string, 用户使用的终端
	userId:			string, 用户ID，唯一