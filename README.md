# 接口文档
## 目录结构



```
InerfaceKg //主目录
│
└───activity //活动功能
│   │   logs //日志
│   │   ad.php //看广告得活动奖励
│   │   cash.php //花费超级现金得活动奖励
│   
└───Apply //代理申请功能(汉中棋牌功能)
│   │   jsapipay //公众号支付功能
│   │   recharge.php //充值房卡
│   │   roomcard.php //充值房卡
│   │   Weixinpay.php //微信支付类
│  
└───AppStore //苹果上架审核
│   │   logs //日志
│   │   AppStore.php //苹果支付类
│   │   index.php //苹果支付
│   │   send2server.php //向服务端请求奖励
│  
└───Client //客户端数据请求目录
│   │   logs //日志
│   │   activity.php //活动数据请求
│   │   agentLogin.php //代理登录
│   │   billboard.php //公告请求
│   │   checkVersion.php //安装包检查更新
│   │   downloadfile.php //请求下载安装包
│   │   gamePayconf.php //请求商城信息
│   │   getGaneList.php //获取可玩游戏列表(vv棋牌)
│  
└───common //公共目录
│   │   code.php //二维码生成接口
│   │   config.php //接口配置文件
│   │   db.php //数据库类
│   │   function.php //公共方法类
│   │   log.php //日志类
│   │   phpqrcode.php //二维码类
│  
└───conductance //微信小程序导量目录
│   │   logs //日志
│   │   allow.php //从小游戏跳出数据记录
│   │   index.php //点击小游戏图标记录
│  
└───Crontab //活动功能
│   │   logs //日志
│   │   getPlayerCount.php //在线人数记录接口
│   │   getPlayerNum.php //获取当前在线人数接口
│  
└───game //大转盘功能
│   │   logs //日志
│   │   conf.php //大转盘配置信息
│   │   getGrandRoulette.php //获取大转盘信息
│   │   getPrizeInfo.php //获取中奖信息
│   │   luckDraw.php //抽奖接口
│   │   robot_names.csv //虚拟中奖信息昵称列表
│  
└───Game_reg //游戏测试帐号注册目录
│   │   logs //日志
│   │   create.php //创建帐号接口
│   │   login.php //登录接口
│   │   tourist.php //游客登录
│  
└───headImg //头像上传功能(棋牌)
│   │   data //图像存储位置
│   │   log //日志
│   │   config.php //存储配置
│   │   HeadImg_Upload.php //头像上传接口
│  
└───ot //语音上传功能(棋牌)
│   │   data //语音存储位置
│   │   log //日志
│   │   config.php //语音配置信息
│   │   MahjongUpload.php //麻将语音上传接口
│   │   Voice_Upload.php //语音上传接口
│  
└───Sendmsg //短信功能(棋牌)
│   │   logs //日志
│   │   SendMsg.php //发送短信接口
│   │   SendMsg_notify.php //短信回调接口
│   │   SendMsg_sned2server.php //请求服务端绑定接口
│   
└───share //分享配置功能
│   │   logs //日志
│   │   getConf.php //获取配置
│   │   getOpenGId.php //获取微信群ID(已失效)
│   │   getShareConf.php //获取微信分享信息
│   │   refreshKey.php //刷新微信用户session_key
│   
└───starb //星彼岸(新马矿工项目)
│   │   logs //日志
│   │   search.php //获取用户信息接口
│   
└───subscription //订阅功能
│   │   logs //日志
│   │   get_info.php //获取订阅信息接口
│   │   get_reward.php //获取每日订阅奖励
│  
└───wx_login //注册登录功能目录
│   │   logs //日志
│   │   App_Login.php //微信App登录
│   │   errorCode.php //微信错误码说明
│   │   get_openid.php //获取微信小程序用户openid
│   │   index.php //微信公众号登录
│   │   mini_program.php //微信小程序登录
│   │   oppo.php //oppo小游戏登录
│   │   qq_player.php //qq小游戏登录
│   │   Register.php //注册类重构(未开发完)
│   │   save_info.php //保存用户信息
│   │   sign_page_code.php //微信分享跳转下载注册
│   │   starb.php //星彼岸注册
│   │   wx_attention.php //关注微信公众号奖励接口
│   │   WX_mark.php //获取微信分享参数接口
│   │   WX_saoLogin.php //微信网站扫码登录
│   │   WxApi.php //登录类
│   │   wxBizDataCrypt.php //微信小程序加解密类
│  
└───wxpay //支付功能目录
│   │   logs //日志
│   │   app.php //微信app支付
│   │   code.php //微信扫码支付
│   │   h5.php //微信h5支付
│   │   jsapi.php //微信公众号支付
│   │   notify.php //微信支付回调地址
│   │   qq.php //qq小游戏支付验证
│   │   starb.php //星彼岸支付回调
│   │   starb_pay.php //星彼岸礼包购买回调
│   │   starb_three_pay.php //星彼岸第三方支付回调
│   │   qq.php //qq小游戏支付验证
│   │   test.php //支付测试地址
│   │   Weixinpay.php //支付类
```

