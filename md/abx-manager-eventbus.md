# abx-manager-eventbus

> abx 事件总线. 画面间事件的注册、触发、监听、销毁.

## 引入使用
``` javascript
import EventBus from "abx-manager-eventbus";
```

## $emit
触发事件并传入需要传递的参数

**参数:**
  1. *name(String)*: 注册时的事件名称
  2. *data(Any)*: 事件触发时,需要传递给回调函数的参数

**返回:**

  *无返回值*

**例子:**
``` javascript
EventBus.$emit(name, data)
```

## $on
注册事件及对应回调函数

**参数:**
  1. *name(String)*: 注册时的事件名称
  2. *fn(Function)*: 事件触发时需要执行的回调函数

**返回:**

  *(Object)*: 注册成功后的事件对象

**例子:**
``` javascript
// 不查看返回值,可直接使用 EventBus.$on(name, fn)
let res = EventBus.$on(name, fn)
```

## $off
销毁已注册事件及对应回调函数

**参数:**
  1. *name(String)*: 注册时的事件名称
  2. *fn(Function)*: 事件触发时需要执行的回调函数

**返回:**

  *(Array)*: 销毁指定事件后，剩余的事件数组

**例子:**
``` javascript
let res = EventBus.$off(name, fn)
```