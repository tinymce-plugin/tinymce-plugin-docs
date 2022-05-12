## 实例 Demo 语法
---

::::details 点击查看demo组用法

````md
<demoGroup>
 <demoGroupItem title="Vue" active>

:::tinymce-vue3

```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div  v-text="content"></div>
</div>
</template>

<script>
import tinymce from "tinymce";
import "@npkg/tinymce-plugin";
import TinymceVue from "/@/assets/lib/TinymceVue";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
export default{
name: 'domeVue3',
components: { TinymceVue },
data(){
    return {
        content: 'dsdsdssfdddddddddddddddddddsd',
        tinymceOptions:{
                // custom_elements: 'tp-collapse',
                min_height: 200,
                max_height: 700,
                skeletonScreen: true,
                base_url:'/tinymce',
                plugins: 'tp code  tpIndent2em autoresize tpCollapse tpTabs tpButtons tpImportword preview',
                toolbar: ['|code tpIndent2em tpCollapse tpTabs tpButtons tpImportword | Preview'],
             
        }
    }
  }
}
</script>
```

:::
 </demoGroupItem>
 <demoGroupItem title="Vue2">

:::tinymce-vue2

```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div v-html="content"></div>
</div>
</template>

<script>
import tinymce from "/@/assets/lib/tinymce-vue/tinymce";
import "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import TinymceVue from "/@/example/vueDemo/Tinymce-vue2.vue";
export default{
name: 'domeVue2',
components: { TinymceVue },
data(){
    return {
        content: 'fivesdsdsd',
        tinymceOptions:{
                min_height: 200,
                max_height: 700,
                base_url:'/tinymce',
                plugins: 'tp code  tpIndent2em autoresize tpCollapse tpTabs tpButtons image preview',
                toolbar: ['code tpIndent2em tpCollapse tpTabs tpButtons Preview'],
                skeletonScreen: true,
             
        }
    }
  }
}
</script>
```

:::
 </demoGroupItem>
 <demoGroupItem title="React">
  
:::tinymce-react

```html
<script>
import React from 'react';
import ReactDOM from 'react-dom';
import tinymce from "tinymce";
import "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import { Editor } from '@tinymce/tinymce-react';

     class ReactDemo extends React.Component{
       constructor(props) {
         super(props);
           this.reactDemoInit = {
                    min_height: 220,
                    base_url:'/tinymce',
                    branding: false,
                    language:'zh_CN',
                    menubar: false,
                    skeletonScreen: true,
                    plugins: ['advlist autolink lists link image charmap print preview anchor', 'searchreplace visualblocks code fullscreen tpIndent2em autoresize tpCollapse tpTabs tpButtons', 'insertdatetime media table paste code help wordcount tpImportword'],
                    toolbar: 'undo redo tpIndent2em autoresize tpCollapse tpTabs tpButtons tpImportword | formatselect image | ' + 'bold italic backcolor | alignleft aligncenter ' + 'alignright alignjustify | bullist numlist outdent indent | ' + 'removeformat | help',
                    content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:14px }'
             };
           this.reactDemoInitialValue = "<p>这是一个REactDemo</p>"
        }
      render(){
        return (
           <div>
            ...
          </div>
          );
      }
    }

   ReactDOM.render(<ReactDemo />, document.getElementById('ReactRootID'));
</script>
```

:::

 </demoGroupItem>
</demoGroup>
````

::::

::::details 点击查看vue3 Dome用法

````md
:::tinymce-vue3

```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div  v-text="content"></div>
</div>
</template>

<script>
import tinymce from "tinymce";
import "@npkg/tinymce-plugin";
import TinymceVue from "/@/assets/lib/TinymceVue";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
export default{
name: 'domeVue3',
components: { TinymceVue },
data(){
    return {
        content: 'dsdsdssfdddddddddddddddddddsd',
        tinymceOptions:{
                // custom_elements: 'tp-collapse',
                min_height: 200,
                max_height: 700,
                skeletonScreen: true,
                base_url:'/tinymce',
                plugins: 'tp code  tpIndent2em autoresize tpCollapse tpTabs tpButtons tpImportword preview',
                toolbar: ['|code tpIndent2em tpCollapse tpTabs tpButtons tpImportword | Preview'],
             
        }
    }
  }
}
</script>
```

:::
````
::::

::::details 点击查看vue2 Dome用法

