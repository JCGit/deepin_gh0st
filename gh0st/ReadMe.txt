Gh0st RAT[2008127更新]

Gh0st RAT
C.Rufus Security Team
http://www.wolfexp.net

控制端与服务端都采用IOCP模型，数据传输采用zlib压缩方式
稳定快速，上线数量无上限，可同时控制上万台主机
控制端自动检测CPU使用率调整自己的工作线程, 稳定高效
宿主为svchost以系统服务启动,上线间隔为两分钟
心跳包机制防止意外掉线..
支持HTTP和DNS上线两种方式
自动恢复SSDT(这功能干什么，大家都知道，免杀自己做吧)
控制端224K，返朴归真的界面，生成的服务端无壳，156K，可多次重复安装,重复安装要等2秒，要退出守护线程
其它细节方面的功能大家自己去发现吧

功能:
文件管理  完全仿Radmin所写, 文件、文件夹批量上传、删除、下载、创建、重命名..
屏幕监视  此模块全用汇编编写，传速速度快，控制屏幕，发送Ctrl+Alt+Del，7种色彩显示方式
键盘记录  可记录中英文信息，离线记录(记录上限50M)功能
远程终端  一个简单shell
系统管理  进程管理，窗口管理，拨号上网密码获取
视频监控  监控远程摄像头
会话管理  注销，重启，关机，卸载服务端
其它功能  下载执行指定URL中的程序，隐藏或者显示访问指定网址，清除系统日志
地址位置  将IP数据库文件QQWry.Dat放置程序同目录下即可显示地理位置
集群控制  可同时控制多台主机，同时打开视频监控等管理功能


演示地址
http://www.wolfexp.net/other/Gh0st_RAT/index.html
http://www.wolfexp.net/other/Gh0st_RAT/demo.rar


更多请关注红狼安全小组官方网站 http://www.wolfexp.net/



#源码分析


CMainFrame	主UI框架类																										-
																															|
	NotifyProc	接收，并分发网络事件																						|
																															|	
	@NC_CLIENT_CONNECT																										|
	@NC_CLIENT_DISCONNECT																									|
	@NC_TRANSMIT:																											|
	@NC_RECEIVE:					->	处理进度																			|
	@NC_RECEIVE_COMPLETE			->  事件完成	-> 分发 窗口消息  逻辑消息												|
																															|		
																															|
																															|
																															|
CGh0stApp	主逻辑类																										|
	|																														|
	|																														|
	-------------------CGh0stView 链接视图类																				|
							|																								|
							|																								|
							|																								|
							--------------------------初始化 创建CSettingsView												|
							|								 创建CBuildView													|
							|																								|	
							|																								|
							|																	NotifyProc					|	
							-------------------------CIOCPServer 控制端IO控制  ---------------------------------------->CMainFrame
																|															|
																|															|
																|-----------ListenThreadProc------------------OnAccept------------PostRecv
																|												  |			|
																|												  |(绑定)	|
																|-----------完成端口-------------------------------			|
																|															|
																|															|
																|-----------ThreadPoolFunc工作线程-----------------ProcessIOMessage(OnClientReading, OnClientWriting, OnClientInitializing)



#功能分发
@CFileManagerDlg		文件管理
@CScreenSpyDlg			屏幕控制
@CWebCamDlg				视频查看
@CAudioDlg				语音监听
@CKeyBoardDlg			键盘记录
@CSystemDlg				系统管理
@CShellDlg				远程终端













