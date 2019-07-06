快速入门
=========================

下面以mac系统为例，介绍以SIoT为MQTT服务器，掌控板板为智能终端，搭建一个最简单的物联网数据采集系统。

运行SIoT系统：
----------------------

双击运行SIoT_mac，将看到一个黑色的CMD窗口，不要关闭它。

.. image:: ../image/setup/02_run_02.png


编写程序（mPythonX）
--------------------------------

打开mPythonX，编写如下代码。

.. image:: ../image/setup/04_quick_05.png

**说明**：

  -  请确保掌控板和电脑连接的是同一个无线路由器，可以相互访问。
  -  “mpythonx/001”表示项目名称为“mpythonx”，设备名称为“001”。
  -  服务器地址就是运行siot的电脑的ip地址，可以运行cmd，输入ipconfig获取

给掌控板写入程序并且运行。

重新启动掌控板，等屏幕显示IP地址后，是否会出现“mqtt-ok”。


Web管理
----------------------

打开网址：localhost：8080（或者使用电脑的IP地址）。

输入用户名“siot”和密码“dfrobot”，就可以看到项目列表中多了"yy"

在名称为“yy”设备消息中，当按下“A”键时，在网页端就可以接收到“0”，按下“B”键，可以接收到“1”。

.. image:: ../image/setup/04_quick_06.png

在名称为“yy”设备消息中，当发送“01”时，就可以控制掌控板的红灯亮；发送“02”时，就可以控制掌控板亮绿灯；发送“03”时，控制掌控板亮蓝灯；发送“00”，控制掌控板灯熄灭。

.. image:: ../image/setup/04_quick_07.png

故障排查
---------------------

如果接收不到数据，请关闭运行SIoT服务器的电脑的各种病毒防火墙或者网络防火墙（安全卫士）。

在其他电脑使用mqtt的工具测试SIoT，推荐MqttTool（一个测试mqtt的软件，只有100k不到。）

- GitHub地址：https://github.com/vvlink/SIoT/tree/master/MQTT%20tools/Mqtttool
- 下载地址：https://github.com/vvlink/SIoT/tree/master/MQTT%20tools/Mqtttool

