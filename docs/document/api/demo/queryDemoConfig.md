

**1\. DEMO查询**
###### 接口功能
> DEMO查询接口

###### URL
> [http://api.java110.com:8008/api/demo.queryDemoConfig](http://api.java110.com:8008/api/demo.queryDemoConfig)

###### 支持格式
> JSON

###### HTTP请求方式
> GET

###### 请求参数(header部分)
|参数名称|约束|类型|长度|描述|取值说明|
| :-: | :-: | :-: | :-: | :-: | :-:|
|app_id|1|String|30|应用ID|Api服务分配                      |
|transaction_id|1|String|30|请求流水号|不能重复 1000000000+YYYYMMDDhhmmss+6位序列 |
|sign|1|String|-|签名|请参考签名说明|
|req_time|1|String|-|请求时间|YYYYMMDDhhmmss|

###### 请求参数(url部分)
|参数名称|约束|类型|长度|描述|取值说明|
| :-: | :-: | :-: | :-: | :-: | :-: |
|demoName|1|String|20|用例名称|-|
|demoValue|1|String|20|用例值|-|
|page|1|-|-|分页|-|
|row|1|-|-|分页|-|

###### 返回协议

当http返回状态不为200 时请求处理失败 body内容为失败的原因

当http返回状态为200时请求处理成功，body内容为返回内容




###### 举例
> 地址：[http://api.java110.com:8008/api/demo.queryDemoConfig?page=1&row=10](http://api.java110.com:8008/api/demo.queryDemoConfig?page=1&row=10)

``` javascript
请求头信息：
Content-Type:application/json
USER_ID:1234
APP_ID:8000418002
TRANSACTION_ID:10029082726
REQ_TIME:20181113225612
SIGN:aabdncdhdbd878sbdudn898
请求报文：

无

返回报文：
 [{
 	"demoId": "965000",
 	"demoName": "测试用例",
 	"demoRemark": "测试说明",
 	"demoValue": "测试用例值",
 	"page": -1,
 	"records": 0,
 	"row": 0,
 	"statusCd": "0",
 	"total": 0,
 	"userId": "1002"
 },{
 	"demoId": "902019101816650018",
 	"demoName": "11",
 	"demoRemark": "111",
 	"demoValue": "222",
 	"page": -1,
 	"records": 0,
 	"row": 0,
 	"statusCd": "0",
 	"total": 0,
 	"userId": "30518940136629616640"
 }]

```