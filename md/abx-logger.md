# abx-logger

## 引入使用
```javascript
import { TradeLog } from "abx-logger"
```

## info
提示信息

**参数**

  1. *message(String)*: 信息
  2. *exception(LogException)*: 异常对象

**返回**

  *无返回值*

**例子**

```javascript
TradeLog.info(message, exception)
```

## warn
警告信息

**参数**

  1. *message(String)*: 信息
  2. *exception(LogException)*: 异常对象

**返回**

  *无返回值*

**例子**

```javascript
TradeLog.warn(message, exception)
```

## debug
调试信息

**参数**

  1. *message(String)*: 信息
  2. *exception(LogException)*: 异常对象

**返回**

  *无返回值*

**例子**

```javascript
TradeLog.debug(message, exception)
```

## error
错误信息

**参数**

  1. *message(String)*: 信息
  2. *exception(LogException)*: 异常对象

**返回**

  *无返回值*

**例子**

```javascript
TradeLog.error(message, exception)
```

## fatal
致命信息

**参数**

  1. *message(String)*: 信息
  2. *exception(LogException)*: 异常对象

**返回**

  *无返回值*

**例子**

```javascript
TradeLog.fatal(message, exception)
```

