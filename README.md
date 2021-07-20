# 简介

## 简介

* [简介](./#简介)
* [1. changelog](./#1-changelog)
* [2. Dobotlink 功能表](./#2-dobotlink-功能表)
  * [2.1. 模块平台支持表](./#21-模块平台支持表)
  * [2.2. 教育版开发节点表](./#22-教育版开发节点表)
  * [2.3. 工业版开发节点表](./#23-工业版开发节点表)
* [3. 框架图](./#3-框架图)
* [4. 工业插件类图](./#4-工业插件类图)

## 1. changelog

## 2. Dobotlink 功能表

* 已支持: ✅
* 开发中: 🚧
* 不支持: ❌

### 2.1. 模块平台支持表

| 模块 | Windows | MacOS | Linux | Android | iOS | Embed Linux\(Qt5.6\) | Chromebook | 教育版本 | 工业版本 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 主框架 | ✅ | ✅ | ✅ | 🚧 | ❌ | ✅ | 🚧 | ✅ | ✅ |
| MagicianPlugin\(弃用\) | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| M1Plugin\(弃用\) | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| MircobitPlugin\(弃用\) | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Protocol3.0Plugin\(弃用\) | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ |
| MagicDevicePlugin\(包含 P3\) | 🚧 | 🚧 | 🚧 | ❌ | ❌ | ❌ | 🚧 | ✅ | ❌ |
| ArdiunoPlugin | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ |
| DownloadPlugin\(未使用\) | 🚧 | 🚧 | 🚧 | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ |
| IndustrialPlugin | ✅ | ❌ | ❌ | 🚧 | ❌ | ❌ | ❌ | ❌ | ✅ |
| PythonDebuggerPlugin | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |
| LuaDebuggerPlugin | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ✅ |
| DynamicPlugin | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |
| AIPlugin | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ |

### 2.2. 教育版开发节点表

| 版本 | 控制 Magic 系列 | 更新 M | 更新 MB/ML | 控制 MG | 更新 MG | 图像分割识别 | 脱机\(AIStarter\) | 在线/脱机 M | 在线 MB/ML | 在线 MG | 节点 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Windows | ✅ | 🚧 | 🚧 | 🚧 | 🚧 | ✅ | ✅ | ✅ | ✅ | 🚧 | 2020 年 10 月 |
| MacOS | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | 无 |
| Chromebook | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | 无 |

### 2.3. 工业版开发节点表

| 版本 | 控制 M1 | 在线 M1 | M1 动态算法 | 控制工业设备 | 在线工业设备 | 脱机工业设备 | 节点 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Windows | ✅ | ✅ | ✅ | 🚧 | 🚧 | 🚧 | 2020 年 10 月 |
| Android | ❌ | ❌ | ❌ | 🚧 | 🚧 | 🚧 | 2020 年 11 月 |
| Embed Linux | ❌ | ❌ | ❌ | 🚧 | 🚧 | 🚧 | 2020 年 12 月 |

## 3. 框架图

```json
@startuml
!includeurl https://raw.githubusercontent.com/RicardoNiepel/C4-PlantUML/release/1-0/C4_Component.puml

System(TencentCloud, "TencentCloud")
System(BaiduCloud, "BaiduCloud")
System(Magician, "Magician")
System(M1, "M1")
System(MagicBox, "MagicBox")
System(MagicianLite, "MagicianLite")
System(AIStarter, "AIStarter")
System(Arduino, "Arduino")
System(MobilePlatform, "MobilePlatform")
System(Microbit, "Microbit")
System(MagicianGo, "MagicianGo")
System(MagicianPro, "MagicianPro")
System(M1Pro, "M1Pro")
System(CR, "CR")

Lay_D(Magician, M1)
Lay_D(M1, MagicBox)
Lay_D(MagicBox, M1)
Lay_D(MagicBox, MagicianLite)
Lay_D(MagicianLite, AIStarter)
Lay_D(AIStarter, Arduino)
Lay_D(Arduino, MobilePlatform)
Lay_D(MobilePlatform, Microbit)

System_Boundary(DobotLink_SYS, "DobotLink System") {
    System(ArduinoSDK, "ArduinoSDK")

    Container_Boundary(DobotLink, "DobotLink") {
        Boundary(EduDevicePlugin, "教育 Device Plugin") {
            Boundary(MagicianPlugin, "Magician Plugin(弃用)", "Component") {
                Component(DobotDll, "DobotDll", "C++ Qt", "Magician通讯模块")
            }
            Boundary(M1Plugin, "M1 Plugin(弃用)", "Component") {
                Component(DobotM1Dll, "DobotM1Dll", "C++ Qt", "M1通讯模块")
            }
            Boundary(MagicDevicePlugin, "Magic Devic Plugin", "Component") {
                Boundary(MagicDeviceDll, "Magic Devic Dll", "Component") {
                    Component(MagicianProtocol, "Magician 协议", "C++ Qt", "协议栈框架")
                    Component(Procotol3Framwork, "Procotol3Framwork", "C++", "协议栈框架")

                    Lay_D(MagicianProtocol, Procotol3Framwork)
                }
            }
            Component(ArduinoPlugin, "Arduino Plugin", "C++ Qt", "Arduino插件")
            Component(MicrobitPlugin, "Microbit Plugin", "C++ Qt", "Microbit插件")
            Component(Procotol3Plugin, "Procotol3 Plugin(弃用)", "C++ Qt", "Procotol3协议插件")

            Lay_D(Procotol3Framwork, MagicianPlugin)
            Lay_D(MagicianPlugin, M1Plugin)
            Lay_D(M1Plugin, ArduinoPlugin)
            Lay_D(ArduinoPlugin, MicrobitPlugin)
            Lay_D(MicrobitPlugin, Procotol3Plugin)

            Rel_R(MagicianProtocol, Magician, "通讯", "Serial UDP")
            Rel_R(MagicianProtocol, M1, "通讯", "Serial UDP")
            Rel_R(MagicianProtocol, MagicBox, "通讯", "Serial BLE")
            Rel_R(MagicBox, MagicianLite, "通讯")
            Rel_R(MagicBox, MagicianGo, "通讯")

            Rel_R(ArduinoPlugin, ArduinoSDK, "IPC")
            Rel_R(ArduinoSDK, AIStarter, "下载")
            Rel_R(ArduinoSDK, Arduino, "下载")
            Rel_R(ArduinoSDK, MobilePlatform, "下载")

            Rel_R(MicrobitPlugin, Microbit, "通讯")
            Lay_L(MicrobitPlugin, Microbit)

            Rel_R(Procotol3Framwork, MagicBox, "通讯", "Serial BLE")
        }

        Boundary(IncDevicePlugin, "工业 Device Plugin") {
            Component(IndustrialRobotPlugin, "Industrial Robot Plugin", "C++ Qt", "IndustrialRobot插件")
            Component(LibCurl, "LibCurl", "C++", "高性能网络通讯库")

            Lay_D(Procotol3Plugin, IndustrialRobotPlugin)
            Rel_R(IndustrialRobotPlugin, LibCurl, "依赖")

            Rel_R(LibCurl, MagicianPro, "通讯", "HTTP")
            Rel_R(LibCurl, M1Pro, "通讯", "HTTP")
            Rel_R(LibCurl, CR, "通讯", "HTTP")
        }

        Boundary(FuncPlugin, "Function Plugin") {
            Component(PythonDebuggerPlugin, "Python Debug Plugin", "C++ Qt", "Python调试插件")
            Boundary(LuaDebuggerPlugin, "Lua Debug Plugin", "Component") {
                Component(LuaInterpreter, "LuaInterpreter", "C", "Lua 解析器")
            }
            Component(AIPlugin, "AI Plugin", "C++ Qt", "AI")
            Component(DynamicPlugin, "Dynamic Plugin", "C++ Qt", "Dynamic算法插件")
            Component(DownloadPlugin, "Download Plugin", "C++ Qt", "固件下载插件")
        }

        Lay_D(PythonDebuggerPlugin, AIPlugin)
        Lay_D(AIPlugin, DynamicPlugin)
        Lay_D(DynamicPlugin, LuaDebuggerPlugin)
        Lay_D(LuaDebuggerPlugin, DownloadPlugin)
    }

    Component(DobotRPC, "DobotRPC", "Python websocket", "RPC模块")

    Container_Boundary(Debugger, "Debugger") {
        Component(DobotEDU, "DobotEDU", "Python OpenCV", "教育开发SDK")
    }
    Container(AI, "PyImageOM", "Python OpenCV sk-learn", "图像识别应用")
    Container(Dynamic, "DynamicAlgorithmRPC", "Python PDB", "动态参数计算应用")
    Container(Mcuisp, "Mcuisp", "Qt qml C++", "Magician固件下载应用")
    Container(DFU, "DFU", "C++", "MagicBox MagicianLite固件下载应用")

    Lay_R(DobotEDU, DobotRPC)
    Lay_L(PythonDebuggerPlugin, Debugger)
    Lay_R(DobotRPC, AI)
    Lay_D(DobotEDU, Dynamic)
    Lay_D(Dynamic, Mcuisp)
    Lay_D(Mcuisp, DFU)

    Rel_L(AI, DobotRPC, "依赖")
    Rel_L(Dynamic, DobotRPC, "依赖")

    Rel_R(PythonDebuggerPlugin, Debugger, "通讯", "IPC")
    Rel_R(AIPlugin, AI, "通讯", "IPC")
    Rel_R(DynamicPlugin, Dynamic, "通讯", "IPC")
    Rel_R(DownloadPlugin, Mcuisp, "通讯", "IPC")
    Rel_R(DownloadPlugin, DFU, "通讯", "IPC")

    Rel_U(DobotEDU, TencentCloud, "通讯", "HTTP")
    Rel_U(DobotEDU, BaiduCloud, "通讯", "HTTP")
    Rel_L(DobotEDU, DobotRPC, "依赖")
}

@enduml
```

## 4. 工业插件类图

```json
@startuml
interface DPluginInterface {
}
class IndustrialRobotPlugin {
    - m_requestPacketMap: QMap<quint64, DRequestPacket>
    - m_device: Device
}
class Module {
    - QString m_ip;
    - CurlNetworkManager *m_crulManager;
}
class FileControll {
    - QString m_ip;
    - QThreadPool m_pool;
}
class Device {
    - RobotStatus m_status;
    - Module *m_module;
    - FileControll *m_fileControll;
    - quint16 m_wsPort;
    - bool m_isConnectedQMap<QString, QString> m_selfExchangeFunMap;
    - QMap<QString, APIFunction> m_FuncMap;
    - QMap<quint64, QJsonObject> m_requestMap;
    - QMap<quint64, QEventLoop*> m_eventloopMap;
}

FileControll *--> QThreadPool: 1..1
FileControll ..> Thread: 1..n
Module o--> CurlNetworkManager
Device o-u-> RobotStatus
Device *-u-> Module
Device *-u-> Mobdebug
Device *-u-> FileControll: 1..1
IndustrialRobotPlugin .u.|> DPluginInterface
IndustrialRobotPlugin o-u-> Device
@enduml
```

