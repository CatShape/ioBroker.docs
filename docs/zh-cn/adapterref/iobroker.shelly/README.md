---
BADGE-NPM version: https://img.shields.io/npm/v/iobroker.shelly?style=flat-square
BADGE-Downloads: https://img.shields.io/npm/dm/iobroker.shelly?label=npm%20downloads&style=flat-square
BADGE-Snyk Vulnerabilities for npm package: https://img.shields.io/snyk/vulnerabilities/npm/iobroker.shelly?label=npm%20vulnerabilities&style=flat-square
BADGE-node-lts: https://img.shields.io/node/v-lts/iobroker.shelly?style=flat-square
BADGE-Libraries.io dependency status for latest release: https://img.shields.io/librariesio/release/npm/iobroker.shelly?label=npm%20dependencies&style=flat-square
BADGE-GitHub: https://img.shields.io/github/license/iobroker-community-adapters/iobroker.shelly?style=flat-square
BADGE-GitHub repo size: https://img.shields.io/github/repo-size/iobroker-community-adapters/iobroker.shelly?logo=github&style=flat-square
BADGE-GitHub commit activity: https://img.shields.io/github/commit-activity/m/iobroker-community-adapters/iobroker.shelly?logo=github&style=flat-square
BADGE-GitHub last commit: https://img.shields.io/github/last-commit/iobroker-community-adapters/iobroker.shelly?logo=github&style=flat-square
BADGE-GitHub issues: https://img.shields.io/github/issues/iobroker-community-adapters/iobroker.shelly?logo=github&style=flat-square
BADGE-GitHub Workflow Status: https://img.shields.io/github/workflow/status/iobroker-community-adapters/iobroker.shelly/Test%20and%20Release?label=Test%20and%20Release&logo=github&style=flat-square
BADGE-Snyk Vulnerabilities for GitHub Repo: https://img.shields.io/snyk/vulnerabilities/github/iobroker-community-adapters/iobroker.shelly?label=repo%20vulnerabilities&logo=github&style=flat-square
BADGE-Beta: https://img.shields.io/npm/v/iobroker.shelly.svg?color=red&label=beta
BADGE-Stable: http://iobroker.live/badges/shelly-stable.svg
BADGE-Installed: http://iobroker.live/badges/shelly-installed.svg
chapters: {"pages":{"de/adapterref/iobroker.shelly/README.md":{"title":{"de":"ioBroker.shelly"},"content":"de/adapterref/iobroker.shelly/README.md"},"de/adapterref/iobroker.shelly/protocol-coap.md":{"title":{"de":"ioBroker.shelly"},"content":"de/adapterref/iobroker.shelly/protocol-coap.md"},"de/adapterref/iobroker.shelly/protocol-mqtt.md":{"title":{"de":"ioBroker.shelly"},"content":"de/adapterref/iobroker.shelly/protocol-mqtt.md"},"de/adapterref/iobroker.shelly/restricted-login.md":{"title":{"de":"ioBroker.shelly"},"content":"de/adapterref/iobroker.shelly/restricted-login.md"},"de/adapterref/iobroker.shelly/state-changes.md":{"title":{"de":"ioBroker.shelly"},"content":"de/adapterref/iobroker.shelly/state-changes.md"},"de/adapterref/iobroker.shelly/faq.md":{"title":{"de":"ioBroker.shelly"},"content":"de/adapterref/iobroker.shelly/faq.md"},"de/adapterref/iobroker.shelly/debug.md":{"title":{"de":"ioBroker.shelly"},"content":"de/adapterref/iobroker.shelly/debug.md"}}}
translatedFrom: de
translatedWarning: 如果您想编辑此文档，请删除“translatedFrom”字段，否则此文档将再次自动翻译
editLink: https://github.com/ioBroker/ioBroker.docs/edit/master/docs/zh-cn/adapterref/iobroker.shelly/README.md
title: ioBroker.shelly
hash: Iwa5+l+GwmBWVyl3ynhqpkVVK5VdE7bz/5Qu6fQRnK4=
---
![商标](../../../de/admin/shelly.png)

# IoBroker.shelly
这是德语文档 - [🇺🇸德文版](../en/README.md)

＃＃ 目录
- [MQTT协议](协议-mqtt.md)
- [CoAP 协议](协议-coap.md)
- [限制登录](restricted-login.md)
- [状态变化](state-changes.md)
- [调试](debug.md)
- [FAQ](faq.md)

＃＃ 要求
1.nodejs 14.5（或更新版本）
2. js 控制器 3.3.22（或更新版本）
4. Admin Adapter 6.0.0（或更新版本）

## 设备世代
有关详细信息，请参阅*支持的设备*。

- **Gen1**：ESP8266 设备，[CoAP](protocol-coap.md) 或 [MQTT](protocol-mqtt.md)
- **Gen2**：ESP32 设备，[MQTT](protocol-mqtt.md)

＃＃ 一般的
适配器可以通过 CoAP 或 MQTT 与设备通信。

- 默认模式为 MQTT（请参阅 [文档](protocol-mqtt.md) 了解更多信息）
- CoAP 仅与第一代设备兼容！
- **如果要集成Gen2设备，必须配置MQTT！**

问题？先看[常问问题](faq.md)！

![iobroker_general](../../../de/adapterref/iobroker.shelly/img/iobroker_general.png)

## Changelog

<!--
  Placeholder for the next version (at the beginning of the line):
  ### **WORK IN PROGRESS**
-->
### 6.3.1 (2023-01-02)

* (klein0r) Updated MQTT topic prefix handling
* (klein0r) Added temperature for generation 2 devices in cover mode
* (klein0r) Added boost start/stop for Shelly TRV
* (klein0r) Added external power for Shelly H&T

### 6.3.0 (2022-12-22)

* (klein0r) Added more TRV features
* (jlegen) Improved Shelly TRV integration
* (klein0r) Updated knowledge base urls
* (klein0r) Added Ukrainian language

### 6.2.4 (2022-10-23)

* (klein0r) IP address of CoAP devices is unknown in some cases
* (klein0r) Optimized destroy process

### 6.2.3 (2022-10-20)

* (klein0r) Use unique ID for each command - generation 2 devices
* (klein0r) Fix: Ack state if value is unchanged

### 6.2.2 (2022-10-13)

* (klein0r) Fixed state updates for CoAP integration

## License

The MIT License (MIT)

Copyright (c) 2018-2023 Thorsten Stueben <thorsten@stueben.de>,
                        Apollon77 <iobroker@fischer-ka.de> and
                        Matthias Kleine <info@haus-automatisierung.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.