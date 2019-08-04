## 请求响应 RAW
**Request:**
```http
POST https://qc.can-dao.com:7776/Action?_actionName=cityList&key=e885c1b0a4a3229a HTTP/1.1
Host: qc.can-dao.com:7776
Accept: */*
Content-Type: application/json
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Cookie: JSESSIONID=08677145-59d1-42e2-a6b4-f67dd89a7a8f
User-Agent: Mozilla/5.0 (iPhone; CPU iPhone OS 13_0 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Mobile/15E148 MicroMessenger/7.0.5(0x17000523) NetType/WIFI Language/zh_CN
Referer: https://servicewechat.com/wx5ffe69568d6a0d03/0/page-frame.html
Content-Length: 66
Accept-Language: zh-cn

{"actionName":"candao.storeStandard.getOpenCityList","content":{}}
```

**Response:**
```http
HTTP/1.1 200 OK
Server: Tengine/2.1.2
Date: Sun, 28 Jul 2019 16:46:32 GMT
Content-Type: application/json; charset=utf-8
Content-Length: 344
Connection: keep-alive
Access-Control-Allow-Origin: *

{"status":1,"msg":"操作成功","logId":"67da5608-42d7-4b43-8828-f1da99842657","data":[{"cityId":729,"provinceId":729},{"cityId":0,"provinceId":0},{"cityName":"合肥市","cityId":11379,"provinceName":"安徽省","provinceId":729},{"cityName":"广州市","cityId":11478,"provinceName":"广东省","provinceId":736}],"serverTime":1564332593621}
```

## Pinpoint Agent 收集到的数据
[点击查看 Pinpoint Agent 数据来源](http://qc.can-dao.com:6787/proxy_pass/#/transactionList/FRONT-candao-wxa@RESIN/20m/2019-07-29-01-00-00/HWY-119.3.4.13%5E1564135311682%5E394-1564332892623-35)
### 调用链路 Call Tree
![Call Tree](/img/analysis/businesslayer/Action/cityList/img-1.png)

### 服务调用拓补图 Server Map
![Server Map](/img/analysis/businesslayer/Action/cityList/img-2.png)

## 手动关联 Call Tree 的链路关系
[Call Tree](http://qc.can-dao.com:6787/proxy_pass/#/transactionList/HWY-api-gateway@RESIN/10m/2019-07-29-00-55-00/HWY-10.233.33.4%5E1564316313727%5E75151-1564332892614-23)

![Server Map](/img/analysis/businesslayer/Action/cityList/img-3.png)
![Call Tree](/img/analysis/businesslayer/Action/cityList/img-4.png)
