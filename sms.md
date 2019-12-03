## 增加单词服务
|  序号  | 接口方法                         | 接口描述 |
| :--: | :--------------------------- | :--- |
|  一   | [/sms/sendSms](#sms-sendSms) | 发送短信 |
|  二   | [发送短信](#timing)              | 定时任务 |


## 增加单词服务列表


### <span id="sms-sendSms" >一、发送短信</span>
|             接口方法             | 接口描述 |
| :--------------------------: | :--- |
| [/sms/sendSms](#sms-sendSms) | 发送短信 |

#### 1、简介

#### 2、 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3、调用样例
```
{
"english":"response",
"chinese":"你好",
"category":"1",
"remark":""
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
    "data": {
        "englishid": null,
        "english": "data",
        "chinese": "数据",
        "category": 1,
        "remark": "",
        "day": null
    }
}
```
---

### <span id="timing" >二、增加汉语</span>
|      接口方法       | 接口描述 |
| :-------------: | :--- |
| [发送短信](#timing) | 定时任务 |

####1、简介
```

```

#### 2、请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | false | string | 存入的英语单词 |
| chinese  | true  | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3、调用样例
```
{
"english":"",
"chinese":"你好",
"category":"0",
"remark":""
}
```
---

#### 4、 返回结果
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
    "data": {
        "englishid": null,
        "english": "Hello",
        "chinese": "你好",
        "category": 0,
        "remark": "",
        "day": null
    }
}
```
---