## Create React Native Project
<br>Step at below are records that create RN project. May different by RN version, Recommended refer to [Official Document](https://reactnative.dev/docs/environment-setup) to create self.
<br>以下步驟是建立此 React Native 專案的紀錄。隨版本迭代可能有所不同，建議參考 [官方文件](https://reactnative.dev/docs/environment-setup) 來自行建立。 

<br>Create a repo in Github. in my case, the repo name is MVP_ReactNativeStorybook。
<br>在 Github 建立一個名稱為 MVP_ReactNativeStorybook 的 Repo。

<br>Create RN project in command line. 
<br>在本地命令列中輸入以下指令來建立專案
```
cd ~
npx react-native init MVP_ReactNativeStorybook
cd MVP_ReactNativeStorybook
```

<br>Init git and link to Github Repo. 
<br>初始化 git 並連結到 Github Repo。
```
git init
git add .
git commit -m 'init project'
git branch -M main // 移動和重命名分支(-M 比起 -m 會在分支不存在時強制移動)
git remote add origin git@github.com:a0979470582/MVP_ReactNativeStorybook.git
git push --set-upstream origin main
```

## Run on Android physical device
```
adb reverse tcp:8081 tcp:8081
npm start
(press keyboard a) or (run Project in Android Studio)
```

## Run on Android emulator device
```
npm start
(press keyboard a) or (run Project in Android Studio)
```

## Run on iOS 
```
npm start
(press keyboard i) or (run Project in XCode)
```

