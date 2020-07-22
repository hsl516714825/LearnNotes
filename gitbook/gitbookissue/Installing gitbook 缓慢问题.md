# Installing gitbook 缓慢问题

##### 问题描述：

执行 gitbook -V ，显示： Installing GitBook 3.2.3 .......，之后一直处于等待状态，在任务管理器中查看到nodejs在运行状态，但是cpu占有率处于一个很低的状态，且时有时无。

##### 问题分析：

npm 默认使用安装使用的国外镜像，所以速度较慢。

##### 解决方案：

使用国内的镜像。

采用淘宝的镜像：

方法1：在命令窗口输入

```shell
npm config set registry=http://registry.npm.taobao.org -g
```

方法2：在[nodejs安装目录]/node_modules/npm中，打开npmrc，然后添加配置

```ini
registry=http://registry.npm.taobao.org
```



##### 说明：

参考一下站址：

- [gitbook安装中installing gitbook xxx 时间过长的问题](https://blog.csdn.net/qq_39482771/article/details/89436833)
- [解决安装gitbook时卡顿在 Installing GitBook 3.2.3 的问题](http://www.blogdaren.com/post-2567.html)