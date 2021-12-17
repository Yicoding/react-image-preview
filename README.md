# react-image-viewer

[![npm][npm]][npm-url] ![GitHub](https://shopmushi.com/configFile/assets/mit.svg)

基于`react`的图片预览组件，兼容 PC、移动端

[查看文档和示例][site]

## 使用

### npm 或 yarn 安装

```shell
npm install @eco/react-image-viewer
# or
yarn add @eco/react-image-viewer
```

### 示例

```javascript
import React, { useState } from 'react';
import ImageViewer from '@eco/react-image-viewer';

type FileItem = {
  url: string, // 图片url
  loading?: boolean, // 图片是否加载中
  errorTip?: string, // 错误提示
  name?: string, // 文件说明
  fileName?: string, // 文件名称,包含后缀
  [index: string]: any
};

export default () => {
  const [value, setValue] = useState<FileItem[]>([]);

  // 数组改变
  const onChange = (arr: FileItem[]) => setValue(arr);

  return <ImageViewer index={index} urls={urls} onClose={onClose} />;
};
```

[npm]: https://img.shields.io/npm/v/react-image-viewer.svg
[site]: https://yicoding.github.io/react-image-viewer
