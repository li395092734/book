删除单词服务

|  序号  | 接口方法                               | 接口描述     |
| :--: | :--------------------------------- | :------- |
|  一   | [/delete/english](#delete-english) | 根据英文进行删除 |
|  二   | [/delete/id](#delete-id)           | 根据ID进行删除 |

## 删除单词服务列表

### <span id="delete-english" >一、根据英文进行删除</span>
|                接口方法                | 接口描述     |
| :--------------------------------: | :------- |
| [/delete/english](#delete-english) | 根据英文进行删除 |

#### 1、简介
```

```

#### 2、请求参数
|   参数名称    | 必选    | 类型     | 说明      |
| :-------: | :---- | :----- | ------- |
| englishId | false | string | ID      |
|  english  | true  | string | 存入的英语单词 |
|  chinese  | false | string | 存入的汉语   |
|  remark   | false | string | 标记字段    |

---

#### 3、 调用样例
```
{
"englishId":"",
"english":"Final",
"chinese":"",	
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
#### 5、 JSON示例

* 请求成功数据格式：

```
{
    "status": 200,
    "errmsg": "成功",
    "data": "Final"
}
```
---

## <span id="delete-id" >二、根据ID进行删除</span>
|           接口方法           | 接口描述     |
| :----------------------: | :------- |
| [/delete/id](#delete-id) | 根据ID进行删除 |

#### 1、简介
```

```

#### 2、请求参数
|   参数名称    | 必选    | 类型     | 说明      |
| :-------: | :---- | :----- | ------- |
| englishId | true  | string | ID      |
|  english  | false | string | 存入的英语单词 |
|  chinese  | false | string | 存入的汉语   |
|  remark   | false | string | 标记字段    |

---

#### 3、 调用样例
```
{
"englishId":"26",
"english":"",
"chinese":"",	
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
#### 5、 JSON示例

* 请求成功数据格式：

```
{
    "status": 200,
    "errmsg": "成功",
    "data": 26
}
```
---