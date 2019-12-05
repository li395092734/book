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
|  八   | [/select/day](#select-day)               | 查询某天的数据        |

## 查询单词服务列表

### <span id="select-all" >一、查询所有</span>
|            接口方法            | 接口描述 |
| :------------------------: | :--- |
| [/select/all](#select-all) | 查询所有 |

#### 1. 简介
```

```

#### 2. 请求参数
|  参数名称   | 必选    | 类型     | 说明      |
| :-----: | :---- | :----- | ------- |
| english | false | string | 存入的英语单词 |
| chinese | false | string | 存入的汉语   |
| remark  | false | string | 标记字段    |

---

#### 3. 调用样例
```
{
"english":"json",
"chinese":"",	
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
    "data": [
        {
            "englishid": 1,
            "english": "response",
            "chinese": "响应",
            "category": 1,
            "remark": ""
        },
        {
            "englishid": 24,
            "english": "deploy",
            "chinese": "部署",
            "category": null,
            "remark": null
        }
    ]
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
|   参数名称   | 必选   | 类型     | 说明         |
| :------: | :--- | :----- | ---------- |
| pageNum  | true | string | 当前页码（从0开始） |
| pageSize | true | string | 每页显示条数     |

---

#### 3. 调用样例
```
{
"pageNum":"2",
"pageSize":"2"
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
        "pageNum": 2,
        "pageSize": 2,
        "totalSize": 24,
        "totalPages": 12,
        "content": [
            {
                "englishid": 3,
                "english": "File",
                "chinese": "文件",
                "category": 1,
                "remark": null
            },
            {
                "englishid": 4,
                "english": "Edit",
                "chinese": "编辑",
                "category": 1,
                "remark": null
            }
        ]
    }
}
```
---

### <span id="select-oneByEnglish" >三、根据英语查询</span>
|                   接口方法                   | 接口描述   |
| :--------------------------------------: | :----- |
| [/select/oneByEnglish](select-oneByEnglish) | 根据英语查询 |

#### 1. 简介
```

```

#### 2. 请求参数
|  参数名称   | 必选    | 类型     | 说明      |
| :-----: | :---- | :----- | ------- |
| english | true  | string | 存入的英语单词 |
| chinese | false | string | 存入的汉语   |

---

#### 3. 调用样例
```
{
"english":"response"，
"chinese":""
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
        "englishid": 1,
        "english": "response",
        "chinese": "响应",
        "category": 1,
        "remark": ""
    }
}
```
---

### <span id="select-oneByChinese" >四、根据汉语查询</span>
|                   接口方法                   | 接口描述     |
| :--------------------------------------: | :------- |
| [/select/oneByChinese](select-oneByChinese) | 根据汉语查询单个 |

#### 1. 简介
```

```

#### 2. 请求参数
|  参数名称   | 必选    | 类型     | 说明      |
| :-----: | :---- | :----- | ------- |
| english | false | string | 存入的英语单词 |
| chinese | true  | string | 存入的汉语   |

---

#### 3. 调用样例
```
{
"english":"",
"chinese":"响应"
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
        "englishid": 1,
        "english": "response",
        "chinese": "响应",
        "category": 1,
        "remark": ""
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
|   参数名称    | 必选    | 类型     | 说明    |
| :-------: | :---- | :----- | ----- |
| englishId | true  | string | ID    |
|  english  | false | string | 存入的英语 |
|  chinese  | false | string | 存入的汉语 |

---

#### 3. 调用样例
```
{
"englishId":"1",
"english":"",
"chinese":""
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
        "englishid": 1,
        "english": "response",
        "chinese": "响应",
        "category": 1,
        "remark": ""
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
以传入的englishId为基准，如果传入remark为1则ID+1进行查询，为0则ID-1进行查询；
```

#### 2. 请求参数
|   参数名称    | 必选    | 类型     | 说明               |
| :-------: | :---- | :----- | ---------------- |
| englishId | true  | string | ID               |
|  english  | false | string | 存入的汉语            |
|  chinese  | false | string | 存入的汉语            |
|  remark   | true  | string | 标记字段(1上一个；0：下一个) |

---

#### 3. 调用样例
```
{
"englishId":"1",
"english":"",
"chinese":"",	
"remark":"1"
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
        "englishid": 2,
        "english": "Success",
        "chinese": "成功",
        "category": 0,
        "remark": ""
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
根据分类category进行查询；
1：默认的；
2：每月定时查询的；
3：预留；
```

#### 2. 请求参数
|   参数名称   | 必选    | 类型     | 说明      |
| :------: | :---- | :----- | ------- |
| english  | false | string | 存入的英语单词 |
| chinese  | false | string | 存入的汉语   |
| category | true  | string | 存入数据库分类 |
|  remark  | false | string | 标记字段    |

---

#### 3. 调用样例
```
{
"english":"",
"chinese":"",
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
    "data": [
        {
            "englishid": 1,
            "english": "response",
            "chinese": "响应",
            "category": 1,
            "remark": ""
        },
        {
            "englishid": 23,
            "english": "site",
            "chinese": "网站",
            "category": 1,
            "remark": null
        }
    ]
}
```
---

### <span id="select-day" >八、查询某天的数据</span>
|           接口方法            | 接口描述    |
| :-----------------------: | :------ |
| [/select/day](select-day) | 查询某天的数据 |


#### 1. 简介
```
用来查询分类2中的某天的数据
```

#### 2. 请求参数
|   参数名称   | 必选   | 类型     | 说明      |
| :------: | :--- | :----- | ------- |
| category | true | string | 存入数据库分类 |
|   day    | true | string | 存入的天数   |

---

#### 3. 调用样例
```
{
	"category":"2",
	"day":"9"
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
