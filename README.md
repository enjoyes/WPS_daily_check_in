# WPS_daily_~~check_in~~_invite

配合 WPS 打卡活动，完成每日 10 人邀请任务。

***该项目不是全自动的，需要配合微信小程序，每天在手机上进行打卡。***

---
WPS 有一个免费领会员的活动，关注微信小程序“我的WPS会员”，进入首页就可以看到。

每天 6:00-13:00 在小程序上打卡就会送 1 天 WPS 会员。
参与活动后，同时关注微信公众号“WPS会员”，该公众号会每天发微信提醒你打卡。
完成邀请任务可额外获得会员天数，每邀请一位好友可多得 1 天，每天最多邀请 10 个好友。
以防该活动结束，尽可能多嫖几天会员。

本项目的作用是**自动完成邀请好友的任务**。

# 执行步骤：
1. 添加微信小程序‘我的WPS会员’，首页参加打卡活动，进入个人中心记录数字 ID
2. 右上角 Fork 该项目
3. 在 Fork 完的该项目页面中，点击上方 Actions，开启workflow
4. 点击文件 WPS_accept_invitation.py。将第一行 'invite_userid =' 后面的数字改成自己的会员 ID，保存修改即可


# 其它
- 该项目基于 GitHub Action 功能实现

- 该项目每天早上 9 点自动运行，可能会晚个十几分钟；每次修改该项目中的任何文件也会自动执行一次
- 可在微信小程序“我的WPS会员”，‘任务’菜单->‘邀请好友’栏查看是否邀请成功（9 点以后）

---
#### 本来想做全自动打卡，但是查了 github 上其它项目后，发现打卡需要一个验证 code ，获取该 code 要调用微信内部方法 wx.login()。没办法破解，有没有大神提供其它思路。
