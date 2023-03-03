# MVP-ReactNativeStorybook
React Native Storybook Minimum Viable Product(MVP, 最小可行產品) Testing。

This repository records my integrating react-native-storybook process.

<br>[Create React Native Project](#Create-React-Native-Project)
<br>[Install React Native Storybook](#Install-React-Native-Storybook)
<br>[Run Storybook](#Run-Storybook)

## Create React Native Project
First, you need a React Native Project. If you have, please skip the step.
<br>首先需要一個 React Native 專案。如果已經有現有專案，可以略過此步驟。
<br><br>[CreateReactNativeProject.md](https://github.com/a0979470582/MVP_ReactNativeStorybook/blob/main/CreateReactNativeProject.md)

## Install React Native Storybook
Next step is refer to [ReactNativeStorybook manual setup](https://github.com/storybookjs/react-native/blob/next-6.0/MANUAL_SETUP.md).
<br>接下來的流程是參考自 [ReactNativeStorybook 手動安裝文件](https://github.com/storybookjs/react-native/blob/next-6.0/MANUAL_SETUP.md)。

<br>Install required dependecies. 
<br>安裝所需依賴項。

```
yarn add -D @storybook/react-native@next @storybook/core-common @react-native-async-storage/async-storage react-native-safe-area-context react-dom
```

<br>create .storybook folder and some config files. 
<br>建立 .storybook 資料夾及一些配置檔案
```
mkdir .storybook && cd .storybook && touch main.js preview.js Storybook.tsx
```

<br>main.js
```
module.exports = {
  stories: [
    '../components/**/*.stories.?(ts|tsx|js|jsx)'
  ],
  addons: [],
};
```

<br>preview.js
```
export const decorators = [];
export const parameters = {};
```

<br>Storybook.tsx
```
import { getStorybookUI } from '@storybook/react-native';

import './storybook.requires';

export const StorybookUIRoot = getStorybookUI({});
```

<br>Revise metro.config.js
```
module.exports = {
  /* existing config */
  resolver: {
    resolverMainFields: ['sbmodern', 'react-native', 'browser', 'main'],
  },
};
```

<br>Revise package.json
```
{
  "scripts": {
    "prestart": "sb-rn-get-stories",
    "storybook-watcher": "sb-rn-watcher",
  }
}
```

<br>Create a Story at /MVP_ReactNativeStorybook/components/Button/Button.stories.tsx
```
import {Button} from 'react-native';

export default {
  title: 'React Native Button',
  component: Button,
  args: {
    title: 'Hello world',
  },
};

export const Basic = args => <Button {...args} />;
```

<br>到目前為止準備工作就算完成了，接下來將運行看看。
<br>So far the pre-work is complete, and then we will run storybook on the phone.


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


