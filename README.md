# ReactNativeDemo
react-native 初体验

遇到的问题

1，sdk没有配置需要在android目录下添加一个local.properties的文件夹里面的具体内容如下


  ndk.dir=H\:\\install\\sdk\\ndk-bundle
  
  sdk.dir=H\:\\install\\sdk

2.Unable to load script from assets 'index.android.bundle'.make sure you bundle is packaged correctly..... 

以下方法每次都需要执行命令2才能更新

1、创建assets目录

mkdir android/app/src/main/assets

2、执行命令

react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res/

3、重新运行 react-native run-android
