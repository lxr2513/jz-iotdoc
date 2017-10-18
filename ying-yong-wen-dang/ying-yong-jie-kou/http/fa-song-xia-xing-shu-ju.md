# 发送下行数据

```
POST /v1/application/downdata?deveui=1616161616161616&token=79e5300eed5845c5a5136862477f0760&port=2&datatype=0&data=123abc
```

## 请求参数

| **字段名称** | **字段说明** | **类型** | **必填** |
| :---: | :---: | :---: | :---: |
| deveui | device EUI64字符串。deveui必须二选一device EUI64字符串。deveui必须二选一 | string | Y |
| token | 用户token，用于对请求进行鉴权 | string | Y |
| port | 设备传输数据的端口 | number | Y |
| datatype | 数据类型0：hex数据，1：普通字符串 | number | Y |
| data | 要发送的数据。datatype 为0时发送hex数据；为1时发送普通字符串 | string | Y |

## 响应参数

| **字段名称** | **字段说明** | **类型** | **必填** |
| :---: | :---: | :---: | :---: |
| code | 编号 | string | Y |
| message | 信息 | string | Y |

## JSON对象实例

```js
{
    "code": "success",
    "message": "ok"
}
```



