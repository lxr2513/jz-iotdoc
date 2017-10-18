# 获取设备列表

```js
GET /v1/application/devices?appeui=1616161616161616&token=79e5300eed5845c5a5136862477f0760
```

## 请求参数

| **字段名称** | **字段说明** | **类型** | **必填** |
| :---: | :---: | :---: | :---: |
| appeui | 应用eui 64字符串 | string | Y |
| token | 用户token，用于对请求进行鉴权 | string | Y |
| limit | 用于翻页，分页请求返回的记录条数 | number | Y |
| offset | 用于翻页，分页请求返回的起始位置 | number | Y |

## 响应参数

| **字段名称** | **字段说明** | **类型** | **必填** |
| :---: | :---: | :---: | :---: |
| appeui | 设备所属app的EUI | string | Y |
| deveui | 设备eui | string | Y |
| lastact | 设备最后活动时间 | string | Y |
| type | 设备类型 | string | Y |
| name | 设备名称 | string | Y |
| city | 所在城市 | string | Y |
| area | 所在区域 | string | Y |
| address | 详细地址 | string | Y |
| lat | 所在纬度 | string | Y |
| lng | 所在经度 | string | Y |
| createAt | 创建时间 | string | Y |

## JSON对象实例

```js
{
    "list": [
        {
            "address": "",
            "appeui": "2326232656262656",
            "area": "",
            "city": "",
            "createdAt": "2017-02-12 13:22:42",
            "deveui": "0000154156656263",
            "lastact": 1482981405,
            "lat": "",
            "lng": "",
            "name": "222",
            "type": ""
        }
        ...
    ]
    "more": boolean; // 是否有更多记录
}
```



