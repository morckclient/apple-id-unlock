## 1.获取独立账号生成的网页

> `GET` /preview 

- 请求参数
  `json`

```json
 {
  "index": "1",
  "p": "morck"
}
```

| 参数名      | 类型     | 必填  | 描述   |
|----------|--------|-----|------|
| index    | int    | ✔︎  | 账号的序号   |
| p        | string | ✔︎  | 用户访问密码 |

- 示例：https://appleid.morck.xyz/preview?index=1&p=morck

## 2.获取独立账号的JSON

> `GET` /getInfo/id

- 请求参数
  `json`

```json
 {
  "index": "1",
  "p": "morck"
}
```

| 参数名      | 类型     | 必填  | 描述   |
|----------|--------|-----|------|
| index    | number | ✔︎  | 账号的序号   |
| p        | string | ✔︎  | 用户访问密码 |

- 示例：https://appleid.morck.xyz/getInfo/id?index=1&p=morck

- 成功返回示例 `json`

```json
{
    "available": 0, 
    "headline": "APPLE ID", 
    "password": "123456", 
    "update_time": "2022-11-09 17:38:58", 
    "username": "testappleid@mail.com"
}
```

| 参数名                    | 类型                 | 描述      |
|------------------------|--------------------|---------|
| available              | number             | 是否可用    |
| headline               | string             | 账号标题    |
| password               | string             | 账号密码  |
| update_time            | time_stmp          | 更新时间 |
| username               | string             | 账号    |


## 3.获取全部账号的JSON

> `GET` /getInfo/all_id

- 请求参数
  `json`

```json
 {
  "p": "morck"
}
```

| 参数名      | 类型     | 必填  | 描述   |
|----------|--------|-----|------|
| p        | string | ✔︎  | 用户访问密码 |

- 示例：https://appleid.morck.xyz/getInfo/all_id?p=morck

- 成功返回示例 `json`

```json
{
    "account": [
        {
            "available": 0, 
            "headline": "APPLE ID", 
            "password": "Knc896310", 
            "update_time": "2022-11-09 17:38:58", 
            "username": "testappleid@mail.com"
        }
    ]
}
```

| 参数名                    | 类型                 | 描述      |
|------------------------|--------------------|---------|
| account                | array              | 账号数组    |
| available              | number             | 是否可用    |
| headline               | string             | 账号标题    |
| password               | string             | 账号密码  |
| update_time            | time_stmp          | 更新时间 |
| username               | string             | 账号    |
