# Npm pushlish a package process

> Build publish environment

- Init a webpack simple demo

<img src="data:image/png;base64,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" width="200" hegiht="300" align=center style="display:block;margin:20px;"/>

> Developer components

- lib/input/index.vue 文件

  		<template>
  		  <div id="app">
  		  姓名：<input
  		  v-model="inputValue"
  		  type="text"
  		  @change="changeValue" >
  		  </div>
  		  </template>
  		  <script>
  		  export default {
  		  name: 'libInput',
  		  props: {
  		  inputVal: {
  		  type: String,
  		  default: ''
  		  }
  		  },
  		  data () {
  		  return {
  		  inputValue: this.inputVal
  		  }
  		  },
  		  methods: {
  		  changeValue () {
  		  this.\$emit('changeValue', this.inputValue);
  		  }
  		  }
  		  }
  		  </script>

- lib/index.js 文件

      	import libInput from "./input"
      	export default libInput

* Modify package.json [packaged file path]

      	{
      	  "name": "libinput",
      	  "description": "lib input plugin",
      	  "version": "3.2.2",
      	  "author": "刘慧涛 <liuht@mti-sh.cn>",
      	  "license": "MIT",
      	  "private": false,
      	  "main": "dist/libinput.min.js",  //必须添加内容
      	  "scripts": {
      	    "dev": "cross-env NODE_ENV=development webpack-dev-server --open --hot",
      	    "build": "cross-env NODE_ENV=production webpack --progress --hide-modules"
      	  },
      	  ...
      	}

* Modify webpack.config.js ['lib/index.js'：export publish component]

  		var path = require("path")
  		var webpack = require("webpack")

  		module.exports = {
  		  entry: "./src/lib/index.js",
  		  // entry: "./src/main.js",
  		  output: {
  		    path: path.resolve(__dirname, "./dist"),
  		    publicPath: "/dist/",
  		    filename: "libinput.min.js",
  		    // library: "libinput", // library指定的就是你使用require时的模块名，这里便是require("toastPanel")
  		    libraryTarget: "umd", //libraryTarget会生成不同umd的代码,可以只是commonjs标准的，也可以是指amd标准的，也可以只是通过script标签引入的。
  		    umdNamedDefine: true // 会对 UMD 的构建过程中的 AMD 模块进行命名。否则就使用匿名的 define。
  		  },
  		  // 这里我们可以剔除掉一些通用包,自己的包不打包这些类库,需要用户环境来提供
  		 ...
  		}

> Publish package

    npm whoam  //查看登录账户
    npm publish  //发布包

> How use [In new project]

    npm install libinput(package name) --save

    TestComponent.js:
    <template>
      <div id="app">
        <lib-input
          :inputVal="input"
          @changeValue="changeValue"
        ></lib-input>
      </div>
    </template>

    <script>
    import libInput from 'libinput'
    export default {
      name: 'app',
      components: {
        libInput
      },
      data () {
        return {
          input: 'xxxx'
        }
      },
      methods: {
        changeValue (val) {
          // eslint-disable-next-line no-console
          console.log(val)
        }
      }
    }
    </script>

> 注：发布包前修改 .gitignore 文件

    .*
    .DS_Store
    node_modules/
    dist/
    npm-debug.log
    yarn-error.log
    package-lock.json
    webpack.config.js
    index.html
    src/

    # Editor directories and files
    .idea
    *.suo
    *.ntvs*
    *.njsproj
    *.sln
