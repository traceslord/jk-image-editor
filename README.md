# jk-image-editor  

<p>
  <img alt="JK" src="https://img.shields.io/badge/-JK-brightgreen">
  <a href="https://github.com/traceslord/jk-image-editor">
    <img alt="code size" src="https://img.shields.io/github/languages/code-size/traceslord/jk-image-editor">
  </a>
  <img alt="version" src="https://img.shields.io/github/package-json/v/traceslord/jk-image-editor">
  <a href="https://github.com/traceslord/jk-image-editor/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/traceslord/jk-image-editor" alt="license">
  </a>
</p>

> A image editor.

## Installation
注：本插件依赖到了 `element-ui` ，使用前请先下载 `element-ui` （附：[element-ui 官方文档](https://element.eleme.cn/)）
```
npm install jk-image-editor --save
```

## Usage examples
引入 `vue` 组件：
```html
<image-editor></image-editor>
```

```js
import ImageEditor from "jk-image-editor/layout/common";

export default {
  components: {
    ImageEditor
  }
};
```

也可使用自定义框架，本插件提供图片预览与下载的方法：
引入 `vue` 组件：
```html
<el-button @click="previewImage">图片预览</el-button>
<el-button @click="downloadImage">下载图片</el-button>
<image-editor
  ref="imageEditor"
  :width="`${width}px`"
  :height="`${height}px`"
  :background-color="backgroundColor"
>
  <template v-slot:editor-content></template>
</image-editor>
```

```js
import ImageEditor from "jk-image-editor";

export default {
  components: {
    ImageEditor
  },
  data() {
    return {
      width: "500",
      height: "700",
      backgroundColor: "rgba(255, 255, 255, 0)"
    };
  },
  methods: {
    previewImage() {
      this.$refs["imageEditor"].previewImage();
    },
    downloadImage() {
      this.$refs["imageEditor"].downloadImage();
    }
  }
};
```

## Plugin list  
* html2canvas

## License
[MIT](https://github.com/traceslord/jk-image-editor/blob/master/LICENSE)

Copyright (c) 2020-present zhuhuajian
