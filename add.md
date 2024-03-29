## 增加单词服务
|  序号  | 接口方法                                   | 接口描述     |
| :--: | :------------------------------------- | :------- |
|  一   | [/add/english](#add-english)           | 增加英语     |
|  二   | [/add/chinese](#add-chinese)           | 增加汉语     |
|  三   | [/add/batchEnglish](#add-batchEnglish) | 批量增加英文   |
|  四   | [/add/file](#add-file)                 | 通过文档添加英语 |

## 增加单词服务列表


### <span id="add-english" >一、增加英语</span>
|             接口方法             | 接口描述 |
| :--------------------------: | :--- |
| [/add/english](#add-english) | 增加英语 |

#### 1、 简介

```
当前接口仅支持1分类添加；
category分类中：1:普通添加；2：按月定时进行查询（1~30）；3：预留；
```



#### 2、请求参数
|   参数名称   | 必选    | 类型     | 说明             |
| :------: | :---- | :----- | -------------- |
| english  | true  | string | 存入的英语单词        |
| chinese  | false | string | 存入的汉语          |
| category | true  | string | 存入数据库分类（1、2、3） |
|  remark  | false | string | 标记字段           |

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

### <span id="add-chinese" >二、增加汉语</span>
|             接口方法             | 接口描述 |
| :--------------------------: | :--- |
| [/add/chinese](#add-chinese) | 增加汉语 |

#### 1、请求参数

```
当前接口仅支持1分类添加；
category分类中：1:普通添加；2：按月定时进行查询（1~30）；3：预留；
```

---

#### 2、请求参数
|   参数名称   | 必选    | 类型     | 说明             |
| :------: | :---- | :----- | -------------- |
| english  | false | string | 存入的英语单词        |
| chinese  | true  | string | 存入的汉语          |
| category | true  | string | 存入数据库分类(1、2、3) |
|  remark  | false | string | 标记字段           |

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
        "english": "Hello",
        "chinese": "你好",
        "category": 0,
        "remark": "",
        "day": null
    }
}
```
---

### <span id="add-batchEnglish" >三、批量增加英语</span>
|                  接口方法                  | 接口描述   |
| :------------------------------------: | :----- |
| [/add/batchEnglish](#add-batchEnglish) | 批量增加英文 |

#### 1、请求参数

```
当前接口仅支持1分类添加；
category分类中：
1:普通添加；
2：按月定时进行查询（1~30），需要与day内容进行配合使用；
3：预留；
```

---

#### 2、请求参数
|   参数名称   | 必选    | 类型     | 说明              |
| :------: | :---- | :----- | --------------- |
| english  | true  | string | 存入的英语单词         |
| chinese  | false | string | 存入的汉语           |
| category | false | string | 存入数据库分类（1、2、3）  |
|  remark  | false | string | 标记字段            |
|   day    | false | string | 每个月自动显示日期（1~30） |

---

#### 3、调用样例
```
{
"english":"requst rew",
"chinese":"你好",
"category":"2",
"remark":"",
"day":"9"
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
        "requst": "true，类别为：2",
        "rew": "true，类别为：2"
    }
}
```
---

### <span id="add-file" >四、.通过文档添加英语</span>
|          接口方法          | 接口描述     |
| :--------------------: | :------- |
| [/add/file](#add-file) | 通过文档添加英语 |

#### 1、请求参数

```
默认添加到分类1中；
```

---

#### 2、请求参数
| 参数名称 | 必选   | 类型            | 说明      |
| :--: | :--- | :------------ | ------- |
| file | true | MultipartFile | 需要上传的文件 |

---

#### 3、调用样例
```
http://{ip:port}/add/file?
Body下选择form-data格式:
选择类型为:File
key:file
选择文件:选择要上传的文件
注:headers必需为空,否则上传会失败
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
        "myself": "true，类别为：1",
        "me": "true，类别为：1",
        "your": "true，类别为：1",
        "my": "true，类别为：1",
        "you": "true，类别为：1"
    }
}
```
---