# 获取上行数据 {#获取上行数据}

```js
GET /v1/application/data?appeui=1616161616161616&token=79e5300eed5845c5a5136862477f0760&order=desc
```

## 请求参数 {#请求参数}

| **字段名称** | **字段说明** | **类型** | **必填** |
| :--- | :--- | :--- | :--- |
| appeui | APP EUI64字符串 | string | N/Y |
| deveui | device EUI64字符串。appeui和deveui必须二选一 | string | N/Y |
| token | 用户Token，用于对请求进行鉴权 | string | Y |
| start | 拉取数据的开始时间\(自1970零时刻以来毫秒数\) | number | N |
| end | 拉取数据的结束时间\(自1970零时刻以来毫秒数\) | number | N |
| order | 返回列表按时间的排序类型，取值\[desc，asc\]，默认asc | string | N |
| limit | 最大拉取记录数（最大1000） | number | N |

## 响应参数 {#响应参数}

| **字段名称** | **字段说明** | **类型** | **必填** |
| :--- | :--- | :--- | :--- |
| $time | 数据接收时间 | string | Y |
| appeui | APPEUI 64字符串 | string | Y |
| bandwidth | 带宽 | number | Y |
| data | 包内容（按HEX格式编码） | string | Y |
| deveui | 设备eui 64位字符串 | string | Y |
| fcnt | 包计数器 | number | Y |
| fport | LoRaWAN数据端口号（1~223），可用于区分数据类型 | number | Y |
| frequency | 无线频率 | number | Y |
| lorasnr | 信噪比 | number | Y |
| modulation | 调制方式（lora或fsk） | string | Y |
| rssi | 信号强度 | number | Y |
| spreadfactor | 扩频因子 | number | Y |

## JSON对象实例 {#json对象实例}

```py
{
    "list": [
         {
            "$time": "2017-06-06 10:10:10",
            "appeui": "2326232656262656",
            "bandwidth": 125,
            "data": "789654",
            "deveui": "0000154156656263",
            "fcnt": 1,
            "fport": 65,
            "frequency": 471900000,
            "lorasnr": 6.2,
            "modulation": "LORA",
            "rssi": -82,
            "spreadfactor": 12
        }
        ...
    ]
}
```



