# ChromeAutoUpdate
一个自动更新chrome的小工具

第一次使用的时候会下载chrome最新版，需要稍微等待。

360会有各种提示，卸载360即可[doge]。

打开桌面快捷方式时，会检测更新，然后就会关闭自己，没有驻留进程，也不会开机自动。

会根据你的操作系统，自动选择32位、64位版chrome。

每次更新，均在你下次重新启动chrome生效。

目前是测试版，功能还不齐全，每天都会更新添加功能。

注意:本工具不支持xp。

bug反馈联系微博@你的档案。

主页:http://chrome.wbdacdn.com/

#更新原理
请求更新接口，下载chrome新版安装包，解压覆盖。

#更新日志
1.11.1.17:支持升级默认安装的chrome(如果安装在系统目录，会申请管理员权限)，也可以修改配置文件定义chrome安装路径。

1.11.5.18:增加下载超时处理，增加更新渠道默认参数，添加多地址下载支持，解决部分网络用户无法更新。

1.11.6.23:默认保存chrome到安装目录，不和原有chrome冲突

1.11.16.21:判断chrome安装目录是否存在，解决第一次使用的时候，由于目录不存在，导致程序无法响应。

#配置文件

[server]

update_url=http://chrome.wbdacdn.com/update.php             #主程序升级接口

app_update_url=http://chrome.wbdacdn.com/app_update.php     #chrome升级接口

[config]

version=4      #配置文件版本，请勿修改

[app]

index=         #默认打开页面

Params=        #启动chrome的参数

user_agent="Mozilla/5.0(Windows NT 10.0; Win64; x64) AppleWebKit/537.36(KHTML, like Gecko) Chrome/56.0.2902.0 Safari/537.36"

path=C:\soft\ChromeAutoUpdate\ #chrome安装目录，需要 \ 结尾

Channel=dev   #取值 'Stable','Beta','Dev','Canary'
