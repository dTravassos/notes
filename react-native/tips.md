# Tips
### Embedded internal librarys in outher projects

To create package with project name, run yarn: 
```
my-commons > yarn pack
```

To use in project, add reference to package.json
```
...
"my-commons": "file:./local-lib-path/my-commons-v1.1.0.tgz",
...
```

To use in development:
```
"my-commons": "../repo-path/my-commons",
```

### When generate android apk without react-run command to avoid assest/js not found error, customize package.json scrits to build with:
```
react-native bundle --platform android --dev false --entry-file index.android.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res
```

### Configuring adb system variables to run on android (MAC), on .bash_profile
```
export ANDROID_HOME=/Users/user.name/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
```
