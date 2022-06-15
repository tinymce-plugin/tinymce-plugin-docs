---
title: 如何开启骨架屏
---
# 开启骨架屏（skeletonScreen）

通过配置参数 **`skeletonScreen`** 来开启 [`tinymce`](https://www.tiny.cloud) 富文本框编辑器的骨架屏功能 ，改善 [`tinymce`](https://www.tiny.cloud) 富文本编辑器加载过长用户体验不佳
:::tip 提示
 要使用 **`skeletonScreen`** 必须 引入  [**tinymce-plugin**](https://www.npmjs.com/package/tinymce-plugin) 或 [**@npkg/tinymce-plugin**](https://www.npmjs.com/package/@npkg/tinymce-plugin)
:::

```js {4}
import "tinymce-plugin"; 
tinymce.init({
  ...
  skeletonScreen: true,
  ...
})
```
使用效果
![skeletonScreen](/assets/images/skt-demo.png?100%)
