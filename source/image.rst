
.. _image:

===============
青云映像(Image)
===============

*EMQ* 消息服务器1.1.2版本正式登陆 `青云`_ 映像市场，用户可直接创建映像启用EMQ消息服务器:

.. image:: ./_static/images/imagemarket.png

映像属性
--------

+--------------+---------------------------------------------------+
| 属性         | 值                                                |
+--------------+---------------------------------------------------+
| 名称         | EMQTT Ubuntu映像-百万级分布式物联网MQTT消息服务器 |
+--------------+---------------------------------------------------+
| 费用         | 免费                                              |
+--------------+---------------------------------------------------+
| 类别         | 物联网                                            |
+--------------+---------------------------------------------------+
|              | 百万级连接和分布式集群，发布订阅模式的开          |
| 摘要         | 源MQTT消息服务器。完整支持MQTT、MQTT-SN、         |
|              | CoAP等物联网协议。                                |
+--------------+---------------------------------------------------+
| 开发者       | feng@emqtt.io                                     |
+--------------+---------------------------------------------------+
| 提交时间     | 2016-07-11                                        |
+--------------+---------------------------------------------------+
| 更新时间     | 2016-07-11                                        |
+--------------+---------------------------------------------------+

映像描述
--------

1. 该映像基于EMQTT 1.1.2版本创建，启动后MQTT服务器监听在TCP 1883端口；

2. EMQTT服务器WEB控制台，端口18083。默认管理员: admin, 密码: public，映像启动后请登录控制台修改默认密码；

3. 映像默认没有开启MQTT认证，允许MQTT客户端匿名登录；

4. EMQTT程序部署在/opt/emqttd/目录，用户可通过配置etc/emqttd.config或加载插件方式，开启HTTP、PostgreSQL、MySQL、Redis、MongoDB等多种认证方式；

5. EMQTT消息服务器详细配置和使用，请参考文档: http://emqtt.com/docs/

本映像由emqtt.com与青云共同提供技术支持，用户QQ群组: 196066320

映像当前版本
------------

映像包含组件:

1. Erlang/OTP 18.3版本环境

2. EMQTT 1.1.2版本

映像配置说明:

1. 防火墙开启1883(MQTT)、8083(WebSocket)、18083(Dashboard控制台)端口。

2. Dashboard控制台, 端口18083。默认管理员: admin, 密码: public，映像启动后请立即修改密码！

3. 映像默认允许1万线MQTT连接，最大可配置到10万线。

4. 映像内存占用: 5万连接/1G内存。请用户根据MQTT消息吞吐量调整内存。

EMQTT手工启停
-------------

.. code::

    systemctl start emqttd
    systemctl stop emqttd

.. _青云: https://www.qingcloud.com

