## 发送短信服务
|  序号  | 接口方法                         | 接口描述 |
| :--: | :--------------------------- | :--- |
|  一   | [/sms/sendSms](#sms-sendSms) | 发送短信 |
|  二   | [发送短信](#timing)              | 定时任务 |


## 发送短信服务列表


### <span id="sms-sendSms" >一、发送短信</span>
|             接口方法             | 接口描述 |
| :--------------------------: | :--- |
| [/sms/sendSms](#sms-sendSms) | 发送短信 |

#### 1、简介

```
给指定用户发送验证码；
```



#### 2、 请求参数
| 参数名称  | 必选   | 类型     | 说明       |
| :---: | :--- | :----- | -------- |
| phone | true | string | 接收短信的手机号 |
| code  | true | string | 验证码      |

---

#### 3、调用样例
```
{
"phone":"15811451620",
"code":"1234"
}
```
---

#### 4、返回结果
|   字段   | 类型     | 说明    |
| :----: | :----- | :---- |
| status | String | 返回码   |
| errmsg | String | 返回码描述 |
|  data  | json   | 数据    |

---
#### 5、JSON示例

* 请求成功数据格式：

```
{
    "status": 200,
    "errmsg": "成功",
    "data": "{\"Message\":\"OK\",\"RequestId\":\"F73090F1-C1EE-4A4C-9827-7D48647BC34B\",\"BizId\":\"317314775511634969^0\",\"Code\":\"OK\"}"
}
```
---

### <span id="timing" >二、定时任务</span>
|      接口方法       | 接口描述 |
| :-------------: | :--- |
| [发送短信](#timing) | 定时任务 |

####1、简介
```
内部实现定时发送短信；
配置文件注入的方式进行；
```

#### 2、请求参数
|       参数名称        | 必选   | 类型     | 说明                         |
| :---------------: | :--- | :----- | -------------------------- |
|   sendSms.phone   | true | string | 需要发送的手机号（可多个，用逗号隔开）        |
|       send1       | true | string | 是否在当前时间发送（true/false)（时间1） |
| interval.sendSms1 | true | string | 定时发送的时间1                   |
|       send2       | true | string | 是否在当前时间发送（true/false)（时间1） |
| interval.sendSms2 | true | string | 定时发送的时间2                   |
|       send3       | true | string | 是否在当前时间发送（true/false)（时间1） |
| interval.sendSms3 | true | string | 定时发送的时间3                   |

---

#### 3、调用样例
```
sendSms.phone=15811451620,15911177024
send1=true
interval.sendSms1=0 40 8 * * ?
send2=true
interval.sendSms2=0 10 13 * * ?
send3=true
interval.sendSms3=0 30 18 * * ?
```