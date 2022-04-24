# 前言

:::tinymce-vue3 哈市大家啊实打实大苏打好看就好看啊速度很快按时打卡实打实哈开始大师的话看阿松大啊大苏打
```vue
<template>
<div>
 <h1>插件demo展示区域</h1>
  <div class="vueDemo">
    <tinymce-vue v-model="content" :options="tinymceOptions" ></tinymce-vue>
  </div>
  <div  v-html="content"></div>
</div>
</template>

<script>
import tinymce from "/@/assets/lib/tinymce-vue/tinymce";
import tinymcePlugin from "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import TinymceVue from "/@/example/vueDemo/Tinymce-vue.vue";
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

:::tinymce-react sdsdwewe  
```html
<script>
//https://babeljs.io/repl/
import React from 'react';

import ReactDOM from 'react-dom';

  class TodoApp extends React.Component {
  constructor(props) {
    super(props);
    this.state = { items: [], text: '' };
    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  render() {
    return (
      <div>
        <h3>TODO</h3>
        <TodoList items={this.state.items} />
        <form onSubmit={this.handleSubmit}>
          <label htmlFor="new-todo">
            What needs to be done?
          </label>
          <input
            id="new-todo"
            onChange={this.handleChange}
            value={this.state.text}
          />
          <button>
            Add #{this.state.items.length + 1}
          </button>
        </form>
      </div>
    );
  }

  handleChange(e) {
    this.setState({ text: e.target.value });
  }

  handleSubmit(e) {
    e.preventDefault();
    if (this.state.text.length === 0) {
      return;
    }
    const newItem = {
      text: this.state.text,
      id: Date.now()
    };
    this.setState(state => ({
      items: state.items.concat(newItem),
      text: ''
    }));
  }
}

class TodoList extends React.Component {
  render() {
    return (
      <ul>
        {this.props.items.map(item => (
          <li key={item.id}>{item.text}</li>
        ))}
      </ul>
    );
  }
}

ReactDOM.render(
  <TodoApp />,
  document.getElementById('todosexample')
);

</script>
```
:::



:::tinymce-react sdsdwewe  
```html
<script>
//https://babeljs.io/repl/
import React from 'react';
import ReactDOM from 'react-dom';
import tinymce from "/@/assets/lib/tinymce-vue/tinymce";
import tinymcePlugin from "@npkg/tinymce-plugin";
import "@npkg/tinymce-plugin/tpIndent2em";
import "@npkg/tinymce-plugin/tpImportword";
import { Editor } from '@tinymce/tinymce-react';

     class ReactDemo extends React.Component{
       constructor(props) {
         super(props);
           this.reactDemoInit = {
                    height: 500,
                    base_url:'/tinymce',
                    branding: false,
                    language:'zh_CN',
                    menubar: false,
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
          </div>
          );
      }
    }

   ReactDOM.render(<ReactDemo />, document.getElementById('ReactRootID'));
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
                plugins: 'tp code  tpIndent2em autoresize tpCollapse tpTabs tpButtons image  tpImportword preview',
                toolbar: ['|code tpIndent2em tpCollapse tpTabs tpButtons tpImportword | Preview'],
             
        }
    }
  }
}
</script>
```
:::