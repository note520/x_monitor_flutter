# x_monitor_flutter

### 安装

```
dependencies:
  x_monitor_flutter: ^0.1.0
```
#### 使用

```
import 'package:x-monitor-flutter/x_monitor_flutter.dart';
# 入口

void main() {
  XMonitorFlutter appXMonitorFlutter = XMonitorFlutter();
  // 配置基础信息
  appXMonitorFlutter.setConfig({
    'key': 'xxx',// 应用唯一key （必填 ）
    'url':'' // 指定错误上报地址 （必填 ）
    'performanceUrl':'',// 性能数据上报地址（可选 ）
    'userId':'',// 生成guid规则（可选 ）
    'guid':''// userId（可选 ）
  });
  // 获取gps 以及 flutterSDK 基础版本库
  appXMonitorFlutter.setReportSystemOption(locationInfo: {'latitude': 10, 'longitude': 10},frameVersion: '0.1.5');

  return appXMonitorFlutter.catchRun((){
    runApp(MyApp());
  });
}