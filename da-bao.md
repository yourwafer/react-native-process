# Android打包

 react-native@0.45.1版本

1. 使用Android Studio生成加密key，将生成的文件放入android/app目录，路由不强制，可在下面文件中输入路径![](/assets/p1.png)



 2. 跟着步骤创建Key，记住别名与密码，在android/gradle.properties中添加一下内容

```
MYAPP_RELEASE_STORE_FILE=<your file name>.jks
MYAPP_RELEASE_KEY_ALIAS=<you alias name>
MYAPP_RELEASE_STORE_PASSWORD=<your password>
MYAPP_RELEASE_KEY_PASSWORD=<your password>
```

3. 在android/app/build.gradle中添加如下signingConfigs内容

```
    defaultConfig {
        ...
        ...
        ...
    }
    signingConfigs {
        release {
            if (project.hasProperty('MYAPP_RELEASE_STORE_FILE')) {
                storeFile file(MYAPP_RELEASE_STORE_FILE)
                storePassword MYAPP_RELEASE_STORE_PASSWORD
                keyAlias MYAPP_RELEASE_KEY_ALIAS
                keyPassword MYAPP_RELEASE_KEY_PASSWORD
            }
        }
    }
    buildTypes {
        release {
                ...
                ...
               signingConfig signingConfigs.release
        }
    }
```

4. 在react-native@0.45.1及以下，如果本项目运行过run-ios，则需要rm -rf node\_modules，具体参考[https://github.com/facebook/react-native/pull/14638](https://github.com/facebook/react-native/pull/14638)

cd android && ./gradlew assembleRelease



