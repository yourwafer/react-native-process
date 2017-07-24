如果使用react-native-navigation作为页面切换组件，需要注意与React-Native的版本切换

```
"react-native": "0.45.1",
"react-native-navigation": "^1.1.136",
```

在使用上面navigation版本时，react-native版本不能高于0.45.1，否则会报异常，错误大概是‘can't render any thing on top frame’



