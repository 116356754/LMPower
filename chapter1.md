* ## Mysql的安装

Mysql的安装分为：Mysql数据库的部署；Navicat For Mysql的安装和数据库的恢复三个部分组成。

### 1.Mysql的部署

* 将mysql的压缩包mysql-5.7.20-win32.zip解压到D:/mysql目录，如图所示：

![](/assets/mysql_exe.png)

![](/assets/mysql_dir.png)

* 双击运行mysql\_install.bat执行数据库的安装和密码的修改功能，创建collector数据库，如图所示：

![](/assets/mysql_install.png)

* 用Navicat For MySQL，首先创建collector数据库，然后点击右键菜单的“运行SQL文件"，导入init.sql到数据库中，完成初始化数据库工作。

![](/assets/mysql_restore.png)

### 2.ammeter\_real分区

在数据库中ammeter\_real表存储的是实时采集过来的数据，所以表的数据量比较大，可以对该表进行分区。利用Navicat工具打开collector数据库，多次执行call `Set_Partition('collector', 'ammeter_real');`该语句。

![](/assets/real_partion.png)

最后检查ammeter\_real表中的分割区的名称大于当前的日期![](/assets/mysql_partion_view.png)





