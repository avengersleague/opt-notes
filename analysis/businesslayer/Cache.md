## 请求响应 RAW
**Request:**
```http
POST https://qc.can-dao.com:7776/Cache?actionId=1&key=e885c1b0a4a3229a HTTP/1.1
Host: qc.can-dao.com:7776
Accept: */*
Content-Type: application/json
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Cookie: JSESSIONID=08677145-59d1-42e2-a6b4-f67dd89a7a8f
User-Agent: Mozilla/5.0 (iPhone; CPU iPhone OS 13_0 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E148 MicroMessenger/7.0.5(0x17000523) NetType/WIFI Language/zh_CN
Referer: https://servicewechat.com/wx5ffe69568d6a0d03/0/page-frame.html
Content-Length: 24
Accept-Language: zh-cn

{"cityName":"广州市"}
```

**Response:**
```http
HTTP/1.1 200 OK
Server: Tengine/2.1.2
Date: Sun, 28 Jul 2019 16:46:32 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 60
Connection: keep-alive
Access-Control-Allow-Origin: *
Set-Cookie: wxa_V1_cityName=iK4XYvpk/UagDam0a0iZNA==; path=/; expires=Wed
Set-Cookie:  31-Jul-2019 16:49:53 GMT; HttpOnly

{"status":1,"msg":"操作成功","serverTime":1564332593504}
```

## Pinpoint Agent 收集到的数据
[点击查看 Pinpoint Agent 数据来源](http://qc.can-dao.com:6787/proxy_pass/#/transactionList/FRONT-candao-wxa@RESIN/20m/2019-07-29-01-00-00/HWY-119.3.4.13%5E1564135311682%5E392-1564332892193-8)

[点击查看 Pinpoint Agent 数据来源](http://qc.can-dao.com:6787/proxy_pass/#/transactionList/FRONT-candao-wxa@RESIN/20m/2019-07-29-01-00-00/HWY-119.3.4.13%5E1564135311682%5E397-1564332893259-13)
### 调用链路 Call Tree
![Call Tree](/img/analysis/businesslayer/Cache/img-1.png)

### 服务调用拓补图 Server Map
![Server Map](/img/analysis/businesslayer/Cache/img-2.png)
