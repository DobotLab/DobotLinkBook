# 判断触发手势

## 基本信息

| 状态 | 对应 Dobotlink 版本 | 依赖固件版本 | 修改内容 | 备注 |
| :--: | :-----------------: | :----------: | :------- | :--: |
|  ✅  |        6.2.0        |    1.4.0     |          |      |

## 发送

### 例子

```json
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

<table>
  <thead>
    <tr>
      <th style="text-align:center">&#x53C2;&#x6570;&#x540D;</th>
      <th style="text-align:center">&#x662F;&#x5426;&#x5FC5;&#x9009;</th>
      <th style="text-align:center">&#x610F;&#x4E49;</th>
      <th style="text-align:center">&#x7C7B;&#x578B;</th>
      <th style="text-align:center">&#x9ED8;&#x8BA4;&#x503C;</th>
      <th style="text-align:center">&#x53D6;&#x503C;&#x8303;&#x56F4;</th>
      <th style="text-align:center">&#x5907;&#x6CE8;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">
        <p></p>
        <p>portName</p>
      </td>
      <td style="text-align:center">&#x2705;</td>
      <td style="text-align:center">
        <p></p>
        <p>&#x4E32;&#x53E3;&#x540D;/IP</p>
      </td>
      <td style="text-align:center">
        <p></p>
        <p>string</p>
      </td>
      <td style="text-align:center"></td>
      <td style="text-align:center"></td>
      <td style="text-align:center"></td>
    </tr>
    <tr>
      <td style="text-align:center">port</td>
      <td style="text-align:center">&#x2705;</td>
      <td style="text-align:center">BOX&#x7684;&#x7269;&#x7406;&#x63A5;&#x53E3;</td>
      <td style="text-align:center">number</td>
      <td style="text-align:center"></td>
      <td style="text-align:center">0~5</td>
      <td style="text-align:center"></td>
    </tr>
    <tr>
      <td style="text-align:center">data</td>
      <td style="text-align:center">&#x2705;</td>
      <td style="text-align:center">&#x624B;&#x52BF;&#x7C7B;&#x578B;</td>
      <td style="text-align:center">number</td>
      <td style="text-align:center"></td>
      <td style="text-align:center">
        <p></p>
        <ul>
          <li>1&#xFF1A;&#x53F3;</li>
          <li>2&#xFF1A;&#x5DE6;</li>
          <li>4&#xFF1A;&#x4E0A;</li>
          <li>8&#xFF1A;&#x4E0B;</li>
          <li>16&#xFF1A;&#x524D;</li>
          <li>32&#xFF1A;&#x540E;</li>
          <li>64&#xFF1A;&#x987A;&#x65F6;&#x9488;&#x753B;&#x5706;</li>
          <li>128&#xFF1A;&#x9006;&#x65F6;&#x9488;&#x753B;&#x5706;</li>
          <li>255&#xFF1A;&#x6CA1;&#x6709;&#x624B;&#x52BF;</li>
        </ul>
      </td>
      <td style="text-align:center"></td>
    </tr>
    <tr>
      <td style="text-align:center">isQueued</td>
      <td style="text-align:center"></td>
      <td style="text-align:center">&#x662F;&#x5426;&#x961F;&#x5217;&#x6267;&#x884C;</td>
      <td style="text-align:center">bool</td>
      <td style="text-align:center">false</td>
      <td style="text-align:center">
        <ul>
          <li>true&#xFF1A;&#x961F;&#x5217;&#x6267;&#x884C;</li>
          <li>false&#xFF1A;&#x7ACB;&#x5373;&#x6267;&#x884C;</li>
        </ul>
      </td>
      <td style="text-align:center"></td>
    </tr>
    <tr>
      <td style="text-align:center">isWaitForFinish</td>
      <td style="text-align:center"></td>
      <td style="text-align:center">&#x662F;&#x5426;&#x7B49;&#x5F85;&#x961F;&#x5217;&#x6267;&#x884C;&#x5B8C;&#x6210;&#x518D;&#x8FD4;&#x56DE;&#x7ED3;&#x679C;</td>
      <td
      style="text-align:center">bool</td>
        <td style="text-align:center">false</td>
        <td style="text-align:center">
          <p></p>
          <ul>
            <li>true&#xFF1A;&#x7B49;&#x5F85;</li>
            <li>false&#xFF1A;&#x4E0D;&#x7B49;&#x5F85;</li>
          </ul>
        </td>
        <td style="text-align:center">&#x53EA;&#x5728;&#x961F;&#x5217;&#x6267;&#x884C;&#x540E;&#x751F;&#x6548;</td>
    </tr>
    <tr>
      <td style="text-align:center">timeout</td>
      <td style="text-align:center"></td>
      <td style="text-align:center">&#x4E1A;&#x52A1;&#x6267;&#x884C;&#x7684;&#x8D85;&#x65F6;&#x65F6;&#x95F4;</td>
      <td
      style="text-align:center">number</td>
        <td style="text-align:center">25000</td>
        <td style="text-align:center"></td>
        <td style="text-align:center"></td>
    </tr>
  </tbody>
</table>

## 返回

### 例子

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "result": {
    "data": 1
  }
}
```

### 参数

<table>
  <thead>
    <tr>
      <th style="text-align:center">&#x53C2;&#x6570;&#x540D;</th>
      <th style="text-align:center">&#x610F;&#x4E49;</th>
      <th style="text-align:center">&#x7C7B;&#x578B;</th>
      <th style="text-align:center">&#x53D6;&#x503C;&#x8303;&#x56F4;</th>
      <th style="text-align:center">&#x5907;&#x6CE8;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">data</td>
      <td style="text-align:center">&#x662F;&#x5426;&#x68C0;&#x6D4B;&#x5230;&#x76F8;&#x5E94;&#x624B;&#x52BF;</td>
      <td
      style="text-align:center">number</td>
        <td style="text-align:center">
          <p></p>
          <ul>
            <li>1&#xFF1A;&#x662F;</li>
            <li>0&#xFF1A;&#x5426;</li>
          </ul>
        </td>
        <td style="text-align:center"></td>
    </tr>
  </tbody>
</table>

## 异常

### 例子

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "error": {
    "code": -32700,
    "message": "Parse error"
  }
}
```

### 错误码

| code   | message          | 解释                                                          |
| :----- | :--------------- | :------------------------------------------------------------ |
| -32700 | Parse error      | 服务端接收到无效的 JSON。该错误发送于服务器尝试解析 JSON 文本 |
| -32600 | Invalid Request  | 发送的 JSON 内容不是一个有效的请求对象                        |
| -32601 | Method not found | 该方法不存在或无效                                            |
| -32602 | Invalid params   | 无效的方法参数                                                |
| -32603 | Internal error   | JSON-RPC 内部错误                                             |
