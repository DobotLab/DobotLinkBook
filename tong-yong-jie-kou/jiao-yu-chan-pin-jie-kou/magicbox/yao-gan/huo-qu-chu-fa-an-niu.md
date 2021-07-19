# 获取触发按钮

## 基本信息

* 状态：有效
* 引入版本：6.2.0
* 依赖固件版本：

## 发送

### 例子

```text
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "dobotlink.MagicBox.GetJoystickButton",
  "params": {
    "portName": "tty.usbmodem336E317934382",
    "port": 4
  }
}
```

### 参数

* portName
  * 意义：串口名/IP
  * 类型：string
* port
  * 意义：串口名或者IP
  * 类型：number
  * 范围：0~5，对应BOX的物理接口

## 返回

### 例子

```text
{
  "id": 1,
  "jsonrpc": "2.0",
  "result": {
    "res": [0, 4]
  }
}
```

### 参数

* res
  * 意义：触发按钮组成的数组
  * 类型：array&lt;number&gt;
  * 范围
    * 0：前
    * 1：后
    * 2：左
    * 3：右
    * 4：下

## 异常

略

