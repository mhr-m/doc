# abx-plugin-keyboard

## 引入@abx/abx-plugin-keyboard

``` javascript
import { KeyboardPlugin } from '@abx/abx-plugin-keyboard'

let keyboard = new KeyboardPlugin()
```

## verifyId


## getElementId


## bindKeyboard


## setProperty


## getProperty


## showKeyboard

## getValue
获得密文

**参数**

   1. *id(String)*: 密文`id`
   2. *timestamp(String)*: 时间戳，毫秒
   3. *callback(Function)*: 回调函数

**返回**

   1. **

**例子**

```javascript
keyboard.getValue(id, timestamp, callback)
```

## getPinValue
获得PIN密文

**参数**

   1. *id(String)*: 密文`id`
   2. *timestamp(String)*: 时间戳，毫秒

**返回**

**例子**

```javascript
keyboard.getPinValue(id, timestamp, callback)
```

## hideKeyboard


## publicModulus


## publicAppModulus


## publicKeyECC


## passwordIsEqual


## verify


## getLength


## getDegree


## lastError


## clear


## onKeyboardHeightChanged


## onPasswordChanged


## payPublicAppModulus


## payPublicModulus


## payPublicKeyECC

## showPayKeyboard
显示支付密码界面

**参数**

  1. *kbdParam(Object)*: 密码键盘
  2. *payInfo*: 支付内容，包括转入方姓名，转账金额，收款银行，收款账号，业务类型以及手续费

**返回**

  *无返回值*

**例子**

```javascript
let kbdParam = {
    'KEYBOARD_TYPE': '1'
}
let payInfo = {
    PayeeName: '', // 转入方姓名
    TransPrice: '', // 转账金额
    BankName: '', // 收款银行
    PayeeAcNo: '', // 收款账号
    PayeeType: '', // 业务类型，'0' - 转账，'1' - 支付， '2' - 圈存
    PayeeCost: '', // 手续费，PayeeType为0时使用
}
keyboard.showKeyboard(kbdParam, payInfo, callback)
```

## getPayValue
获得支付密文

**参数**

  *timestamp(String)*: 时间戳，毫秒

**返回**

**例子**

```javascript
keyboard.getPayValue(timestamp, callback)
```

## getCipherText
对json字符串加密， 两个公钥按照算法设置，如果已经内容，传入为""即可。

**参数**

  1. *appPubKey(String)*: 应用平台公钥， 如果是rsa，使用公钥模数
  2. *encPubKey(String)*: 加密平台公钥， 如果是rsa，使用公钥模数, 如果是国密，使用"eccX,eccY", 逗号分隔
  3. *timestamp(String)*: 时间戳，毫秒
  4. *jsonStr(String)*: 必须`json`字符串

**返回**

**例子**

```javascript
keyboard.getCipherText(appPubKey, encPubKey, timestamp, jsonStr, callback)
```