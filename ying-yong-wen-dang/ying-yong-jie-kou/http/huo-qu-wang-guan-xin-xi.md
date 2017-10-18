# 获取网关信息

```py
GET /v1/application/gateways/:mac?token=1v7rwa77f89de547bd9f10ed54e4a
```

## 请求参数

| **字段名称** | **字段说明** | **类型** | **必填** |
| :---: | :---: | :---: | :---: |
| mac | 网关mac地址 | string | Y |
| token | 用户token，用于对请求进行鉴权 | string | Y |

## 响应参数

| **字段名称** | **字段说明** | **类型** | **必填** |
| :---: | :---: | :---: | :---: |
| mac | 网关MAC地址 | string | Y |
| name | 网关名称 | string | N |
| version | 网关sdk版本 | string | N |
| city | 网关所在城市 | string | N |
| area | 网关所在区域 | string | N |
| address | 网关详细地址 | string | N |
| lat | 网关所在纬度 | string | N |
| lng | 网关所在经度 | string | N |
| txpower | 网关发射功率 | number | N |
| latency | 网关链路时延（ms） | number | N |
| lastact | 网关最近接受数据时间 | string | N |
| createdAt | 网关创建时间 | string | Y |

## JSON对象实例

```js
{
    "mac": " 154156656263 ",
    "name": "XX网关",
    "city": " null ",
    "area": "",
    "address": "",
    "lat": "23.14812",
    "lng": "104.12112",
    "txpower": 17,
    "latency": 23,
    "version": "0.0.1",
    "lastact": "2017-06-23 10:32:10",
    "createAt": "2017-03-24 11:22:10"
}
```



