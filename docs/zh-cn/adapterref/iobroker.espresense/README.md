---
translatedFrom: en
translatedWarning: 如果您想编辑此文档，请删除“translatedFrom”字段，否则此文档将再次自动翻译
editLink: https://github.com/ioBroker/ioBroker.docs/edit/master/docs/zh-cn/adapterref/iobroker.espresense/README.md
title: ioBroker.espresense
hash: YfSlw/wfFF0mq1sD35u0lZ8HzOtgsGlp/N4k3LJMzvo=
---
![标识](../../../en/adapterref/iobroker.espresense/admin/espresense.png)

![NPM版本](https://img.shields.io/npm/v/iobroker.espresense.svg)
![下载](https://img.shields.io/npm/dm/iobroker.espresense.svg)
![安装数量](https://iobroker.live/badges/espresense-installed.svg)
![稳定存储库中的当前版本](https://iobroker.live/badges/espresense-stable.svg)
![国家公共管理](https://nodei.co/npm/iobroker.espresense.png?downloads=true)

# IoBroker.espresense
**测试：** ![测试与发布](https://github.com/ticaki/ioBroker.espresense/workflows/Test%20and%20Release/badge.svg)

## IoBroker 的 espresense 适配器
连接到[ESPRESENSE](https://espresense.com)

- MQTT服务器和客户端模式
- `启动自己的 mqtt 服务器`激活服务器模式
- `服务器 IP` 仅用于外部 mqtt 服务器
- 内部或外部 mqtt 服务器的“端口、用户名和密码”

- 如果设备已添加到配置中，则只有这些设备才会显示在对象中。

最佳实践：将要监控的设备与 espresense 配对并过滤输出以避免不必要的网络流量。

如需帮助使用问题或如果您了解德语 https://forum.iobroker.net/topic/71189/test-adapter-espresense

* 使用的 mqtt-server 是完全兼容 MQTT 3.1 和 3.1.1 服务器，但适配器仅响应主题 espresense/#

## Changelog
<!--
    Placeholder for the next version (at the beginning of the line):
    ### **WORK IN PROGRESS**
-->
### 0.4.1 (2023-12-30)
* (ticaki) fixed: no names. (2. try)

### 0.4.0 (2023-12-30)
* (ticaki) fixed: no names.
* (ticaki) Added: global esp32 configuration (retained)

### 0.3.0 (2023-12-23)
* (ticaki) Breaking Change: move datadir from node_modules/iobroker.espresense/mydp to iobroker-data/espresense.0 (instance). move the files there and use iobroker fix after it.

### 0.2.1 (2023-12-21)
* (ticaki) fixed: object not exist sometimes.

### 0.2.0 (2023-12-21)
* (ticaki) Add/Remove Devices

### 0.1.3 (2023-12-21)
* (ticaki) prepare for lastest

### 0.1.2 (2023-12-21)
* (ticaki) add common.name to states

### 0.1.1 (2023-12-20)
* (ticaki) fixed: sometimes adapter crashed after login.

### 0.1.0 (2023-12-20)
* (ticaki) Added: send configuration datapoints to esp

### 0.0.3 (2023-12-19)
* (ticaki) Added: Mqtt Server with file db

### 0.0.2 (2023-12-18)
* (ticaki) initial release

## License
MIT License

Copyright (c) 2023 ticaki <github@renopoint.de>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.