#### 删除thinclient_drivers

在使用远程桌面的时候，系统会自动加载一个thinclient_drivers,在用户主目录下。如图：



<img src="/home/lzhao/thinclient_drives/H:/Snipaste_2020-06-26_16-01-04.png" alt="Snipaste_2020-06-26_16-01-04" style="zoom:60%;" />

在删除用户时，若选择保留文件，除了用户目录下其他文件，这个文件也会保留下来。此时再想删除就会提示这是一个目录，无法删除，使用 ```rm -rf  ``` 命令也不行

因为它是作为驱动器挂载在目录下的，只要卸载就可以了 ：

```umount -fl thinclient_drivers```

-f 是强行卸载，若直接umount，会提示target is busy



卸载后，文件就可以正常删除了