## 接口详解
### 活动功能
#### /IntefaceKg/activity/ad.php
##### 说明：通过观看广告获得活动奖励
##### 参数
键值|是否必须|说明
---|:--:|---
playerid|是|玩家ID
serverid|是|服务器ID
activityid|是|活动ID
##### 正常返回
`{code: 0, msg: "操作成功"}`
##### 返回说明
键值|说明
---|---
code|结果码,0表示成功
msg|返回提示


#### /IntefaceKg/activity/cash.php
##### 说明：通过消耗超级现金获得活动奖励
##### 参数
键值|是否必须|说明
---|:--:|---
playerid|是|玩家ID
serverid|是|服务器ID
activityid|是|活动ID
##### 正常返回
`{code: 0, msg: "操作成功"}`
##### 返回说明
键值|说明
---|---
code|结果码,0表示成功
msg|返回提示

### 苹果应用审核功能
#### /IntefaceKg/AppStore/index.php
##### 说明：苹果支付功能
##### 参数
键值|是否必须|说明
---|:--:|---
playerid|是|玩家ID
serverid|是|服务器ID
apple_receipt|是|苹果支付凭证
##### 正常返回
`{status: true, message: "购买成功"}`
##### 返回说明
键值|说明
---|---
status|支付结果
message|返回提示

### 客户端数据请求接口
#### /IntefaceKg/Client/activity.php
##### 说明：活动数据请求接口
##### 参数
键值|是否必须|说明
---|:--:|---
playerid|是|玩家ID
serverid|否|服务器ID
##### 正常返回
```
[{
	"id": 140,
	"start": 1550505600000,
	"end": 1550591999000,
	"type": 1,
	"paytype": 2,
	"title": "传奇卡片",
	"package": {
		"56": 1
	},
	"limit": 1,
	"ad_num": 10,
	"content": "活动期间,看广告10次得运输车传奇卡片,限1次",
	"num": 0,
	"get_num": 0
}]
```
##### 返回说明
键值|说明
---|---
id|活动ID
start|活动开始时间戳
end|活动结束时间戳
type|活动类型(0:跳转商店活动,1:模板1,2:模板2,3:模板3,99:限时礼包)
paytype|领奖方式(0:跳转商店,1:现金支付,2:看广告,3:超级现金)
title|活动标题
package|活动奖励列表,例：{"商品1":商品1数量,"商品2":商品2数量}
limit|活动可参与次数
ad_num|需要看几次广告可得(当paytype为2时有效)
content|活动内容
num|当前看了几次广告(当paytype为2时有效)
get_num|领了几次活动奖励

#### /IntefaceKg/Client/agentLogin.php
##### 说明：通过微信授权登录代理后台(棋牌代码)
##### 参数
键值|是否必须|说明
---|:--:|---
state|是|公众号Appid
code|是|微信登录获取的code
##### 调用成功则跳转后台

