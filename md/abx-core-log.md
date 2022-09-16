# abx-core-log

> abx 日志封装插件,控制并记录平台运行时日志.

## list
列举当前支持的日志开关.

**参数**

  *无参数*

**返回**

  *无返回值*

**例子**

``` javascript
log.list()
```
## open
打开日志开关

**参数**

  *logModules(String|Array)*: 需要打开的日志模块

**返回**

  *无返回值*

**例子**
``` javascript
log.open(logModules)
```
<!-- | 参数 | 说明 | 类型 |
| --- | --- | --- |
| logModules | 需要打开的日志模块 | string,array | -->
## openAll
打开所有的日志开关

**参数**

  *无参数*

**返回值**

  *无返回值*

**例子**
``` javascript
log.openAll()
```

## writeLog
写入日志信息

**参数**

  1. *logType(String)*: 日志级别
  2. *logModule(String)*: 所属日志模块
  3. *message(String)*: 记录的日志信息

**返回**

  *无返回值*

**例子**

``` javascript
log.writeLog(logType, logModule, message)
```
<!-- | 参数 | 说明 | 类型 |
| --- | --- | --- |
| logType | 日志级别 | string |
| logModule | 所属日志模块 | string |
| message | 记录的日志信息 | string | -->

## info
info 级别日志记录

**参数**

  1. *logModule(String)*: 所属日志模块
  2. *message(String)*: 记录的日志信息

**返回值**

  *无返回值*

**例子**

```javascript
log.info(logModule, message)
```

## error
error 级别日志记录
**参数**

  1. *logModule(String)*: 所属日志模块
  2. *message(String)*: 记录的日志信息

**返回值**

  *无返回值*

**例子**

```javascript
log.error(logModule, message)
```
## warn
warn 级别日志记录

**参数**

  1. *logModule(String)*: 所属日志模块
  2. *message(String)*: 记录的日志信息

**返回值**

  *无返回值*

**例子**

```javascript
log.warn(logModule, message)
```
## debug
debug 级别日志记录

**参数**

  1. *logModule(String)*: 所属日志模块
  2. *message(String)*: 记录的日志信息

**返回值**

  *无返回值*

**例子**

```javascript
log.debug(logModule, message)
```
## fatal
fatal 级别日志记录

**参数**

  1. *logModule(String)*: 所属日志模块
  2. *message(String)*: 记录的日志信息

**返回值**

  *无返回值*

**例子**

```javascript
log.fatal(logModule, message)
```

<!-- | 参数 | 说明 | 类型 |
| --- | --- | --- |
| logModule | 所属日志模块 | string |
| message | 记录的日志信息 | string | -->

