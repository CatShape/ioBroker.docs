---
translatedFrom: en
translatedWarning: 如果您想编辑此文档，请删除“translatedFrom”字段，否则此文档将再次自动翻译
editLink: https://github.com/ioBroker/ioBroker.docs/edit/master/docs/zh-cn/adapterref/iobroker.viessmannapi/README.md
title: ioBroker.viessmannapi
hash: rJnTMsjfbY6/GtrlBGj69mnQpu98U+RlnKn7lqTwCPw=
---
![商标](../../../en/adapterref/iobroker.viessmannapi/admin/viessmannapi.png)

![NPM 版本](https://img.shields.io/npm/v/iobroker.viessmannapi.svg)
![下载](https://img.shields.io/npm/dm/iobroker.viessmannapi.svg)
![安装数量（最新）](https://iobroker.live/badges/viessmannapi-installed.svg)
![安装数量（稳定）](https://iobroker.live/badges/viessmannapi-stable.svg)
![依赖状态](https://img.shields.io/david/TA2k/iobroker.viessmannapi.svg)
![新PM](https://nodei.co/npm/iobroker.viessmannapi.png?downloads=true)

# IoBroker.viessmannapi
**测试：** ![测试和发布](https://github.com/TA2k/ioBroker.viessmannapi/workflows/Test%20and%20Release/badge.svg)

## IoBroker 的 viessmannapi 适配器
Viessmannapi 适配器

**Man benötigt eine ClientID von der Viessmann API**

https://app.developer.viessmann.com besuchen und eine Client ID mitdiesen Optionen erstellen：

名称：iobroker

**Google reCAPTCHA deaktivieren**

网址：http://localhost:4200/

Die Client ID in die Einstellungen kopieren

**Außentemperatur findet sich z.B.层级：viessmannapi.0.XXXXX.0.features.heating.sensors.temperature.outside.properties.value.value**

**Remote Befehle sind möglich unter viessmannapi.0.XXXXX.0.features.heating.dhw.temperature.main.commands.setTargetTemperature.setValue**

**兼容性列表**：

**Regelungen für Wand-oder Kompaktgeräte**

Vitotronic 200, Typ HO1, HO1A, HO1B, HO1D, HO2B, HO2C Vitotronic 200 RF, Typ HO1C, HO1E

**Regelungen für bodenstehende Heizkessel**

Vitotronic 200, Typ KO1B, KO2B, KW6, KW6A, KW6B, KW1, KW2, KW4, KW5 Vitotronic 300, Typ KW3

**Regelungen für Wärmepumpen und Hybridgeräte**

Vitotronic 200，典型 WO1A，WO1B，WO1C

**Regelungen für Festbrennstoffkessel**

Vitoligno 200-S mit Ecotronic (ab Softwarestand 2.03) Vitoligno 250-S mit Ecotronic (ab Softwarestand 2.00) Vitoligno 300-C mit Ecotronic (ab Softwarestand 2.12) Vitoligno 300-P mit Vitotronic 200 FO1 Vitoligno 300-S mit Ecotronic (ab Softwarestand 2.04)

**列出所有数据点：https://documentation.viessmann.com/static/iot/data-points**

**Frage zu fehlende Datenpunkte bitte direkt an Viessmann https://www.viessmann-community.com/t5/The-Viessmann-API/bd-p/dev-viessmann-api**

贝斯皮勒：

```
Vorlauftemperatur:
viessmannapi.0.XXXX.features.heating.circuits.0.sensors.temperature.supply.properties.value.value,

Anzahl Zündungen:
viessmannapi.0.XXXXX.features.heating.burners.0.statistics.properties.starts.value

Betriebsstunden
viessmannapi.0.XXXXX.features.heating.burners.0.statistics.properties.hours.value

Kesseltemperatur
viessmannapi.0.XXXXX.features.heating.boiler.sensors.temperature.main.properties.unit.value

Kompressor aktiv:		viessmannapi.0.xxx.0.features.heating.compressors.0.properties.active.value
Heizkreispumpe aktiv:		viessmannapi.0.xxx.0.features.heating.circuits.1.circulation.pump.properties.status.value
Warmwasserbereitung:		viessmannapi.0.xxx.0.features.heating.dhw.charging.properties.active.value
Heizungsmodus:			viessmannapi.0.xxx.0.features.heating.circuits.1.operating.modes.active.properties.value.value
Heizprogramm:			viessmannapi.0.xxx.0.features.heating.circuits.1.operating.programs.active.properties.value.value
Temperatur Heizprogramm normal:	viessmannapi.0.xxx.0.features.heating.circuits.1.operating.programs.normal.properties.temperature.value
Temperatur Heizprogramm reduz.:	viessmannapi.0.xxx.0.features.heating.circuits.1.operating.programs.reduced.properties.temperature.value
Warmwasser Soll Temperatur:	viessmannapi.0.xxx.0.features.heating.dhw.temperature.properties.value.value
Warmwasser Ist Temperatur:	viessmannapi.0.xxx.0.features.heating.dhw.sensors.temperature.hotWaterStorage.properties.value.value
Temperatur Außensensor:		viessmannapi.0.xxx.0.features.heating.sensors.temperature.outside.properties.value.value
Statistik Kompressor Starts:	viessmannapi.0.xxx.0.features.heating.compressors.0.statistics.properties.starts.value
Statistik Kompressor Stunden:	viessmannapi.0.xxx.0.features.heating.compressors.0.statistics.properties.hours.value
Temperatursensoren der Heizkreise:   viessmannapi.0.xxxxxxx.0.features.heating.circuits.0.sensors.temperature.supply.properties.value.value

Primärkreis Vorlauftemperatur:		viessmann.0.xxx.0.features.heating.primaryCircuit.sensors.temperature.supply.properties.value.value
Sekundärkreis Vorlauftemperatur:	viessmann.0.xxx.0.features.heating.secondaryCircuit.sensors.temperature.supply.properties.value.value
Sekundärkreis Rücklauftemperatur:	viessmann.0.xxx.0.features.heating.secondaryCircuit.sensors.temperature.return.properties.value.value
?					viessmann.0.xxx.0.features.heating.sensors.temperature.return.properties.value.value

```

**Beispiel zum setzen eines 时间表：**

```
var standard = '{"mon":[{"start":"00:00","end":"24:00","mode":"standard","position":0}],"tue":[{"start":"00:00","end":"24:00","mode":"standard","position":0}],\
              "wed":[{"start":"00:00","end":"24:00","mode":"standard","position":0}],"thu":[{"start":"00:00","end":"24:00","mode":"standard","position":0}],\
              "fri":[{"start":"00:00","end":"24:00","mode":"standard","position":0}],"sat":[{"start":"00:00","end":"24:00","mode":"standard","position":0}],\
              "sun":[{"start":"00:00","end":"24:00","mode":"standard","position":0}]}'

setState("viessmannapi.0.xxxxxxx.0.features.ventilation.schedule.commands.setSchedule.setValue", JSON.parse(standard));
```

## Changelog

### 2.0.1

-   (TA2k) initial release for new API. Complete new Data objects

## License

MIT License

Copyright (c) 2022 TA2k <tombox2020@gmail.com>

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