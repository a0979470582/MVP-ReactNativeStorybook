# MVP-ReactNativeStorybook
React Native Storybook 的最小可行性測試(MVP)。

## Create React Native Project
首先需要一個 React Native 專案。如果已經有現有專案，可以略過此步驟。

以下步驟是建立此 React Native 專案的紀錄。隨版本迭代可能有所不同，建議參考 [官方文件](https://reactnative.dev/docs/environment-setup) 來自行建立。

<br>在 Github 建立一個 Repo，名稱為 MVP_ReactNativeStorybook。

<br>在本地命令列中輸入以下指令來建立專案
```
cd ~
react-native init MVP_ReactNativeStorybook
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

// 如果 repo 已經有一些 commit，可能會無法從 local push 到 repo。請執行：
git fetch
git rebase origin/main
git push
```

