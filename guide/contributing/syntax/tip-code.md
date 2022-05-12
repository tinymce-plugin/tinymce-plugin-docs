---
title: 提示与代码高亮
---
## 提示、标注、警告和危险操作

```md
:::tip Tip
这是一个提示
:::
```
:::tip Tip
这是一个提示
:::

```md
:::info Info
Info
:::
```
:::info Info
Info
:::

```md
:::warning Warning
这是一个警告
:::
```
:::warning Warning
这是一个警告
:::

```md
:::danger Danger
这是一个危险操作
:::
```
:::danger Danger
这是一个危险操作
:::
```md
:::details Details
 这是一个详情
:::
```
:::details Details
这是一个详情
:::

## 代码高亮


````md
```js {4}
import "tinymce-plugin"; 
tinymce.init({
  ...
  skeletonScreen: true,
  ...
})
```
````

```js {4}
import "tinymce-plugin"; 
tinymce.init({
  ...
  skeletonScreen: true,
  ...
})
```


````md
```js {1,3-4}
import "tinymce-plugin"; 
tinymce.init({
  ...
  skeletonScreen: true,
  ...
})
```
````

```js {1,3-4}
import "tinymce-plugin"; 
tinymce.init({
  ...
  skeletonScreen: true,
  ...
})
```

