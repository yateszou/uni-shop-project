# uni-shop-project
基于uniapp开发的一个商场+项目

运行第一步首先下载后台支持以及api接口，地址：链接：https://pan.baidu.com/s/1jDFHsPC_dvjwXYW8YDwCtA 提取码：0909 

第一步：将接口保存到本地服务器，这里建议用phpstudy搭建一个本地服务器，数据库名一定要和表名一样，自定义得去另行配置，这里不详说
![image](https://s1.ax1x.com/2020/09/16/wcxMpn.png)

第二步：导入表到数据库中，提示：字符集记得选择utf-8

第三步：在下载的文件夹里鼠标右键打开Powershell，如果没有Powershell，就按住shift+鼠标右键，就会出现了，之后命令行下载依赖：npm install

![image](https://s1.ax1x.com/2020/09/16/wgS0eK.png)

![image](https://s1.ax1x.com/2020/09/16/wgSasx.png)

下载完成之后进入src目录，输入命令：node app.js 提示：如果出现请求失败，那么就去app.js里设置一下数据库密码，然后再：node app.js

![image](https://s1.ax1x.com/2020/09/16/wgSdL6.png)

然后接口就可以正常请求了

