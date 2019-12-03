查询单词服务

|  序号  | 接口方法                                     | 接口描述           |
| :--: | :--------------------------------------- | :------------- |
|  一   | [/select/all](#select-all)               | 查询所有           |
|  二   | [/select/findPage](#select-findPage)     | 分页查询           |
|  三   | [/select/oneByEnglish](#select-oneByEnglish) | 根据英语查询单个       |
|  四   | [/select/oneByChinese](#select-oneByChinese) | 根据汉语查询单个       |
|  五   | [/select/oneById](#select-oneById)       | 根据Id进行查询       |
|  六   | [/select/near](#select-near)             | 根据Id进行下一个（上一个） |
|  七   | [/select/category](#select-category)     | 根据分类信息查询全部     |
|  八   | [/select/Day](#select-Day)               | 查询某天的数据        |

## 查询单词服务列表

### <span id="select-all" >一、查询所有</span>
|            接口方法            | 接口描述 |
| :------------------------: | :--- |
| [/select/all](#select-all) | 查询所有 |

#### 1. 简介
```

```

#### 2. 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3. 调用样例
```
{
"english":"response",
"chinese":"你好",
"category":"1",
"remark":""
}
```
---

#### 4. 返回结果
|   字段   | 类型     | 说明    |
| :----: | :----- | :---- |
| status | String | 返回码   |
| errmsg | String | 返回码描述 |
|  data  | json   | 数据    |

---
#### 5. JSON示例

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

### <span id="select-findPage" >二、分页查询</span>
|                接口方法                 | 接口描述 |
| :---------------------------------: | :--- |
| [/select/findPage](select-findPage) | 分页查询 |

#### 1. 简介
```

```

#### 2. 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3. 调用样例
```
{
"english":"response",
"chinese":"你好",
"category":"1",
"remark":""
}
```
---

#### 4. 返回结果
|   字段   | 类型     | 说明    |
| :----: | :----- | :---- |
| status | String | 返回码   |
| errmsg | String | 返回码描述 |
|  data  | json   | 数据    |

---
#### 5. JSON示例

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

### <span id="select-oneByEnglish" >三、根据英语查询单个</span>
|                   接口方法                   | 接口描述     |
| :--------------------------------------: | :------- |
| [/select/oneByEnglish](select-oneByEnglish) | 根据英语查询单个 |

#### 1. 简介
```

```

#### 2. 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3. 调用样例
```
{
"english":"response",
"chinese":"你好",
"category":"1",
"remark":""
}
```
---

#### 4. 返回结果
|   字段   | 类型     | 说明    |
| :----: | :----- | :---- |
| status | String | 返回码   |
| errmsg | String | 返回码描述 |
|  data  | json   | 数据    |

---
#### 5. JSON示例

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

### <span id="select-oneByChinese" >四、根据汉语查询单个</span>
|                   接口方法                   | 接口描述     |
| :--------------------------------------: | :------- |
| [/select/oneByChinese](select-oneByChinese) | 根据汉语查询单个 |

#### 1. 简介
```

```

#### 2. 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3. 调用样例
```
{
"english":"response",
"chinese":"你好",
"category":"1",
"remark":""
}
```
---

#### 4. 返回结果
|   字段   | 类型     | 说明    |
| :----: | :----- | :---- |
| status | String | 返回码   |
| errmsg | String | 返回码描述 |
|  data  | json   | 数据    |

---
#### 5. JSON示例

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

### <span id="select-oneById" >五、根据Id进行查询</span>
|               接口方法                | 接口描述     |
| :-------------------------------: | :------- |
| [/select/oneById](select-oneById) | 根据Id进行查询 |

#### 1. 简介
```

```

#### 2. 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3. 调用样例
```
{
"english":"response",
"chinese":"你好",
"category":"1",
"remark":""
}
```
---

#### 4. 返回结果
|   字段   | 类型     | 说明    |
| :----: | :----- | :---- |
| status | String | 返回码   |
| errmsg | String | 返回码描述 |
|  data  | json   | 数据    |

---
#### 5. JSON示例

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

### <span id="select-near" >六、根据Id进行下一个（上一个）</span>
|            接口方法             | 接口描述           |
| :-------------------------: | :------------- |
| [/select/near](select-near) | 根据Id进行下一个（上一个） |

#### 1. 简介
```

```

#### 2. 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3. 调用样例
```
{
"english":"response",
"chinese":"你好",
"category":"1",
"remark":""
}
```
---

#### 4. 返回结果
|   字段   | 类型     | 说明    |
| :----: | :----- | :---- |
| status | String | 返回码   |
| errmsg | String | 返回码描述 |
|  data  | json   | 数据    |

---
#### 5. JSON示例

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

### <span id="select-category" >七、根据分类信息查询全部</span>
|                接口方法                 | 接口描述       |
| :---------------------------------: | :--------- |
| [/select/category](select-category) | 根据分类信息查询全部 |

#### 1. 简介
```

```

#### 2. 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3. 调用样例
```
{
"english":"response",
"chinese":"你好",
"category":"1",
"remark":""
}
```
---

#### 4. 返回结果
|   字段   | 类型     | 说明    |
| :----: | :----- | :---- |
| status | String | 返回码   |
| errmsg | String | 返回码描述 |
|  data  | json   | 数据    |

---
#### 5. JSON示例

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

### <span id="select-Day" >八、查询某天的数据</span>
|           接口方法            | 接口描述    |
| :-----------------------: | :------ |
| [/select/Day](select-Day) | 查询某天的数据 |


#### 1. 简介
```

```

#### 2. 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | true  | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3. 调用样例
```
{
"english":"response",
"chinese":"你好",
"category":"1",
"remark":""
}
```
---

#### 4. 返回结果
|   字段   | 类型     | 说明    |
| :----: | :----- | :---- |
| status | String | 返回码   |
| errmsg | String | 返回码描述 |
|  data  | json   | 数据    |

---
#### 5. JSON示例

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
