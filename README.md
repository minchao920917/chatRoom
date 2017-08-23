##		基于java的聊天室小程序

###		知识基础：

应用到的java知识点有：

1.	Thread 线程
	
	线程池，线程启动，接口等。客户端，服务器端都用到了线程

2.	Socket
	
	使用了socket进行端口监听和数据传递
			new Socket("localhost",port);

3.	Swing图形化
	
	简单的按钮，输入框，弹框等

4.	数据流

	字符流包装、缓冲字符输出流包装、
	PrintWrite(new OutputStream(new socket(".."),"UTF-8"),true)


这是一个java做的简易的聊天室小程序，只有客户端和服务器端，客户端使用了javaSwing进行了简单的优化，看起来不是那么的枯燥。服务器端并没有进行优化，所以服务器端不能导出。


操作：

-	导入java项目：
-	更改ip和端口号，将客户端Client的socket端口号和服务器server的socket端口号保持一致
-	运行Server.java以Java Application （Alt +Shift +i+j）方式运行服务器端
	
	你会看见控制台如下所示:

	![聊天室服务器运行结果.png](https://i.loli.net/2017/08/22/599c1c08bd63e.png)
	
	解释：端口和线程池数量都再config.properties文件中定义的，可在其中直接修改

-	运行Client.java以同样的方式执行。
	
	你会看到这样的结果
	
	![聊天室客户端运行结果1.png](https://i.loli.net/2017/08/22/599c1c8b7235e.png)
	
	输入昵称回车或点击确定

	![聊天室运行结果2.png](https://i.loli.net/2017/08/22/599c1d2477c10.png)
	
	如图所示，这里输入的是minchao，则会显示这样的效果。

下面来点更骚的，在Client中直接写入服务器的固定IP，然后右击Client.java,
![exprotClinet1.png](https://i.loli.net/2017/08/22/599c1e9dc71a1.png)

选择Runnable JAR file点击下一步

![export.png](https://i.loli.net/2017/08/22/599c1ebb6eb14.png)

最后在桌面会生成聊天室客户端.jar文件，此文件在装有jre的环境的机器上是可以直接打开的。

因此你可以发给跟你同在一个网段里的计算机，让其双击进行聊天。

此聊天室，用于大型公司外网受限且内网通讯器被监听的时候。

是当初毕业初期就职于南京中软的时候写的，用于和部分同事沟通使用的。