````md
:::tinymce-vue2
```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div v-html="content"></div>
</div>
</template>

<script>
import tinymce from "/@/assets/lib/tinymce-vue/tinymce";
import "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import TinymceVue from "/@/example/vueDemo/Tinymce-vue2.vue";
export default{
name: 'domeVue2',
components: { TinymceVue },
data(){
    return {
        content: 'fivesdsdsd',
        tinymceOptions:{
                min_height: 200,
                max_height: 700,
                base_url:'/tinymce',
                plugins: 'tp code  tpIndent2em autoresize tpCollapse tpTabs tpButtons image preview',
                toolbar: ['code tpIndent2em tpCollapse tpTabs tpButtons Preview'],
                skeletonScreen: true,
             
        }
    }
  }
}
</script>
```
:::

````
::::

::::details 点击查看 React Dome用法
````md

:::tinymce-react
```html
<script>
import React from 'react';
import ReactDOM from 'react-dom';
import tinymce from "tinymce";
import "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import { Editor } from '@tinymce/tinymce-react';

     class ReactDemo extends React.Component{
       constructor(props) {
         super(props);
           this.reactDemoInit = {
                    min_height: 220,
                    base_url:'/tinymce',
                    branding: false,
                    language:'zh_CN',
                    menubar: false,
                    skeletonScreen: true,
                    plugins: ['advlist autolink lists link image charmap print preview anchor', 'searchreplace visualblocks code fullscreen tpIndent2em autoresize tpCollapse tpTabs tpButtons', 'insertdatetime media table paste code help wordcount tpImportword'],
                    toolbar: 'undo redo tpIndent2em autoresize tpCollapse tpTabs tpButtons tpImportword | formatselect image | ' + 'bold italic backcolor | alignleft aligncenter ' + 'alignright alignjustify | bullist numlist outdent indent | ' + 'removeformat | help',
                    content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:14px }'
             };
           this.reactDemoInitialValue = "<p>这是一个REactDemo</p>"
        }
      render(){
        return (
           <div>
           ...
          </div>
          );
      }
    }

   ReactDOM.render(<ReactDemo />, document.getElementById('ReactRootID'));
</script>
```

:::

````
::::

<demoGroup>
 <demoGroupItem title="Vue" active>

:::tinymce-vue3

```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div  v-text="content"></div>
</div>
</template>

<script>
import tinymce from "tinymce";
import "@npkg/tinymce-plugin";
import TinymceVue from "/@/assets/lib/TinymceVue";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
export default{
name: 'domeVue3',
components: { TinymceVue },
data(){
    return {
        content: 'dsdsdssfdddddddddddddddddddsd',
        tinymceOptions:{
                // custom_elements: 'tp-collapse',
                min_height: 200,
                max_height: 700,
                skeletonScreen: true,
                base_url:'/tinymce',
                plugins: 'tp code  tpIndent2em autoresize tpCollapse tpTabs tpButtons tpImportword preview',
                toolbar: ['|code tpIndent2em tpCollapse tpTabs tpButtons tpImportword | Preview'],
             
        }
    }
  }
}
</script>
```

:::
 </demoGroupItem>
 <demoGroupItem title="Vue2">

:::tinymce-vue2

```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div v-html="content"></div>
</div>
</template>

<script>
import tinymce from "/@/assets/lib/tinymce-vue/tinymce";
import "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import TinymceVue from "/@/example/vueDemo/Tinymce-vue2.vue";
export default{
name: 'domeVue2',
components: { TinymceVue },
data(){
    return {
        content: 'fivesdsdsd',
        tinymceOptions:{
                min_height: 200,
                max_height: 700,
                base_url:'/tinymce',
                plugins: 'tp code  tpIndent2em autoresize tpCollapse tpTabs tpButtons image preview',
                toolbar: ['code tpIndent2em tpCollapse tpTabs tpButtons Preview'],
                skeletonScreen: true,
             
        }
    }
  }
}
</script>
```

:::
 </demoGroupItem>
 <demoGroupItem title="React">
  
:::tinymce-react

