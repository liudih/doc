
## 如何禁用媒体音量控制弹出窗口[永久]

chrome://flags/


media key 禁用

## win10 关闭 AeroShake


gpedit.msc

“用户配置–管理模板–桌面”，在右侧找到并双击“关闭Aero Shake窗口最小化鼠标手势”

## 删除我的电脑的文件夹图标

在注册表中，找到

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\MyComputer\NameSpace项


找到项：

视频：{f86fa3ab-70d2-4fc7-9c99-fcbf05467f3a}

图片：{24ad3ad4-a569-4530-98e1-ab02f9417aa8}

文档：{d3162b92-9365-467a-956b-92703aca08af}

下载：{088e3905-0323-4b02-9826-5d99428e115f}

音乐：{3dfdf296-dbec-4fb4-81d1-6a3438bcf4de}

桌面：{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}

3D对象：{0DB7E03F-FC29-4DC6-9020-FF41B59E513A}



删除 ！

## win10 到期时间查询

// 运行输入：
Slmgr.vbs -xpr


// bat批处理文件如下： 
:: cmd /k 不关闭窗口 cmd /c 关闭窗口
cmd /c Slmgr.vbs -xpr

## WIN10删除远程连接记录方法

1、我的文档里 一个隐藏文件 搜 default.rdp  删除
2、注册表  regedit  -> HKEY_CURRENT_USER \ Software\Microsoft \ Terminal Server Client \ Default  删除记录

## WIN10删除文件提示找不到项目

创建 del.bat 
内容：
DEL /F /A /Q \\?\%1
RD /S /Q \\?\%1


文件拖入 del.bat

##  删除office2016最近记录

word:

文件 ->  选项  -> 高级 -> 显示 ->
显示此数目的“最近使用的文档”(R):   25    // 这里修改为0

excel:

文件 ->  选项  -> 高级 -> 显示 ->
显示此数目的“最近使用的工作簿”(R):   25    // 这里修改为0

regedit:

清空注册表数据
> 计算机\HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Excel\File MRU

> 计算机\HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Excel\Place MRU

> 计算机\HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Word\File MRU

> 计算机\HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Word\Place MRU

> 计算机\HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Word\Reading Locations

gpedit.msc:

设置启用：
用户配置 -> 管理模板 -> “开始”菜单和任务栏：
- 退出系统时清除最近打开的文档的历史
- 为新用户清除最近的程序列表
- 从“开始”菜单中删除“最近添加”列表
- 不保留最近打开文档的历史
- 从“开始”菜单中删除“最近使用的项目”菜单

