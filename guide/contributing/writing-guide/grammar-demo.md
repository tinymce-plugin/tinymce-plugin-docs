## 实例 Demo 语法
---
::::details 点击查看demo组用法

````md {3,38,81,125}
<demoGroup>
<demoGroupItem title="Javascript">
// 需要空一行很重要
:::tinymce
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="renderer" content="webkit">
  <script src="https://cdn.staticfile.org/jquery/2.2.4/jquery.min.js"></script>
  <!-- <script src='./api/api.js'></script> -->
  
  <script src='/tinymce/tinymce.js'></script><!-- 必要 -->
  <script src='/tinymce/tinymce-plugin.js'></script><!-- 必要 -->
</head>

<body tp-page-height="498">
      <div class="demo">
        <div id="tinymce-app">
           ...
        </div>
      </div>
  <script>
    ...
  </script>
</body>
</html>

```
:::
 </demoGroupItem>
 <demoGroupItem title="Vue" active>

:::tinymce-vue3

```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div  v-html="content"></div>
</div>
</template>

<script>
import tinymce from "tinymce";
import "tinymce-plugin";
import TinymceVue from "@tinymce-plugin/tinymce-vue";
import "tinymce-plugin/plugins/tpIndent2em/plugin.js";
import "tinymce-plugin/plugins/tpImportword/plugin.js";
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
                base_url:'/v6/tinymce',
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
import tinymce from "tinymce";
import "tinymce-plugin";
import "tinymce-plugin/plugins/tpIndent2em/plugin.js";
import "tinymce-plugin/plugins/tpImportword/plugin.js";
import TinymceVue from "@tinymce-plugin/tinymce-vue";
export default{
name: 'domeVue2',
components: { TinymceVue },
data(){
    return {
        content: 'fivesdsdsd',
        tinymceOptions:{
                min_height: 200,
                max_height: 700,
                base_url:'/v6/tinymce',
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
import "tinymce-plugin";
import "tinymce-plugin/plugins/tpIndent2em/plugin.js";
import "tinymce-plugin/plugins/tpImportword/plugin.js";
import { Editor } from '@tinymce/tinymce-react';

     class ReactDemo extends React.Component{
       constructor(props) {
         super(props);
           this.reactDemoInit = {
                    min_height: 220,
                    base_url:'/v6/tinymce',
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
::::details 点击查看javascript用法
````md
:::tinymce
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="renderer" content="webkit">
  <script src="https://cdn.staticfile.org/jquery/2.2.4/jquery.min.js"></script>
  <!-- <script src='./api/api.js'></script> -->
  
  <script src='/v6/tinymce/tinymce.js'></script><!-- 必要 -->
  <script src='/v6/tinymce/tinymce-plugin'></script><!-- 必要 -->
</head>

<body tp-page-height="498">
      <div class="demo">
        <div id="tinymce-app">
           ...
        </div>
      </div>
  <script>
    ...
  </script>
</body>
</html>

```
:::
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
  <div  v-html="content"></div>
</div>
</template>

<script>
import tinymce from "tinymce";
import "tinymce-plugin";
import TinymceVue from "@tinymce-plugin/tinymce-vue";
import "tinymce-plugin/plugins/tpIndent2em/plugin.js";
import "tinymce-plugin/plugins/tpImportword/plugin.js";
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
                base_url:'/v6/tinymce',
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
import tinymce from "tinymce";
import "tinymce-plugin";
import "tinymce-plugin/plugins/tpIndent2em/plugin.js";
import "tinymce-plugin/plugins/tpImportword/plugin.js";
import TinymceVue from "@tinymce-plugin/tinymce-vue";
export default{
name: 'domeVue2',
components: { TinymceVue },
data(){
    return {
        content: 'fivesdsdsd',
        tinymceOptions:{
                min_height: 200,
                max_height: 700,
                base_url:'/v6/tinymce',
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
import "tinymce-plugin";
import "tinymce-plugin/plugins/tpIndent2em/plugin.js";
import "tinymce-plugin/plugins/tpImportword/plugin.js";
import { Editor } from '@tinymce/tinymce-react';

     class ReactDemo extends React.Component{
       constructor(props) {
         super(props);
           this.reactDemoInit = {
                    min_height: 220,
                    base_url:'/v6/tinymce',
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

:::::details 点击查看 tinymce-box用法
````md
::::tinymce-box
:::html
```html
<textarea id='basic-example'>
  <p><img style="display: block; margin-left: auto; margin-right: auto;" title="Tiny Logo" src="https://www.tiny.cloud/docs/images/logos/android-chrome-256x256.png" alt="TinyMCE Logo" width="128" height="128" /></p>
  <h2 style="text-align: center;">Welcome to the TinyMCE editor demo!</h2>

  <h2>Got questions or need help?</h2>

  <ul>
    <li>Our <a href="https://www.tiny.cloud/docs/">documentation</a> is a great resource for learning how to configure TinyMCE.</li>
    <li>Have a specific question? Try the <a href="https://stackoverflow.com/questions/tagged/tinymce" target="_blank" rel="noopener"><code>tinymce</code> tag at Stack Overflow</a>.</li>
    <li>We also offer enterprise grade support as part of <a href="https://www.tiny.cloud/pricing">TinyMCE premium plans</a>.</li>
  </ul>

  <h2>A simple table to play with</h2>

  <table style="border-collapse: collapse; width: 100%;" border="1">
    <thead>
      <tr>
        <th>Product</th>
        <th>Cost</th>
        <th>Really?</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>TinyMCE</td>
        <td>Free</td>
        <td>YES!</td>
      </tr>
      <tr>
        <td>Plupload</td>
        <td>Free</td>
        <td>YES!</td>
      </tr>
    </tbody>
  </table>

  <h2>Found a bug?</h2>

  <p>
    If you think you have found a bug please create an issue on the <a href="https://github.com/tinymce/tinymce/issues">GitHub repo</a> to report it to the developers.
  </p>

  <h2>Finally ...</h2>

  <p>
    Don't forget to check out our other product <a href="http://www.plupload.com" target="_blank">Plupload</a>, your ultimate upload solution featuring HTML5 upload support.
  </p>
  <p>
    Thanks for supporting TinyMCE! We hope it helps you and your users create great content.<br>All the best from the TinyMCE team.
  </p>
</textarea>

```
:::
:::js
```js
tinymce.init({
  selector: 'textarea#basic-example',
  height: 500,
  menubar: false,
  skeletonScreen: true,
  plugins: [
    'advlist autolink lists link image charmap print preview anchor',
    'searchreplace visualblocks code fullscreen',
    'insertdatetime media table paste code help wordcount'
  ],
  toolbar: 'undo redo | formatselect | ' +
  'bold italic backcolor | alignleft aligncenter ' +
  'alignright alignjustify | bullist numlist outdent indent | ' +
  'removeformat | help',
  content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:14px }'
});
```
:::css
```css
#basic-example{
    color: #333;
}
```
:::
::::
````
:::::

:::tinymce-vue3
```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div  v-html="content"></div>
</div>
</template>

<script>

import tinymce from "tinymce";
import "tinymce-plugin";
import TinymceVue from "@tinymce-plugin/tinymce-vue";
import "tinymce-plugin/plugins/tpIndent2em/plugin.js";
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
                base_url:'/v6/tinymce',
                external_plugins:{
                  tpImportword: '/v6/tinymce/tpImportword/plugin.js',
                },
                plugins: ' code   autoresize tpCollapse tpTabs tpButtons  preview',
                toolbar: ['|code tpIndent2em tpImportword | Preview'],
             
        }
    }
  }
}
</script>
```

:::

<demoGroup>
 <demoGroupItem title=" Javascript ">

:::tinymce
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="renderer" content="webkit">
  <script src="https://cdn.staticfile.org/jquery/2.2.4/jquery.min.js"></script>
  <!-- <script src='./api/api.js'></script> -->
  
  <script src='/v6/tinymce/tinymce.js'></script><!-- 必要 -->
  <script src='/v6/tinymce/tinymce-plugin.js'></script> <!--必要 -->

  <style>
    body{max-width: 1920px;width: 100%; margin: 0 auto;}
    header{}
    .header_logo{ display: inline-block;vertical-align: middle;}
    header > div{ display: block; text-align: center;}
   .demo,#showID{ margin-top:50px;}
   #showID{ padding: 20px;}
   #tinymce-app .tinymce-box {padding-bottom: 0px!important;}
   .tiny_color{ color:#344A85 ;text-shadow: 0 3px 5px #677285; display: inline-block;margin-right: -20px; vertical-align: middle;}
   .plugin_color { color: #43B984;text-shadow: 0 3px 5px #34435C;display: inline-block;margin-left: -23px; vertical-align: middle;}
   .text-center{ text-align: center;}
   .animated #logoSvgId{
    fill-opacity: 0.75
   }
   a{display: inline-block; padding: 20px;font-size: 20px; list-style: none; text-decoration: none;color: #333;}
   #logoSvgId{display: inline-block; vertical-align: middle;}
   .btn{ border-radius: 20px; outline: none; width: 300px;height: 60px; margin: 20px auto; display: block; background: #1488F5; text-align: center;line-height: 60px; font-size: 28px;letter-spacing: 2px; color: #dedede;}
  </style>
</head>

<body tp-page-height="498">
      <div class="demo">
         <button onclick="savefun()">sdsd</button>
        <div id="tinymce-app">
            <div class="tinymce-demo" style="color: #000;">
                <div class="tinymce-cnt" id="mytextarea">
                  <div id="fvContentID"><ol>
                    <li style="letter-spacing: 2px;"><span style="color: #2dc26b;"><span style="color: #000000;">不知如何使用编辑框可以点击<img src="https://xwjywjb.obs.cn-southwest-2.myhuaweicloud.com/db/UploadFile/2020/11/13/fcd5cc64-aff6-4ded-8f14-6a98b66a2aea.png">（或 Alt+0)，查看帮助-【快捷键】【功能介绍】【操作手册】【疑问解答】【反馈问题】 。</span></span></li>
                    <li style="letter-spacing: 2px;"><span style="color: #3598db;">鼠标悬浮</span>在<em>功能图标</em>上可了解功能名称</li>
                    <li style="letter-spacing: 2px;"><span style="color: #e03e2d;">如过需要修改2020年11月之前的旧新闻，建议先清除格式&nbsp; 或&nbsp; 一键布局<img src="https://xwjywjb.obs.cn-southwest-2.myhuaweicloud.com/db/UploadFile/2020/11/13/e952a0d5-2d30-4d86-ae7d-e8fd5c4e7cc7.png">，将旧新闻样式去掉重新排版</span></li>
                    <li style="letter-spacing: 2px;"><span style="color: #e03e2d;">若文档编辑调整过程中发生意外关闭【如：登录时间过长】，并且未存为草稿 可以点击<img src="https://xwjywjb.obs.cn-southwest-2.myhuaweicloud.com/db/UploadFile/2020/12/25/9b1473d3-e399-43d9-86b1-a0cb5970d7d0.png">，恢复文档编辑状态（1小时以内的最近状态）</span></li>
                    <li style="letter-spacing: 2px;"><span style="color: #e03e2d;"><span id="attachment_mce_1" contenteditable="false"><img style="width: 30px;" src="https://api.hope55.com/Content/js/tinymce/plugins/attachment/icons/file_type_pdf2.svg" width="30px"><a href="https://xwjywjb.obs.cn-southwest-2.myhuaweicloud.com/db/UploadFile/2020/11/9/a7653b78-f186-4237-81fb-213aac317ebe.pdf" target="_blank" rel="noopener">新编辑器新闻上传操作说明(1).pdf (1.04 M)</a></span> </span></li>
                  </ol></div>
                  <style> #fvContentID a{display:inline-block!important} #fvContentID .attachment>img{display:inline-block!important;max-width:30px!important;min-width:30px!important;}#fvContentID .attachment>a{display:contents!important;}</style>
                </div>
            </div>
        </div>
      </div>
  <script>
    function savefun(){
      // $("#showID").html(tinymceConfig.getHtml())
        $("#showID").html(tinymce.activeEditor.getContent())
      console.log(tinymce.activeEditor.getContent());
    }

                var xhrOnProgress = function (fun) {
                xhrOnProgress.onprogress = fun;
                return function () {
                    var xhr = $.ajaxSettings.xhr();
                    if (typeof xhrOnProgress.onprogress !== 'function')
                        return xhr;
                    if (xhrOnProgress.onprogress && xhr.upload) {
                        xhr.upload.onprogress = xhrOnProgress.onprogress;
                    }
                    return xhr;
                }
            }
            var tinymceConfig= {
                tinyID: "mytextarea",//作用域ID
                placeholder: '', //默认文字
                infoHtml: $(this.tinyID).html(),//初始化内容
                GbaseUrl: '',//全局baseUrl
                OMHtml: '<div style="height: 1500px;"><p><h2>操作手册：</h2></p></div><p>666</p>', //设置操作手册Html
                CPHtml: '',
            }
          tinymce.init({
                 selector: '#'+tinymceConfig.tinyID,
                 language:'zh_CN',
                 menubar:false,
                 branding: false,
                 min_height:400,
                 max_height: 700,
                //  baseURL: './'
                 plugins: '      preview insertdatetime  attachment  searchreplace visualblocks autolink   fullscreen  image  link media code codesample table charmap  pagebreak  anchor advlist lists  help emoticons      tpIndent2em  tpImportword    autoresize   tpCollapse tpTabs tpButtons',
                 toolbar_groups: {
                         formatting: {
                             text: '文字格式',
                             tooltip: 'Formatting',
                             items: 'bold italic underline | superscript subscript',
                         },
                         alignment: {
                             icon: 'align-left',
                             tooltip: 'alignment',
                             items: 'alignleft aligncenter alignright alignjustify',
                         }
                  },
                 toolbar: ['|code formatselect fontselect fontsizeselect forecolor backcolor bold italic underline strikethrough  link alignment bullist numlist blockquote subscript superscript  removeformat table image  media    emoticons     pagebreak    tpImportword codesample visualblocks insertdatetime    quickbars   cut copy undo redo ltr rtl tpCollapse tpTabs tpButtons restoredraft  searchreplace fullscreen tpIndent2em  help wordcount preview'],
                 table_style_by_css: true,
                 OperationManualHtml: '',
                 CommonProblemHtml: '',
                 fixed_toolbar_container:'#tinymce-app .toolbar',
                 custom_ui_selector: '#tinymce-app',
                 placeholder:''+tinymceConfig.placeholder,
                 file_picker_types: 'media',
                 powerpaste_word_import: "clean", // 是否保留word粘贴样式  clean | merge 
                 powerpaste_html_import: 'clean', // propmt, merge, clean
                 powerpaste_allow_local_images: true,//
                 powerpaste_keep_unsupported_src:true,
                 paste_data_images: true,
                 toolbar_sticky: false,
                skeletonScreen: true,
                 autosave_ask_before_unload: false,
                 fontsize_formats: '12px 14px 16px 18px 24px 36px 48px 56px 72px',
                 font_formats: '微软雅黑=Microsoft YaHei,Helvetica Neue,PingFang SC,sans-serif;苹果苹方=PingFang SC,Microsoft YaHei,sans-serif;宋体=simsun,serif;仿宋体=FangSong,serif;黑体=SimHei,sans-serif;Arial=arial,helvetica,sans-serif;Symbol=symbol;Tahoma=tahoma,arial,helvetica,sans-serif;Terminal=terminal,monaco;Times New Roman=times new roman,times;Verdana=verdana,geneva;Webdings=webdings;Wingdings=wingdings,zapf dingbats;',
                 images_upload_base_path: '',
               
                 images_upload_handler: (blobInfo, progress) => new Promise((resolve, reject)=>{
                     var file = blobInfo.blob();
                    var reader = new FileReader();
                        reader.onload = function(e){
                        resolve(e.target.result)
                        }
                   reader.readAsDataURL(file)
                 }),
                 file_picker_callback: function (succFun, value, meta) { //自定义文件上传函数 
                    var filetype = '.pdf, .txt, .zip, .rar, .7z, .doc, .docx, .xls, .xlsx, .ppt, .pptx, .mp3, .mp4';
                    var input = document.createElement('input');
                    input.setAttribute('type', 'file');
                    input.setAttribute('accept', filetype);
                    input.click();
                    input.onchange = function () {
                        var file = this.files[0];
                        var data = new FormData();
                         data.append("file", file);
                        $.ajax({
                            data: data,
                            type: 'GET',
                            url: './api/file.json',
                            header:{'Content-Type':'multipart/form-data'},
                            cache: false,
                            contentType: false,
                            processData: false,
                            dataType: 'json',
                            xhr: xhrOnProgress(function (e) {
                                const percent = (e.loaded / e.total * 100 | 0) + '%';//计算百分比
                                // console.log(percent);
                                progressCallback(percent);
                  
                            }),
                        }).then(function (data) {
                            if ( data.code== 200) {
                                succFun(data.data,{ text: data.data });
                            }
                        }).fail(function (error) {
                            failFun('上传失败:' + error.message)
                        });
                    }
                 },
                 file_callback: function (file, succFun) { //文件上传  file:文件对象 succFun(url|string,obj) 成功回调
                    var data = new FormData();
                    data.append("file", file);
                    $.ajax({
                        data: data,
                        type: 'GET',
                        url: '/v6/tinymce/api/file.json',
                        cache: false,
                        contentType: false,
                        processData: false,
                        header:{'Content-Type':'multipart/form-data'},
                        dataType: 'json',
                        xhr: xhrOnProgress(function (e) {
                            const percent = (e.loaded / e.total * 100 | 0) + '%';//计算百分比
                            progressCallback(percent);
                        }),
                    }).then(function (data) {
                        if ( data.code== 200) {
                            succFun(data.data,{text: file.name});
                        } 
                    }).fail(function (error) {
                        // failFun('上传失败:' + error.message)
                    });
                 },
                 tp_attachment_max_size: 5009715200,
                //  attachment_style: '.attachment>img{display:inline-block!important;max-width:30px!important;}',
                 tp_attachment_assets_path: '/v6/tinymce/plugins/attachment/icons',
                
              
                 init_instance_callback: function(editor){
                     $('#tinymce-app').fadeIn(1000);
                  //    editor.execCommand('selectAll');
                  //    editor.selection.getRng().collapse(false);
                  //    editor.focus();
                 }
          }).then(function(res){
          
                 tinymce.feedBackIframeUrl ='/v6/tinymce/plugins/help/docBox.html'; //反馈链接
             });
  </script>
</body>
</html>

```
:::
 </demoGroupItem>
 <demoGroupItem title="Vue" active>

:::tinymce-vue3

```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :init="tinymceOptions" ></tinymce-vue>
  </div>
  <div  v-html="content"></div>
</div>
</template>

<script>
import tinymce from "tinymce";
import "tinymce-plugin";
import TinymceVue from "@tinymce-plugin/tinymce-vue";
import "tinymce-plugin/plugins/tpIndent2em/plugin.js";
import "tinymce-plugin/plugins/tpImportword/plugin.js";
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
                base_url:'/v6/tinymce',
                plugins: ' code  tpIndent2em autoresize tpCollapse tpTabs tpButtons tpImportword preview',
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
import "tinymce-plugin";
import "tinymce-plugin/plugins/tpIndent2em/plugin.js";
import "tinymce-plugin/plugins/tpImportword/plugin.js";
import TinymceVue from "@tinymce-plugin/tinymce-vue";
export default{
name: 'domeVue2',
components: { TinymceVue },
data(){
    return {
        content: 'fivesdsdsd',
        tinymceOptions:{
                min_height: 200,
                max_height: 700,
                base_url:'/v6/tinymce',
                plugins: ' code  tpIndent2em autoresize tpCollapse tpTabs tpButtons image preview',
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
import "tinymce-plugin";
import "tinymce-plugin/plugins/tpIndent2em/plugin.js";
import "tinymce-plugin/plugins/tpImportword/plugin.js";
import { Editor } from '@tinymce/tinymce-react';

     class ReactDemo extends React.Component{
       constructor(props) {
           super(props);
           this.state = { reactDemoInitialValue: "<p>这是一个REactDemo</p>"};
           this.reactDemoInit = {
                    min_height: 220,
                    base_url:'/v6/tinymce',
                    branding: false,
                    language:'zh_CN',
                    menubar: false,
                    skeletonScreen: true,
                    plugins: 'advlist autolink lists link image charmap  preview anchor searchreplace visualblocks code fullscreen tpIndent2em autoresize tpCollapse tpTabs tpButtons insertdatetime media table code help wordcount tpImportword',
                    toolbar: 'undo redo tpIndent2em autoresize tpCollapse tpTabs tpButtons tpImportword | formatselect image | ' + 'bold italic backcolor | alignleft aligncenter ' + 'alignright alignjustify | bullist numlist outdent indent | ' + 'removeformat | help',
                    content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:14px }'
             };
       this.handleChange = (data)=>{
              this.setState({reactDemoInitialValue: data})
        }
      }
      render(){
        return (
           <div>
            <h1>tinymce demo2</h1>
            <div>
            <Editor initialValue={this.state.reactDemoInitialValue} init={this.reactDemoInit} onEditorChange={this.handleChange} />
            </div>
            <div dangerouslySetInnerHTML={{__html: this.state.reactDemoInitialValue }} ></div>
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


:::tinymce
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="renderer" content="webkit">
  <script src="https://cdn.staticfile.org/jquery/2.2.4/jquery.min.js"></script>
  <!-- <script src='./api/api.js'></script> -->
  
  <script src='/v6/tinymce/tinymce.js'></script><!-- 必要 -->
  <script src='/v6/tinymce/tinymce-plugin.js'></script> <!--必要 -->

  <style>
    body{max-width: 1920px;width: 100%; margin: 0 auto;}
    header{}
    .header_logo{ display: inline-block;vertical-align: middle;}
    header > div{ display: block; text-align: center;}
   .demo,#showID{ margin-top:50px;}
   #showID{ padding: 20px;}
   #tinymce-app .tinymce-box {padding-bottom: 0px!important;}
   .tiny_color{ color:#344A85 ;text-shadow: 0 3px 5px #677285; display: inline-block;margin-right: -20px; vertical-align: middle;}
   .plugin_color { color: #43B984;text-shadow: 0 3px 5px #34435C;display: inline-block;margin-left: -23px; vertical-align: middle;}
   .text-center{ text-align: center;}
   .animated #logoSvgId{
    fill-opacity: 0.75
   }
   a{display: inline-block; padding: 20px;font-size: 20px; list-style: none; text-decoration: none;color: #333;}
   #logoSvgId{display: inline-block; vertical-align: middle;}
   .btn{ border-radius: 20px; outline: none; width: 300px;height: 60px; margin: 20px auto; display: block; background: #1488F5; text-align: center;line-height: 60px; font-size: 28px;letter-spacing: 2px; color: #dedede;}
  </style>
</head>

<body tp-page-height="498">
      <div class="demo">
        <button onclick="savefun()">sdsd</button>
        <div id="tinymce-app">
            <div class="tinymce-demo" style="color: #000;">
                <div class="tinymce-cnt" id="mytextarea">
                  <div id="fvContentID"><ol>
                    <li style="letter-spacing: 2px;"><span style="color: #2dc26b;"><span style="color: #000000;">不知如何使用编辑框可以点击<img src="https://xwjywjb.obs.cn-southwest-2.myhuaweicloud.com/db/UploadFile/2020/11/13/fcd5cc64-aff6-4ded-8f14-6a98b66a2aea.png">（或 Alt+0)，查看帮助-【快捷键】【功能介绍】【操作手册】【疑问解答】【反馈问题】 。</span></span></li>
                    <li style="letter-spacing: 2px;"><span style="color: #3598db;">鼠标悬浮</span>在<em>功能图标</em>上可了解功能名称</li>
                    <li style="letter-spacing: 2px;"><span style="color: #e03e2d;">如过需要修改2020年11月之前的旧新闻，建议先清除格式&nbsp; 或&nbsp; 一键布局<img src="https://xwjywjb.obs.cn-southwest-2.myhuaweicloud.com/db/UploadFile/2020/11/13/e952a0d5-2d30-4d86-ae7d-e8fd5c4e7cc7.png">，将旧新闻样式去掉重新排版</span></li>
                    <li style="letter-spacing: 2px;"><span style="color: #e03e2d;">若文档编辑调整过程中发生意外关闭【如：登录时间过长】，并且未存为草稿 可以点击<img src="https://xwjywjb.obs.cn-southwest-2.myhuaweicloud.com/db/UploadFile/2020/12/25/9b1473d3-e399-43d9-86b1-a0cb5970d7d0.png">，恢复文档编辑状态（1小时以内的最近状态）</span></li>
                    <li style="letter-spacing: 2px;"><span style="color: #e03e2d;"><span id="attachment_mce_1" contenteditable="false"><img style="width: 30px;" src="https://api.hope55.com/Content/js/tinymce/plugins/attachment/icons/file_type_pdf2.svg" width="30px"><a href="https://xwjywjb.obs.cn-southwest-2.myhuaweicloud.com/db/UploadFile/2020/11/9/a7653b78-f186-4237-81fb-213aac317ebe.pdf" target="_blank" rel="noopener">新编辑器新闻上传操作说明(1).pdf (1.04 M)</a></span> </span></li>
                  </ol></div>
                  <style> #fvContentID a{display:inline-block!important} #fvContentID .attachment>img{display:inline-block!important;max-width:30px!important;min-width:30px!important;}#fvContentID .attachment>a{display:contents!important;}</style>
                </div>
            </div>
            <div id="showID" > </div>
        </div>
      </div>
  <script>
    function savefun(){
      $("#showID").html(tinymce.activeEditor.getContent())
      console.log(tinymce.activeEditor.getContent());
    }

                var xhrOnProgress = function (fun) {
                xhrOnProgress.onprogress = fun;
                return function () {
                    var xhr = $.ajaxSettings.xhr();
                    if (typeof xhrOnProgress.onprogress !== 'function')
                        return xhr;
                    if (xhrOnProgress.onprogress && xhr.upload) {
                        xhr.upload.onprogress = xhrOnProgress.onprogress;
                    }
                    return xhr;
                }
            }
            var tinymceConfig= {
                tinyID: "mytextarea",//作用域ID
                placeholder: '', //默认文字
                infoHtml: $(this.tinyID).html(),//初始化内容
                GbaseUrl: '',//全局baseUrl
                OMHtml: '<div style="height: 1500px;"><p><h2>操作手册：</h2></p></div><p>666</p>', //设置操作手册Html
                CPHtml: '',
            }
          tinymce.init({
                 selector: '#'+tinymceConfig.tinyID,
                 language:'zh_CN',
                 menubar:false,
                 branding: false,
                 min_height:400,
                 max_height: 700,
                //  baseURL: './'
                 plugins: '      preview insertdatetime  attachment  searchreplace visualblocks autolink   fullscreen  image  link media code codesample table charmap  pagebreak  anchor advlist lists  help emoticons      tpIndent2em  tpImportword    autoresize   tpCollapse tpTabs tpButtons',
                 toolbar_groups: {
                         formatting: {
                             text: '文字格式',
                             tooltip: 'Formatting',
                             items: 'bold italic underline | superscript subscript',
                         },
                         alignment: {
                             icon: 'align-left',
                             tooltip: 'alignment',
                             items: 'alignleft aligncenter alignright alignjustify',
                         }
                  },
                 toolbar: ['|code formatselect fontselect fontsizeselect forecolor backcolor bold italic underline strikethrough  link alignment bullist numlist blockquote subscript superscript  removeformat table image  media    emoticons     pagebreak    tpImportword codesample visualblocks insertdatetime    quickbars   cut copy undo redo ltr rtl tpCollapse tpTabs tpButtons restoredraft  searchreplace fullscreen tpIndent2em  help wordcount preview'],
                 table_style_by_css: true,
                 OperationManualHtml: '',
                 CommonProblemHtml: '',
                 fixed_toolbar_container:'#tinymce-app .toolbar',
                 custom_ui_selector: '#tinymce-app',
                 placeholder:''+tinymceConfig.placeholder,
                 file_picker_types: 'media',
                 powerpaste_word_import: "clean", // 是否保留word粘贴样式  clean | merge 
                 powerpaste_html_import: 'clean', // propmt, merge, clean
                 powerpaste_allow_local_images: true,//
                 powerpaste_keep_unsupported_src:true,
                 paste_data_images: true,
                 toolbar_sticky: false,
                skeletonScreen: true,
                 autosave_ask_before_unload: false,
                 fontsize_formats: '12px 14px 16px 18px 24px 36px 48px 56px 72px',
                 font_formats: '微软雅黑=Microsoft YaHei,Helvetica Neue,PingFang SC,sans-serif;苹果苹方=PingFang SC,Microsoft YaHei,sans-serif;宋体=simsun,serif;仿宋体=FangSong,serif;黑体=SimHei,sans-serif;Arial=arial,helvetica,sans-serif;Symbol=symbol;Tahoma=tahoma,arial,helvetica,sans-serif;Terminal=terminal,monaco;Times New Roman=times new roman,times;Verdana=verdana,geneva;Webdings=webdings;Wingdings=wingdings,zapf dingbats;',
                 images_upload_base_path: '',
               
                 images_upload_handler: (blobInfo, progress) => new Promise((resolve, reject)=>{
                     var file = blobInfo.blob();
                    var reader = new FileReader();
                        reader.onload = function(e){
                        resolve(e.target.result)
                        }
                   reader.readAsDataURL(file)
                 }),
                 file_picker_callback: function (succFun, value, meta) { //自定义文件上传函数 
                    var filetype = '.pdf, .txt, .zip, .rar, .7z, .doc, .docx, .xls, .xlsx, .ppt, .pptx, .mp3, .mp4';
                    var input = document.createElement('input');
                    input.setAttribute('type', 'file');
                    input.setAttribute('accept', filetype);
                    input.click();
                    input.onchange = function () {
                        var file = this.files[0];
                        var data = new FormData();
                         data.append("file", file);
                        $.ajax({
                            data: data,
                            type: 'GET',
                            url: './api/file.json',
                            header:{'Content-Type':'multipart/form-data'},
                            cache: false,
                            contentType: false,
                            processData: false,
                            dataType: 'json',
                            xhr: xhrOnProgress(function (e) {
                                const percent = (e.loaded / e.total * 100 | 0) + '%';//计算百分比
                                // console.log(percent);
                                progressCallback(percent);
                  
                            }),
                        }).then(function (data) {
                            if ( data.code== 200) {
                                succFun(data.data,{ text: data.data });
                            }
                        }).fail(function (error) {
                            failFun('上传失败:' + error.message)
                        });
                    }
                 },
                 file_callback: function (file, succFun) { //文件上传  file:文件对象 succFun(url|string,obj) 成功回调
                    var data = new FormData();
                    data.append("file", file);
                    $.ajax({
                        data: data,
                        type: 'GET',
                        url: '/v6/tinymce/api/file.json',
                        cache: false,
                        contentType: false,
                        processData: false,
                        header:{'Content-Type':'multipart/form-data'},
                        dataType: 'json',
                        xhr: xhrOnProgress(function (e) {
                            const percent = (e.loaded / e.total * 100 | 0) + '%';//计算百分比
                            progressCallback(percent);
                        }),
                    }).then(function (data) {
                        if ( data.code== 200) {
                            succFun(data.data,{text: file.name});
                        } 
                    }).fail(function (error) {
                        // failFun('上传失败:' + error.message)
                    });
                 },
                 tp_attachment_max_size: 5009715200,
                //  attachment_style: '.attachment>img{display:inline-block!important;max-width:30px!important;}',
                 tp_attachment_assets_path: '/v6/tinymce/plugins/attachment/icons',
                
              
                 init_instance_callback: function(editor){
                     $('#tinymce-app').fadeIn(1000);
                  //    editor.execCommand('selectAll');
                  //    editor.selection.getRng().collapse(false);
                  //    editor.focus();
                 }
          }).then(function(res){
          
                 tinymce.feedBackIframeUrl ='/v6/tinymce/plugins/help/docBox.html'; //反馈链接
             });
  </script>
</body>
</html>

```
:::



::::tinymce-box
:::html
```html
<textarea id='basic-example'>
  <h1><strong>👋 Welcome !</strong></h1>
  <p><img style="display: block; margin-left: auto; margin-right: auto;" title="Tiny Logo" src="/thinymce-pluginIcon.png" alt="TinyMCE Logo" width="128"  /></p>
  <p>欢迎来到 <a href="https://github.com/tinymce-plugin" target="_blank"><strong><code class="fv-code_inline">Tinymce-plugin</code></strong></a></p><p>这是一个专注 提供 <strong>强大、好用、丰富</strong> 的 <a href="https://www.tiny.cloud" target="_blank"><code class="fv-code_inline">tinymce</code></a> 富文本编辑器 <strong>插件</strong>、<strong>扩展</strong> 和 <strong>技术</strong> 的技术社区，方便 <strong>交流讨论</strong>，<strong>分享经验</strong> 。</p><p>本社区有多个不错的插件或者项目，欢迎 Star ⭐ 关注~</p>
  <h1> ✨Tinymce-plugin</h1>
  <p><a href="https://github.com/tinymce-plugin" target="_blank"><img src="https://tinymce-plugin.github.io/badge.svg" alt="tinymce-plugin"></a>&nbsp; <a href="https://www.npmjs.com/package/tinymce-plugin" target="_blank"><img src="https://img.shields.io/npm/v/tinymce-plugin.svg" alt="release candidate"></a>&nbsp; <a href="https://www.tiny.cloud" target="_blank"><img src="https://img.shields.io/badge/tinymce-6.x-green.svg" alt="tinymce Version"></a>&nbsp; <a href="https://github.com/tinymce-plugin/tinymce-plugin/blob/main/LICENSE" target="_blank"><img src="https://img.shields.io/github/license/tinymce-plugin/tp-indent2em.svg" alt="GitHub license"></a>&nbsp; <a href="https://www.tiny.cloud" target="_blank"><img src="https://img.shields.io/npm/dm/tinymce-plugin" alt="tinymce Version"></a></p>
</textarea>

```
:::
:::js
```js
tinymce.init({
  selector: 'textarea#basic-example',
  height: 500,
  menubar: false,
  skeletonScreen: true,
  plugins: 'link image searchreplace visualblocks code fullscreen insertdatetime media table code help wordcount',
   images_upload_handler: function (blobInfo, succFun, failFun) {
                    var file = blobInfo.blob();
                    var reader = new FileReader();
                    reader.onload = function(e){
                     succFun(e.target.result)
                    }
                   reader.readAsDataURL(file)
  },
  toolbar: 'undo redo | formatselect | ' +
  'bold italic backcolor | alignleft aligncenter ' +
  'alignright alignjustify | bullist numlist outdent indent | ' +
  'removeformat | help',
  content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:14px }'
});
```
:::css
```css
#basic-example{
    color: #333;
}
```
:::
::::
