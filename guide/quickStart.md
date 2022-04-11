---
title: 快速上手
---
## 快速上手
:::tinymce-react sdsd  
```html
<div>
 <h1>插件demo展示区域</h1>
  <div id="ReactRootID" >
   
  </div>
</div>
<script>
//https://babeljs.io/repl/
import React from 'react';
import ReactDOM from 'react-dom';
import tinymce from "/@/assets/lib/tinymce-vue/tinymce";
import tinymcePlugin from "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import { Editor } from '@tinymce/tinymce-react';

     class reactDemo extends React.Component{
       constructor(props) {
         super(props);
           this.reactDemoInit = {
                    min_height: 200,
                    base_url:'/tinymce',
                    branding: false,
                    language:'zh_CN',
                    menubar: false,
                    plugins: ['advlist autolink lists link image charmap print tpImportword preview anchor', 'searchreplace visualblocks code fullscreen indent2em autoresize tpCollapse tpTabs tpButtons', 'insertdatetime media table paste code help wordcount'],
                    toolbar: 'undo redo indent2em autoresize tpCollapse tpTabs tpButtons | formatselect image tpImportword | ' + 'bold italic backcolor | alignleft aligncenter ' + 'alignright alignjustify | bullist numlist outdent indent | ' + 'removeformat | help',
                    content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:14px }',
                    skeletonScreen: true
             };
           this.reactDemoInitialValue ="<p>这是一个REactDemo</p>"
        }
      render() {
        return /*#__PURE__*/React.createElement("div", null, /*#__PURE__*/React.createElement("div", null, ""), /*#__PURE__*/React.createElement(Editor, {
                  initialValue: this.reactDemoInitialValue,
                  init: this.reactDemoInit
          }));
        }
    }

   ReactDOM.render(React.createElement(reactDemo,null), document.getElementById('ReactRootID'));
</script>
```
:::

:::tinymce-vue2 sdsVuwDFSDF 
```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :options="tinymceOptions" ></tinymce-vue>
  </div>
  <div v-html="content"></div>
</div>
</template>

<script>
import tinymce from "/@/assets/lib/tinymce-vue/tinymce";
import tinymcePlugin from "@npkg/tinymce-plugin";
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