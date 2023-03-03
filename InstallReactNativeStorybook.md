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
