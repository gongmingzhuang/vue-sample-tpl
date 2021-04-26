# vue-sample-tpl
vue custom sample project template

# 1.初始化node 项目 - npm init

- 生成package.json 文件，用于记录项目的详细信息以及开发中使用的依赖包。
  |- 添加启动命令
  ```javascript
	{
		// serve - 项目启动命令
		// build - 项目打包命令
		"script": {
			"serve": "vue-cli-service serve",
			"build": "vue-cli-service build"
		}
	}
  ```


# 2.添加必要依赖

- vue

> npm install vue -S

- @vue/cli-service - vue-cli命令依赖

> npm install @vue/cli-service -D



# 3.文件系统

- public - 公共资源目录
	|- index.html
- src
	|- assets
	|- components
		|- example
			|- HelloWorld.vue
	|- App.vue
	|- main.js
- .gitignore
- vue.config.js
- README.md


# 4.main.js
```javascript
	import Vue from 'vue'
	import App from './App.vue'

	Vue.config.productionTip = false

	new Vue({
	  render: h => h(App),
	}).$mount('#app')
```


# 5.index.html
```html
	<!DOCTYPE html>
	<html lang="">
	  <head>
	    <meta charset="utf-8">
	    <meta http-equiv="X-UA-Compatible" content="IE=edge">
	    <meta name="viewport" content="width=device-width,initial-scale=1.0">
	    <link rel="icon" href="<%= BASE_URL %>favicon.ico">
	    <title><%= htmlWebpackPlugin.options.title %></title>
	  </head>
	  <body>
	    <div id="app"></div>
	  </body>
	</html>
```


# 6.vue.config.js
```javascript
	module.exports = {
	  publicPath: "./",
	  outputDir: "dist",
	  devServer: {
	    port: 8011
	  }
	}
```


# 7.项目启动/打包

> npm run serve

> npm run build


---
---
--- [end][20210426] ---
