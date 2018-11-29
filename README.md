# vue-vue-cli3.0-jQuery
vue cli3.0 安裝 jQuery


### 安裝jquery

`npm install jquery --save`

### 在package.json中的dependencies檢查是否有 "jquery": "^3.3.1"

```"dependencies": {
    "@babel/core": "^7.1.2",
    "bootstrap": "^4.1.1",
    "jquery": "^3.3.1",
    "popper.js": "^1.14.4",
    "register-service-worker": "^1.0.0",
    "vue": "^2.5.17",
    "vue-resource": "^1.5.1",
    "vue-router": "^3.0.1",
    "vuex": "^3.0.1"
  },
  ```
  
  ### .eslintrc.js 文件中，env 中添加 jquery:true
  
  ```env: {
        node: true,
        jquery: true
    },
    
  ```
  
  ### 自己創vue.config.js 文件後 添加
  
  ```const webpack = require('webpack');
  
      module.exports={
         configureWebpack: {
             plugins: [
                 new webpack.ProvidePlugin({
                     $:"jquery",
                     jQuery:"jquery",
                     "windows.jQuery":"jquery"
                 })
             ]
         }
      }
```

### main.js中 引入 “import $ from 'jquery'”

```import 'jquery'
   import $ from 'jquery';
```
