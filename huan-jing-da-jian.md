# 搭建开发环境

参考

React Native中文网 [https://reactnative.cn/docs/0.46/getting-started.html](https://reactnative.cn/docs/0.46/getting-started.html)

官网[https://facebook.github.io/react-native/docs/getting-started.html](https://facebook.github.io/react-native/docs/getting-started.html)

这两个初始化项目的方式有所不同中文网使用**react-native init &lt;ProjectName&gt;**，官网使用**create-react-native-app &lt;ProjectName&gt;**，两种方式差别蛮大，但官网上面说的蛮清楚，意思就是可以让你尽快的运行一个React Native的项目，而不需要安装xcode和android sdk。

## 区别

1. 中文网提供完整的环境搭建过程，包括基础软件的安装\(Node,npm,yarn\)；
2. 官网安装的前提是你已经有了基础软件，所以仅仅教你安装npm install -g create-react-native-app
3. 官网的目的是快速构建起环境，create-react-native-app运行结果会在[Expo](https://expo.io/)软件中运行，所以更简单
4. 中文网react-native init初始化的项目包括完整的XCode项目文件以及Android gradle项目构建文件，所以后续打包成Apk，ipa更合适

所以，想快速看见效果的，可以使用官网的方式，但前期如果有第三方Demo，他们使用的方式基本都是中文网方式，所以，最终还是需要安装。

