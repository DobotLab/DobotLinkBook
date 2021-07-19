# 获取摇杆位置

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
  "method": "dobotlink.MagicBox.GetJoystickPos",
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
    "x": 123,
    "y": 0,
    "z": 0
  }
}
```

### 参数

* x
  * 意义：x坐标
  * 类型：number
  * 范围：0~255
* y
  * 意义：y坐标
  * 类型：number
  * 范围：0~255
* z
  * 意义：是否被按下
  * 类型：number
  * 范围
    * 1：被按下
    * 0：没按下

## 异常

略

