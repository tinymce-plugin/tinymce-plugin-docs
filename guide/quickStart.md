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
import tp$ from "/@/assets/lib/tinymce-vue/tinymce-plugin/tinymce-plugin";
import { Editor } from '@tinymce/tinymce-react';

     class reactDemo extends React.Component{
       constructor(props) {
         super(props);
           this.reactDemoInit = {
                    height: 500,
                    base_url:'/tinymce',
                    branding: false,
                    language:'zh_CN',
                    menubar: false,
                    plugins: ['advlist autolink lists link image charmap print preview anchor', 'searchreplace visualblocks code fullscreen indent2em autoresize tpCollapse tpTabs tpButtons', 'insertdatetime media table paste code help wordcount'],
                    toolbar: 'undo redo indent2em autoresize tpCollapse tpTabs tpButtons | formatselect image | ' + 'bold italic backcolor | alignleft aligncenter ' + 'alignright alignjustify | bullist numlist outdent indent | ' + 'removeformat | help',
                    content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:14px }'
             };
           this.reactDemoInitialValue ="<p>这是一个REactDemo</p>"
        }
      render() {
        return /*#__PURE__*/React.createElement("div", null, /*#__PURE__*/React.createElement("h1", null, "tinymce demo"), /*#__PURE__*/React.createElement(Editor, {
                  initialValue: this.reactDemoInitialValue,
                  init: this.reactDemoInit
          }));
        }
    }

   ReactDOM.render(React.createElement(reactDemo,null), document.getElementById('ReactRootID'));
</script>
```
:::