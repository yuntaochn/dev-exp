V-Rep踩坑
===

V-REP 使用过程中，遇到了许多障碍，有很多都是意料之外的，整理于下。

1. Remote API 正在逐渐废弃，建议使用b0或者b0 Remote API的方式。
b0，即BlueZero，基于zmq。
类似与TCP/IP、Redis等，但是vrep内部实现的b0似乎并不完整。

2. 在场景中添加模型时，许多模型自带有脚本，可供参考，
但是如果自己新建脚本，以使用添加的模型时，建议将自带的脚本删除或者注释掉，因为有可能会与新建的脚本冲突。

3. 格式转换
v-rep 内部API返回的数据有可能占用太多空间，以至于处理以及传输时非常耗费时间，故应现在内部进行格式转换，将其转换为buffer，可以参考API ``sim.transformbBuffer()``。

[原文](https://blog.csdn.net/mec_zhang/article/details/90443144?spm=1001.2014.3001.5502)