#### /IntefaceKg/Client/billboard.php
##### 说明：获得公告信息
##### 正常返回
```
[{
	"time": 1538222493,
	"type": 0,
	"popup": "0",
	"title": "\u5ba2\u670d\u5fae\u4fe1",
	"url": "https:\/\/wxgame.gzqidong.cn\/kg\/Upload\/Billboard\/5a6i5pyN5b6u5L+himage0type1316379580.png"
}]
```
##### 返回说明
键值|说明
---|---
time|创建时间
type|公告类型(0:图片,1:网页)
popup|是否自动弹出(0:不弹出,1:弹出)
title|公告名
url|公告图链接

#### /IntefaceKg/Client/checkVersion.php
##### 说明：安装包检查更新
##### 参数
键值|是否必须|说明
---|:--:|---
pf|是|安装包类型(ios,android)
version|是|客户端安装包版本号
mode|是|是否测试(0:正式,1:测试)
chl|是|安装包渠道
serverid|是|服务器ID
##### 正常返回
```
{
	"code": 0,
	"msg": "",
	"data": {
		"version": "1.0.0",
		"url": "http:\/game.gzyizhong.cn\/InterfaceKg\/Client\/downloadfile.php?pf=ios&chl=yxx&debug=0&serverid=ww02"
	}
}
```
##### 返回说明
键值|说明
---|---
code|结果码，0:表示成功
msg|返回提示
data|返回结果(version:安装包最新版本号,url:请求下载地址)

#### /IntefaceKg/Client/downloadfile.php
##### 说明：安装包下载接口
##### 参数
键值|是否必须|说明
---|:--:|---
pf|是|安装包类型(ios,android)
version|是|客户端安装包版本号
dubug|是|是否测试(0:正式,1:测试)
chl|是|安装包渠道
serverid|是|服务器ID
##### 请求成功则直接下载安装包

#### /IntefaceKg/Client/gamePayconf.php
##### 说明：安装包下载接口
##### 参数
键值|是否必须|说明
---|:--:|---
playerid|是|玩家ID
serverid|是|服务器ID
##### 正常返回
```
[{
	"pid": 1,
	"price": 6,
	"num": 0,
	"buytype": 1,
	"buy": 60,
	"icon": 1,
	"serverid": "ww02",
	"buylimit": 0,
	"day_num": 0,
	"day_limit": 0,
	"start": 1537545600,
	"end": 1537804799,
	"gift": 6
}, {
	"pid": 19,
	"price": 0,
	"num": 1,
	"buytype": 3,
	"buy": 0,
	"icon": 1,
	"serverid": "ww02",
	"buylimit": 1,
	"day_num": 0,
	"day_limit": 0,
	"content": {
		"6": 1,
		"31": 1
	},
	"star": "6"
}, {
	"pid": 8,
	"price": 6,
	"num": 1,
	"buytype": 2,
	"buy": 0,
	"icon": 1,
	"serverid": "ww02",
	"buylimit": 0,
	"day_num": 0,
	"day_limit": 0,
	"content": {
		"5": 1,
		"8": 1,
		"11": 1
	},
	"star": "10"
}, {
	"pid": 14,
	"price": 2,
	"num": 0,
	"buytype": 4,
	"buy": 0,
	"icon": 1,
	"serverid": "ww02",
	"buylimit": 0,
	"day_num": 1,
	"day_limit": 1,
	"start": 1550562140,
	"end": 1550562140,
	"gift": 0,
	"content": {
		"61": 1
	},
	"star": "0"
}]
```
##### 返回说明
键值|说明
---|---
pid|商品id
price|商品价格
num|购买次数限制(0:没有次数限制)
buytype|购买类型(1:超级现金,2:新手礼包,3:首充礼包,4:节日礼包,5:荣誉币,6:订阅功能)
buy|超级现金数量
icon|商品图标编号
serverid|服务器ID
buylimit|还可以购买几次
day_num|每日可购次数制(0:没有次数限制)
day_limit|当天还可以买几次
start|开始时间戳，当buytype为1时表示活动期间赠送超级现金，不为1时表示商品在活动期间内发售
end|结束时间戳，当buytype为1时表示活动期间赠送超级现金，不为1时表示商品在活动期间内发售
gift|赠送的超级现金数量
content|礼包包含的物品列表，例：{"商品1":商品1数量,"商品2":商品2数量}
star|当矿层开启到几星开启(矿工游戏)
starb|星彼岸支付ID

