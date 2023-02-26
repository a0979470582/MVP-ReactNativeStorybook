# MVP-ReactNativeStorybook
React Native Storybook 的最小可行性測試(MVP)。

## Create React Native Project
首先需要一個 React Native 專案。如果已經有現有專案，可以略過此步驟。

以下步驟是建立此 React Native 專案的紀錄。隨版本迭代可能有所不同，建議參考 [官方文件](https://reactnative.dev/docs/environment-setup) 來自行建立。

<br>在 Github 建立一個 Repo，名稱為 MVP_ReactNativeStorybook。

<br>在本地命令列中輸入以下指令來建立專案
```
cd ~
npx react-native init MVP_ReactNativeStorybook
cd MVP_ReactNativeStorybook
```

<br>初始化 git 並連結到 Githup Repo。
```
git init
git add .
git commit -m 'init project'
git branch -M main // 移動和重命名分支(-M 比起 -m 會在分支不存在時強制移動)
git remote add origin git@github.com:a0979470582/MVP_ReactNativeStorybook.git
git push --set-upstream origin main
```

<br>在本地運行專案(Android 手機)
```
adb reverse tcp:8081 tcp:8081
npm start
在 Android Studio 上運行專案 
```

## Install React Native Storybook
接下來的流程是參考自 [ReactNativeStorybook 手動安裝文件](https://github.com/storybookjs/react-native/blob/next-6.0/MANUAL_SETUP.md)

<br>安裝所需依賴項

```
yarn add -D @storybook/react-native@next @storybook/core-common @react-native-async-storage/async-storage react-native-safe-area-context react-dom
```

<br>建立 .storybook 資料夾並建立一些預設檔案


