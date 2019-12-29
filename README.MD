# Flutter插件：flutter_webview_plugin

在下面代码后
dependencies:
  flutter:
    sdk: flutter

添加依赖
  flutter_webview_plugin: ^0.3.0

# main.dart中导入包
#
```
import 'package:flutter_webview_plugin/flutter_webview_plugin.dart';
```

# iOS Http支持
#
iOS端info.plist配置，AndroidStudioProjects/flutter_app_webview/ios/Flutter/AppFrameworkInfo.plist

其中NSAppTransportSecurity节点是为了支持http协议

```
<key>io.flutter.embedded_views_preview</key>
    <true/>
<key>NSAppTransportSecurity</key>
    <dict>
        <key>NSAllowsArbitraryLoads</key>
        <true/>
    </dict>
```

# main.dart是webview的代码

通过把适配移动端的网页嵌入到只可以打开一个url的flutter中可以实现跨平台的伪移动端
