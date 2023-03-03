# MVP-ReactNativeStorybook
React Native Storybook Minimum Viable Product(MVP, 最小可行產品) Testing。

This repository records my integrating react-native-storybook process.

<br>[Create React Native Project](#Create-React-Native-Project)
<br>[Install React Native Storybook](#Install-React-Native-Storybook)
<br>[Run Storybook](#Run-Storybook)
<br>[Issue](#Issue)
<br>[Optimize Storybook](#Optimize-Storybook)

## Create React Native Project
First, you need a React Native Project. If you have, please skip the step.
<br>首先需要一個 React Native 專案。如果已經有現有專案，可以略過此步驟。
<br><br>[CreateReactNativeProject.md](https://github.com/a0979470582/MVP_ReactNativeStorybook/blob/main/CreateReactNativeProject.md)

## Install React Native Storybook
Next step is refer to [ReactNativeStorybook manual setup](https://github.com/storybookjs/react-native/blob/next-6.0/MANUAL_SETUP.md).
<br>接下來的流程是參考自 [ReactNativeStorybook 手動安裝文件](https://github.com/storybookjs/react-native/blob/next-6.0/MANUAL_SETUP.md)。
<br><br>[InstallReactNativeStorybook.md](https://github.com/a0979470582/MVP_ReactNativeStorybook/blob/main/InstallReactNativeStorybook.md)


## Run Storybook
Use <StorybookUIRoot /> element In App.tsx
```
import {StorybookUIRoot} from './.storybook/Storybook';

function App(): JSX.Element {
  return <StorybookUIRoot />;
}
```

<br>Execute command to update Sotrybook
```
yarn sb-rn-get-stories
```

<br>Re-run Android Studio

<br>Check Storybook on the phone
<br><image src="https://user-images.githubusercontent.com/45554149/221398084-943c29d8-91dc-44a7-9808-86ea1ec39cb2.jpg" width="200px"/>

## Issue
1. How can I do when I see the error 'Error loading story index'?
Need reset cache.
```
yarn start -- --reset-cache
```

## Optimize Storybook
To be continued

