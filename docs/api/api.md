
# **ATRI-BOT** API 文档

## API Key
- 在私聊场景下向 **ATRi-BOT** 发送`/api`命令, 若需要获得新的API Key则使用`/api new`
- API Key遵循规范, 在需要API Key的每个请求url query包含`key=string`参数

### Endpoint
- **URL**: https://public.meownya.asia
- **响应格式**：JSON

### 接口列表

#### 1 获取 **ATRI-BOT** 版本信息

- **接口**：`GET /api/version`
- **描述**：获取版本信息
- **请求参数**：
  - `key` [string]：用户的唯一API Key(必填)
  
- **示例请求**：
  ```bash
  GET /api/version
  ```

- **响应数据**：

  ```json
  {
    "status": int,
    "message": string,
    "data": {
        "version": string,
        "go": string,
        "status": string,
        "message": string
    }
  }
  ```

- **响应码**：
  - `200 OK`：请求成功
  - `403 Forbidden`：错误的API Key或没有权限
  - `500 Internal Server Error`：服务器内部错误

---

#### 2 用户信息

- **接口**：`GET api/info`
- **描述**：获得API Key对应用户信息
- **请求参数**：
  - `key` [string]：用户的唯一API Key(必填)
  
- **示例请求**：
  ```bash
  GET /api/info
  ```

- **响应数据**：

  ```json
  {
    "status": int,
    "message": string,
    "data": {
        "verify": boolean,
        "apiData": {}
    }
  }
  ```

- **响应码**：
  - `200 OK`：请求成功
  - `403 Forbidden`：错误的API Key或没有权限
  - `500 Internal Server Error`：服务器内部错误

---
