# sapnwrfcsdk
sap nwrfcsdk 7.2  include the win32, win64, linux x64. and sapcar.exe is win64.

# how to use the sar file( the command):
sapsar -xvf XXX.sar


第一步：安装版本库 nwrfcsdk.zip

vi /etc/ld.so.conf.d/nwrfcsdk.conf
## 输入以下内容
/usr/sap/nwrfcsdk/lib
:wq 保存退出

## 使配置生效
ldconfig

https://php7-sapnwrfc.readthedocs.io/zh/latest/building.html
第二部：源码编译
$ git clone https://github.com/gkralik/php7-sapnwrfc.git
$ cd php7-sapnwrfc
$ phpize
$ ./configure
$ make
$ sudo make install

在 php.ini 中增加一行
extension=sapnwrfc.so
重启