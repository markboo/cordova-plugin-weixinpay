# cordova-plugin-wxpay

微信APP支付cordova,ionic插件(Android版，Ios版)


# 安装本插件

$ cordova plugin add https://github.com/ijry/cordova-plugin-wxpay.git

# 删除本插件：

$cordova plugin rm com.qdc.plugins.wxpay




# JS调用说明

* 事先前调用后台预支付API生成订单数据及签名数据
* 调用plugin的JS方法【wxpay.payment】进行支付

```js
	**wxpay.payment(json, cb_success, cb_failure);**
	# 参数说明：格式为JSON格式
	# cb_success:调用成功回调方法
	# cb_failure:调用失败回调方法
	{
	appid: 公众账号ID
	noncestr: 随机字符串
	package: 扩展字段
	partnerid: 商户号
	prepayid: 预支付交易会话ID
	timestamp: 时间戳
	sign: 签名
	}
	注：订单总金额，只能为整数，单位为【分】，参数值不能带小数。
```
