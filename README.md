# WebRoot

DataEye内部Java项目前端框架模板

## 安装

首先安装`Node.js`

[下载地址](http://www.nodejs.org)

安装完成之后执行：

```bash
npm install -g gulp-cli
```

其它说明：

> * 资源打包合并见根目录gulpfile.js
> * AMD资源优化使用r.js
> * 国际化采用预处理方式而不是传统的字典引用

## 运行

请在本地运行一个Web Server，比如apache，然后使用localhost打开page目录下的文件。

不要直接打开html文件，这样不起作用。

## assets

静态资源目录，包含:

> * components: Ractive组件(html)
> * css
> * fonts (font-awsome & bootstrap)
> * img 
> * js 

### assets/components

single file components，最终会被转换为js文件。

转换后的JS文件需要国际化（预处理），输出三个语言版本。

### js/app

业务脚本全部放这里

### js/bootstrap

bootstrap的JS插件

### js/ie8

ie8兼容处理脚本

## tpl

全部JSP页面模板。

开发环境使用requirejs的text插件加载。
生产环境会将其转换为AMD模块（builde config设置stubModules: ['text']）。
最终打包输出到app.js。

所以app.js需要国际化（预处理），输出三个语言版本
