# 判断触发手势

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
  "method": "dobotlink.MagicBox.IsSensorHandModel",
  "params": {
    "portName": "tty.usbmodem336E317934382",
    "port": 4,
    "data": 0
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
* data
  * 意义：手势类型
  * 类型：number
  * 范围
    * 1：右
    * 2：左
    * 4：上
    * 8：下
    * 16：前
    * 32：后
    * 64：顺时针画圆
    * 128：逆时针画圆
    * 255：没有手势

## 返回

### 例子

```text
{
  "id": 1,
  "jsonrpc": "2.0",
  "result": {
    "data": 1
  }
}
```

### 参数

* data
  * 意义：是否
  * 类型：number
  * 范围
    * 1：是
    * 0：否

## 异常

略

