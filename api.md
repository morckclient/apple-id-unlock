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
| index    | int    | ✔︎  | 账号的序号   |
| p        | string | ✔︎  | 用户访问密码 |

- 示例：https://appleid.morck.xyz/getInfo/id?index=1&p=morck
