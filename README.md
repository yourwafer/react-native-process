# 开发介绍

使用React和Javascript开发Native App

```
import React, { Component } from 'react';
import { Text, View } from 'react-native';

class WhyReactNativeIsSoGreat extends Component {
  render() {
    return (
      <View>
        <Text>
          If you like React on the web, you'll like React Native.
        </Text>
        <Text>
          You just use native components like 'View' and 'Text',
          instead of web components like 'div' and 'span'.
        </Text>
      </View>
    );
  }
}
```

使用React Native时，你不是在构建一个手机Web应用，不是一个HTML5应用，也不是一个Hybrid应用。你构建的是一个使用Objective-C或java的原生应用。React-native使用的是原生基础组件，只是你用的是React把它们表现出来。

```
import React, { Component } from 'react';
import { Image, ScrollView, Text } from 'react-native';

class AwkwardScrollingImageWithText extends Component {
  render() {
    return (
      <ScrollView>
        <Image source={{uri: 'https://i.chzbgr.com/full/7345954048/h7E2C65F9/'}} />
        <Text>
          在IOS上 ScrollView使用原生的UIScrollView.
          在Android上使用ScrollView.

          On iOS, a React Native Image uses a native UIImageView.
          On Android, it uses a native ImageView.
        </Text>
      </ScrollView>
    );
  }
}
```



