# API 参考

本页面用于练习接口文档的编写方式。

以下接口仅为文档示例，本项目没有提供真实后端服务，不能直接请求这些路径获取数据。

## 查询文档列表

### 接口信息

| 项目 | 内容 |
| --- | --- |
| 请求方法 | GET |
| 请求路径 | /api/docs |
| 功能 | 查询文档条目列表 |
| 返回格式 | JSON |

### 查询参数

| 参数 | 类型 | 是否必填 | 说明 |
| --- | --- | --- | --- |
| page | integer | 否 | 页码，默认值为 1 |
| page_size | integer | 否 | 每页条数，默认值为 10 |

### 请求示例

```http
GET /api/docs?page=1&page_size=10 HTTP/1.1
Host: example.com
Accept: application/json
```

### 返回示例

```json
{
  "page": 1,
  "page_size": 10,
  "total": 2,
  "items": [
    {
      "id": 1,
      "title": "使用指南",
      "path": "guide.md"
    },
    {
      "id": 2,
      "title": "关于本项目",
      "path": "about.md"
    }
  ]
}
```

### 返回字段说明

| 字段 | 类型 | 含义 |
| --- | --- | --- |
| page | integer | 当前页码 |
| page_size | integer | 每页条数 |
| total | integer | 文档总数 |
| items | array | 当前页的文档列表 |
| items[].id | integer | 文档编号 |
| items[].title | string | 文档标题 |
| items[].path | string | 文档路径 |

## 错误返回示例

当查询参数不符合要求时，可以使用以下格式描述错误：

```json
{
  "error": {
    "code": "INVALID_PARAMETER",
    "message": "page 必须是大于等于 1 的整数"
  }
}
```

## 文档编写体会

一份接口文档需要说明请求方法、路径、参数和返回结果。
字段表格可以帮助读者理解数据含义，代码示例可以展示具体格式。

[返回首页](index.md) · [查看使用指南](guide.md)