```html
<script>
import React from 'react';
import ReactDOM from 'react-dom';
import tinymce from "tinymce";
import "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import { Editor } from '@tinymce/tinymce-react';

     class ReactDemo extends React.Component{
       constructor(props) {
         super(props);
           this.reactDemoInit = {
                    min_height: 220,
                    base_url:'/tinymce',
                    branding: false,
                    language:'zh_CN',
                    menubar: false,
                    skeletonScreen: true,
                    plugins: ['advlist autolink lists link image charmap print preview anchor', 'searchreplace visualblocks code fullscreen tpIndent2em autoresize tpCollapse tpTabs tpButtons', 'insertdatetime media table paste code help wordcount tpImportword'],
                    toolbar: 'undo redo tpIndent2em autoresize tpCollapse tpTabs tpButtons tpImportword | formatselect image | ' + 'bold italic backcolor | alignleft aligncenter ' + 'alignright alignjustify | bullist numlist outdent indent | ' + 'removeformat | help',
                    content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:14px }'
             };
           this.reactDemoInitialValue = "<p>这是一个REactDemo</p>"
        }
      render(){
        return (
           <div>
            <h1>tinymce demo2</h1>
            <div>
            <Editor initialValue={this.reactDemoInitialValue} init={this.reactDemoInit} />
            </div>
            <div dangerouslySetInnerHTML={{__html: this.reactDemoInitialValue }} ></div>
          </div>
          );
      }
    }

   ReactDOM.render(<ReactDemo />, document.getElementById('ReactRootID'));
</script>
```

:::

 </demoGroupItem>
</demoGroup>


:::tinymce-vue3

```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div  v-text="content"></div>
</div>
</template>

<script>
import tinymce from "tinymce";
import "@npkg/tinymce-plugin";
import TinymceVue from "/@/assets/lib/TinymceVue";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
export default{
name: 'domeVue3',
components: { TinymceVue },
data(){
    return {
        content: 'dsdsdssfdddddddddddddddddddsd',
        tinymceOptions:{
                // custom_elements: 'tp-collapse',
                min_height: 200,
                max_height: 700,
                skeletonScreen: true,
                base_url:'/tinymce',
                plugins: 'tp code  tpIndent2em autoresize tpCollapse tpTabs tpButtons tpImportword preview',
                toolbar: ['|code tpIndent2em tpCollapse tpTabs tpButtons tpImportword | Preview'],
             
        }
    }
  }
}
</script>
```

:::



:::tinymce-vue2
```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div v-html="content"></div>
</div>
</template>

<script>
import tinymce from "/@/assets/lib/tinymce-vue/tinymce";
import "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import TinymceVue from "/@/example/vueDemo/Tinymce-vue2.vue";
export default{
name: 'domeVue2',
components: { TinymceVue },
data(){
    return {
        content: 'fivesdsdsd',
        tinymceOptions:{
                min_height: 200,
                max_height: 700,
                base_url:'/tinymce',
                plugins: 'tp code  tpIndent2em autoresize tpCollapse tpTabs tpButtons image preview',
                toolbar: ['code tpIndent2em tpCollapse tpTabs tpButtons Preview'],
                skeletonScreen: true,
             
        }
    }
  }
}
</script>
```
:::

:::tinymce-react
```html
<script>
//https://babeljs.io/repl/
import React from 'react';
import ReactDOM from 'react-dom';
import tinymce from "tinymce";
import "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import { Editor } from '@tinymce/tinymce-react';

     class ReactDemo extends React.Component{
       constructor(props) {
         super(props);
           this.reactDemoInit = {
                    min_height: 220,
                    base_url:'/tinymce',
                    branding: false,
                    language:'zh_CN',
                    menubar: false,
                    skeletonScreen: true,
                    plugins: ['advlist autolink lists link image charmap print preview anchor', 'searchreplace visualblocks code fullscreen tpIndent2em autoresize tpCollapse tpTabs tpButtons', 'insertdatetime media table paste code help wordcount tpImportword'],
                    toolbar: 'undo redo tpIndent2em autoresize tpCollapse tpTabs tpButtons tpImportword | formatselect image | ' + 'bold italic backcolor | alignleft aligncenter ' + 'alignright alignjustify | bullist numlist outdent indent | ' + 'removeformat | help',
                    content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:14px }'
             };
           this.reactDemoInitialValue = "<p>这是一个REactDemo</p>"
        }
      render(){
        return (
           <div>
            <h1>tinymce demo2</h1>
            <div>
            <Editor initialValue={this.reactDemoInitialValue} init={this.reactDemoInit} />
            </div>
            <div dangerouslySetInnerHTML={{__html: this.reactDemoInitialValue }} ></div>
          </div>
          );
      }
    }

   ReactDOM.render(<ReactDemo />, document.getElementById('ReactRootID'));
</script>
```
:::