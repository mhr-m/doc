# abx-manager-http

> abx 内请求方法封装.

## 引入使用
```javascript
import { HttpManager } from "abx-manager-http"
```

## postAsync
封装 post 方法

**参数:**
  1. *url(String)*: 请求的地址
  2. *data(Object)*: 用户自定义的请求体信息
  3. *header(Object)*: 用户自定义的请求头信息

**返回:**

  *(Object)*: 请求返回的响应

**例子:**
``` javascript
let response = await HttpManager.postAsync(url, data, header);
```

## getAsync
封装 post 方法

**参数:**
  1. *url(String)*: 请求的地址
  2. *params(Object)*: 用户自定义的请求体信息
  3. *header(Object)*: 用户自定义的请求头信息

**返回:**

  *(Object)*: 请求返回的响应

**例子:**
``` javascript
let response = await HttpManager.getAsync(url, params, header);
```

