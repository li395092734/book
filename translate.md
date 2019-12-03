## 翻译服务
|  序号  | 接口方法                                     | 接口描述   |
| :--: | :--------------------------------------- | :----- |
|  一   | [/translate/english](#translate-english) | 根据英语翻译 |
|  二   | [/translate/chinese](#translate-chinese) | 根据汉语翻译 |


## 翻译服务列表

### <span id="translate-english" >一、根据英语翻译</span>
|                   接口方法                   | 接口描述   |
| :--------------------------------------: | :----- |
| [/translate/english](#translate-english) | 根据英语翻译 |

#### 1、简介
```

```

#### 2、 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3、 调用样例
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
#### 5、 JSON示例

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


### <span id="translate-chinese" >二、根据汉语翻译</span>
|                   接口方法                   | 接口描述   |
| :--------------------------------------: | :----- |
| [/translate/chinese](#translate-chinese) | 根据汉语翻译 |

#### 1、简介
```

```

#### 2、 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3、 调用样例
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
#### 5、 JSON示例

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