#### /IntefaceKg/Client/getGameList.php
##### 说明：根据渠道获得游戏列表(棋牌)
##### 参数
键值|是否必须|说明
---|:--:|---
chl|是|渠道
##### 正常返回
`{code: 0, msg: "操作成功",data:{list:[1,2,3,4,5],default:[1,2,3,4]}}`
##### 返回说明
键值|说明
---|---
code|结果码,0表示成功
msg|返回提示
data|list:游戏列表,default:默认游戏列表

### 公共功能
#### /IntefaceKg/common/code.php
##### 说明：根据渠道获得游戏列表(棋牌)
##### 参数
键值|是否必须|说明
---|:--:|---
data|是|二维码内容
##### 正常返回
二维码图片

### 在线人数统计
#### /IntefaceKg/Crontab/getPlayerCount.php
##### 说明：记录在线人数

#### /IntefaceKg/Crontab/getPlayerNum.php
##### 说明：输出在线人数

### 大转盘功能
#### /IntefaceKg/game/getGrandRoulette.php
##### 说明：获取大转盘信息
##### 参数
键值|是否必须|说明
---|:--:|---
playerid|是|玩家ID
serverid|是|服务器ID
##### 正常返回
```
{
	"product": [{
		"productid": 45,
		"num": 1
	}, {
		"productid": 11,
		"num": 1
	}, {
		"productid": 36,
		"num": 1
	}, {
		"productid": 49,
		"num": 1
	}, {
		"productid": 5,
		"num": 1
	}, {
		"productid": 11,
		"num": 1
	}, {
		"productid": 37,
		"num": 1
	}, {
		"productid": 43,
		"num": 1
	}],
	"gift": {
		"num": 26,
		"giftid": 48,
		"limit": 30
	},
	"consume": 100,
	"free": 0,
	"max": 60,
	"day_limit": 60,
	"share": 60,
	"share_limit": 60
}
```
##### 返回说明
键值|说明
---|---
product|转盘物品列表,{"productid": 物品ID,"num": 物品数量}
gift|赠送物品,{"num": 当前抽了几次,"giftid": 赠送的物品ID,"limit": 抽多少次赠送}
consume|物品消耗超级现金数量
free|用户免费抽取次数
max|每日最多抽取多少次
day_limit|当天还可以抽几次
share|当天剩余看广告抽奖或分享抽奖的次数
share_limit|每日看广告抽奖或分享抽奖的次数

### 游戏测试帐号注册功能
#### /IntefaceKg/Game_reg/create.php
##### 说明：根据account创建游戏帐号
##### 参数
键值|是否必须|说明
---|:--:|---
playerid|是|玩家ID
serverid|是|服务器ID
account|是|游戏帐号
chl|否|用户渠道
upplayerid|否|上级玩家ID
aid|否|代理ID
##### 正常返回
`{msg: 0,playerid: 100001, account: "test01"}`
##### 返回说明
键值|说明
---|---
code|结果码,0表示成功
msg|返回提示

#### /IntefaceKg/Game_reg/login.php
##### 说明：系统自动创建游戏帐号
##### 参数
键值|是否必须|说明
---|:--:|---
playerid|是|玩家ID
serverid|是|服务器ID
chl|否|用户渠道
upplayerid|否|上级玩家ID
aid|否|代理ID
##### 正常返回
`{msg: 0,playerid: 100001, account: "test01"}`
##### 返回说明
键值|说明
---|---
code|结果码,0表示成功
msg|返回提示

#### /IntefaceKg/Game_reg/tourist.php
##### 说明：系统自动创建游客帐号
##### 参数
键值|是否必须|说明
---|:--:|---
playerid|是|玩家ID
serverid|是|服务器ID
chl|否|用户渠道
upplayerid|否|上级玩家ID
aid|否|代理ID
##### 正常返回
`{msg: 0,playerid: 100001, account: "test01"}`
##### 返回说明
键值|说明
---|---
code|结果码,0表示成功
msg|返回提示

