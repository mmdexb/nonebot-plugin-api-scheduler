# 面板
面板地址：your_ip_address:8080/dashboard 
账号：请在插件源码中authenticate函数设置
密码：请在插件源码中authenticate函数设置
## Scheduler Timer 定时任务
何时发送任务：需要输入格式为 YYYY-MM-DD HH:MM:SS的时间戳，任务将会在此时间执行一次
Content：输入需要发送的文字内容
Image Url：输入需要发送的图片的网络地址（能够在公网访问到）
QQ Group Id：输入信息发送到的QQ群号 （机器人需已加入该群）
Is At All：勾选后，信息将艾特全体成员。（机器人需有管理员权限）
点击Get Scheduler Timer后，任务将发送到机器人。


### 使用范例
何时发送任务：2024-10-24 15:00:00
Content：这是一条测试性信息
ImageUrl：https://img.picui.cn/free/2024/10/24/6719eeabae889.png
QQ Group Id：717742522 
Is At All：勾选

若正确执行，机器人将会在2024年10月24日的15时0分0秒向群号为717742522内发送“这是一条测试性信息 [图片]”并艾特全体成员。



## Scheduler Plan 计划任务
每隔几天发送一次：输入两次发送间隔的天数（此项大于0，1为每天发送，2为每2天发送，以此类推）
几时、几分、几秒：按需求填写。正确填写后，机器人将在应当发送的当天的x时y分z秒发送信息。
Content：输入需要发送的文字内容
Image Url：输入需要发送的图片的网络地址（能够在公网访问到）
QQ Group Id：输入信息发送到的QQ群号 （机器人需已加入该群）
Is At All：勾选后，信息将艾特全体成员。（机器人需有管理员权限）
点击Get Scheduler Plan后，任务将发送到机器人。

### 使用范例
每隔几天发送一次：1
几时：14 几分：00 几秒：00
Content：现在时间是14:00:00
ImageUrl：留空
QQ Group Id：717742522 
Is At All：勾选

若正确执行，机器人将在每天的14时整向群号为717742522发送信息“现在时间是14:00:00”并艾特全体成员。
值得注意的是，若当前时间为14:00:00以前，上面的例子也会在当天的14:00:00执行发送操作。


## Cancel Scheduler Job 取消定时任务
输入任务ID，点击按钮，则会取消定时任务。


## List Scheduler Jobs 任务列表
面板进入后，将会获取一次任务列表。你也可以点击List Jobs按钮实现手动刷新。

Job ID：任务的唯一ID，由系统自动分配。
name：调用的机器人功能
next_run_time	: 下一次执行的时间
trigger	: 定时信息
send_to	:目标群号
send_what：发送内容

