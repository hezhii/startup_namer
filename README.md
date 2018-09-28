# startup_namer

根据 [Flutter 官网](https://flutter.io/get-started/codelab/)上的教程编写的 Flutter App。

使用 IntelliJ IDEA 作为开发工具，测试时使用的是 iOS 模拟器（iPhone X）。

相关资源：[Dart 中文网](http://dart.goodev.org/) [Flutter 中文网](https://flutterchina.club/) [开源软件包](https://pub.dartlang.org/flutter/)

## 如何使用

克隆代码到本地：
```bash
$ git clone https://github.com/hezhii/startup_namer.git
```

运行应用程序：

1. 查看当前可运行的设备列表。
    ```bash
    $ flutter devices
    ```

2. 在指定设备上运行。
    ```bash
    $ cd startup_namer
    $ flutter run -d device-id
    ```

## 知识点

* 在 Flutter 中，大多数都是控件（widget），包括对齐(alignment)、填充(padding)和布局(layout)，对应 React 中的组件。
* widget 主要工作是提供一个 `build()` 方法来描述如何根据其他较低级别的 widget 来显示自己，对应 React 中的 `render()` 方法。
* `pubspec.yaml` 文件管理 Flutter App 的静态资源和依赖，对应 Node.js 中的 `package.json`，使用 `flutter package get` 安装配置文件中的依赖。
* 安装依赖会生成 `pubspec.lock` 文件，对应 `package-lock.json` 或 `yarn.lock`。
* 导入内置库：`import dart:scheme`；导入第三方库：`import package:scheme`；导入本地文件，使用文件系统路径。
* 控件分为有状态和无状态，对应 React 中两种创建组件的方式：class 和函数。控件状态是一个 State 类的实例。
* State 也需要实现 `build` 方法并返回一个控件，感觉和控件有点类似。
* 调用 `setState()` 函数触发更新，参数是一个函数，在函数里面可以直接修改状态对象的属性。
* Flutter 中使用 Navigator 管理路由栈。将路由 push 到栈中，将会显示该路由页面。弹出路由，则显示前一个页面。
* 控件的 `build()` 函数接受一个 `BuildContext` 对象；State 对象拥有 `context` 成员变量。
