## 增加单词服务
| 序号 | 接口方法 | 接口描述 |
|:-------------:|:-------------|:-------------|
| 一 |[/add/english](#add-english) | 增加英语 |
| 二 |[/add/chinese](#add-chinese) | 增加汉语 |
| 三 |[/add/batchEnglish](#add-batchEnglish) | 批量增加英文 |
| 四 |[/add/file](#add-file) | 通过文档添加英语 |

## 增加单词服务列表


### <span id="add-english" >一、增加英语</span>
| 接口方法 | 接口描述 |
|:-------------:|:-------------|
| [/add/english](#add-english) | 增加英语 |


#### 1. 请求参数
| 参数名称| 必选 | 类型 | 说明 |
|:-------------:|:-------------|:-------------|--------------|
| english | true | string |存入的英语单词|
| chinese | false | string |存入的汉语|
| category | true | string |存入数据库分类|
| remark | false | string | 标记字段       |

---

#### 2. 调用样例
```
{
"english":"response",
"chinese":"你好",
"category":"1",
"remark":""
}
```
---

#### 3. 返回结果
| 字段| 类型 | 说明 |
|:-------------:|:-------------|:-------------|
| status | String | 返回码 |
| errmsg | String | 返回码描述 |
| data | json | 数据 |

---
#### 4. JSON示例

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

### <span id="add/chinese" >二、增加汉语</span>
| 接口方法 | 接口描述 |
|:-------------:|:-------------|
| [/add/chinese](#add-chinese) | 增加汉语 |


#### 1. 请求参数
| 参数名称| 必选 | 类型 | 说明 |
|:-------------:|:-------------|:-------------|--------------|
| english | false | string |存入的英语单词|
| chinese | true | string |存入的汉语|
| category | true | string |存入数据库分类|
| remark | false | string | 标记字段       |

---

#### 2. 调用样例
```
{
"english":"",
"chinese":"你好",
"category":"0",
"remark":""
}
```
---

#### 3. 返回结果
| 字段| 类型 | 说明 |
|:-------------:|:-------------|:-------------|
| status | String | 返回码 |
| errmsg | String | 返回码描述 |
| data | json | 数据 |

---
#### 4. JSON示例

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
| 接口方法 | 接口描述 |
|:-------------:|:-------------|
| [/add/batchEnglish](#add-batchEnglish) | 批量增加英文 |


#### 1. 请求参数
| 参数名称| 必选 | 类型 | 说明 |
|:-------------:|:-------------|:-------------|--------------|
| english | true | string |存入的英语单词|
| chinese | false | string |存入的汉语|
| category | false | string |存入数据库分类|
| remark | false | string | 标记字段       |
| day | false | string | 每个月自动显示日期 |

---

#### 2. 调用样例
```
{
"english":"requst rew",
"chinese":"你好",
"category":"0",
"remark":"",
"day":"9"
}
```
---

#### 3. 返回结果
| 字段| 类型 | 说明 |
|:-------------:|:-------------|:-------------|
| status | String | 返回码 |
| errmsg | String | 返回码描述 |
| data | json | 数据 |

---
#### 4. JSON示例

* 请求成功数据格式：

```
{
    "status": 200,
    "errmsg": "成功",
    "data": {
        "requst": "true，类别为：0",
        "rew": "true，类别为：0"
    }
}
```
---

### <span id="add-file" >四、.通过文档添加英语</span>
| 接口方法 | 接口描述 |
|:-------------:|:-------------|
| [/add/file](#add-file) | 通过文档添加英语 |


#### 1. 请求参数
| 参数名称| 必选 | 类型 | 说明 |
|:-------------:|:-------------|:-------------|
| file | true | MultipartFile |需要上传的文件|

---

#### 2. 调用样例
```
http://{ip:port}/add/file?
Body下选择form-data格式:
选择类型为:File
key:file
选择文件:选择要上传的文件
注:headers必需为空,否则上传会失败
```
---

#### 3. 返回结果
| 字段| 类型 | 说明 |
|:-------------:|:-------------|:-------------|
| status | String | 返回码 |
| errmsg | String | 返回码描述 |
| data | json | 数据 |

---
#### 4. JSON示例

* 请求成功数据格式：

```
{
    "status": 200,
    "errmsg": "成功",
    "data": {
        "myself": "true，类别为：null",
        "me": "true，类别为：null",
        "your": "true，类别为：null",
        "my": "true，类别为：null",
        "you": "true，类别为：null"
    }
}
```
---