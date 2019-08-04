## 请求响应 RAW
**Request:**
```http
POST https://qc.can-dao.com:7776/SecretAction?_actionName=userInfo&key=e885c1b0a4a3229a HTTP/1.1
Host: qc.can-dao.com:7776
Accept: */*
Content-Type: application/json
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Cookie: JSESSIONID=08677145-59d1-42e2-a6b4-f67dd89a7a8f
User-Agent: Mozilla/5.0 (iPhone; CPU iPhone OS 13_0 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E148 MicroMessenger/7.0.5(0x17000523) NetType/WIFI Language/zh_CN
Referer: https://servicewechat.com/wx5ffe69568d6a0d03/0/page-frame.html
Content-Length: 53
Accept-Language: zh-cn

{"actionName":"candao.user.getBaseInfo","content":{}}
```

**Response:**
```http
HTTP/1.1 200 OK
Server: Tengine/2.1.2
Date: Sun, 28 Jul 2019 16:46:31 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 301
Connection: keep-alive
Access-Control-Allow-Origin: *
Set-Cookie: wxa_V1_secretKey=DB7EgYkUnaT/bfVoUty855bsoNad9AKsAvpDiYG8utk=; path=/; expires=Wed
Set-Cookie:  31-Jul-2019 16:49:53 GMT; HttpOnly
Set-Cookie: wxa_V1_autoLogin=luyg1p30AqwC+kOJgby62Q==; path=/; expires=Thu
Set-Cookie:  01-Dec-1994 16:00:00 GMT; HttpOnly

{"status":1,"msg":"操作成功","data":{"uid":40894,"userName":"d6129b7ec54d4230","nickName":"13143345615","sex":0,"phone":"13143345615","canAlterPasswd":false,"canAlterUname":true,"cityId":0,"platformKey":"e1d122204769b9d9"},"logId":"f3219e3b-b63b-44c1-a2b8-180892da3be7","serverTime":1564332593319}
```

## Pinpoint Agent 收集到的数据
[点击查看 Pinpoint Agent 数据来源](http://qc.can-dao.com:6787/proxy_pass/#/transactionList/FRONT-candao-wxa@RESIN/20m/2019-07-29-01-00-00/HWY-119.3.4.13%5E1564135311682%5E391-1564332892181-18)
### 调用链路 Call Tree
![Call Tree](/img/analysis/businesslayer/SecretAction/img-1.png)

### 服务调用拓补图 Server Map
![Server Map](/img/analysis/businesslayer/SecretAction/img-2.png)

## 手动关联 Call Tree 的链路关系
[Call Tree](http://qc.can-dao.com:6787/proxy_pass/#/transactionList/HWY-api-gateway@RESIN/10m/2019-07-29-00-55-00/HWY-10.233.33.4%5E1564316313727%5E75134-1564332892175-5)

![Server Map](/img/analysis/businesslayer/SecretAction/img-3.png)
![Call Tree](/img/analysis/businesslayer/SecretAction/img-4.png)
