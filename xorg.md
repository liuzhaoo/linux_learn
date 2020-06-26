### 远程桌面的配置

这几天配置了实验室的服务器用来做深度学习，装了ubuntu20.04. 实验室人比较多，所以考虑配置远程桌面，本来对此一窍不通，上网查询后了解到XRDP比较快便采用此方法。



网上有很多教程，这里提供一个十分简便的方法：使用国外大神的一个脚本，他把所有的安装命令集成到了一起，目前已支持20.04。

[下载压缩包](https://github.com/liuzhaoo/linux_learn/releases/tag/xrdp)(xrdp-install-1.2.zip)后解压，按以下命令操作：

> ```
> chmod +x  ~/Downloads/xrdp-installer-1.2.sh
> # 赋予文件执行权限
> ```

- 注意路径指定为自己文件的位置

然后执行标准安装：

```
 ./xrdp-installer-1.2.sh
```

其中，有很多自定义安装选项，可以自己去看： 

http://c-nergy.be/blog/?p=14888

脚本执行完毕就可以进行远程桌面连接了，推荐使用windows自带远程连接，输入服务器即可连接，进入登录界面后输入ubuntu用户名就可以登陆成功啦！

记录几个常用命令：



>``` 
># 验证xrdp是否正在运行：
>sudo systemctl status xrdp
>
># 重启xrdp服务
>sudo service xrdp restart
>```



### 安装后登陆蓝屏的情况

我在按以上方法安装之后，打开windows的远程桌面可以输入服务器地址并进入登录页面，但是输入用户名和密码后便开始了长时间的蓝屏。

其实这种情况是登陆成功了的，但是桌面加载出了问题，我又找到这位大神的其他脚本，执行就可以解决问题！

下载地址：https://github.com/liuzhaoo/linux_learn/releases/tag/xrdp （install-xrdp-3.0.zip）

执行步骤和上面一样，先赋予权限，然后执行：

>```
>chmod +x  ~/Downloads/install-xrdp-3.0.sh
>
>./install-xrdp-3.0.sh
>```

- 注意对应自己路径

最后，附上来源：

http://c-nergy.be/blog/?p=14888

http://c-nergy.be/blog/?p=13663