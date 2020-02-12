# 配置项



## el

 docsify 初始化的挂载元素，可以是一个 CSS 选择器，默认为 `#app` 。



## repo

配置仓库地址或者 `username/repo` 的字符串，在页面右上角渲染一个 [GitHub Corner](http://tholman.com/github-corners/) 挂件。 

```js
window.$docsify = {
  repo: 'https://github.com/wdpm/docsify-zh-cn-simple-guide'
};
```



## maxLevel

 默认情况下会抓取文档中所有标题渲染成目录，可配置最大支持渲染的标题层级。 默认值为6。

```js
window.$docsify = {
  maxLevel: 4
};
```



## loadNavbar

加载自定义导航栏。设置为 `true` 后会加载 `_navbar.md` 文件。 

```js
window.$docsify = {
  // 加载 _navbar.md
  loadNavbar: true
};
```



## loadSidebar

 加载自定义侧边栏。设置为 `true` 后会加载 `_sidebar.md` 文件。

```js
window.$docsify = {
  // 加载 _sidebar.md
  loadSidebar: true
};
```



## subMaxLevel

 自定义侧边栏后默认不会再生成目录，可以通过设置生成目录的最大层级开启这个功能。 

```js
window.$docsify = {
  subMaxLevel: 2
};
```



## auto2top

切换页面后是否自动跳转到页面顶部。 

```js
window.$docsify = {
  auto2top: true
};
```



## homepage

设置首页文件加载路径。 适合不想将 `README.md` 作为入口文件渲染。

```js
window.$docsify = {
  // 入口文件改为 /home.md
  homepage: 'home.md'
};
```



## basePath

文档加载的根路径，可以是二级路径或者是其他域名的路径。 

```js
window.$docsify = {
  basePath: '/docs/',

  // 直接渲染其他域名的文档
  basePath: 'https://docsify.js.org/'
};
```



## coverpage

开启后加载 `_coverpage.md` 文件，也可以自定义文件名。 

```js
window.$docsify = {
  coverpage: true,

  // 自定义文件名
  coverpage: 'cover.md'
};
```



## logo

在侧边栏中出现的网站图标，你可以使用`CSS`来更改大小。

```js
window.$docsify = {
  logo: '/_media/icon.svg'
};
```



## name

文档标题，会显示在侧边栏顶部。 

```js
window.$docsify = {
  name: 'XXX'
};
```



## markdown

 参考 Markdown 配置。 



## themeColor

 替换主题色。利用 [CSS3 支持变量](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_variables)的特性，对于老的浏览器有 polyfill 处理。 

```js
window.$docsify = {
  themeColor: '#3F51B5'
};
```



## alias

定义路由别名，可以更自由的定义路由规则。 支持正则。 

```js
window.$docsify = {
  alias: {
    '/foo/(+*)': '/bar/$1', // supports regexp
    '/zh-cn/changelog': '/changelog'
  }
};
```



## executeScript

执行文档里的 script 标签里的脚本。 如果 Vue 存在，则自动开启。 

> !如果执行的是一个外链脚本，比如 jsfiddle 的内嵌 demo，请确保引入 [external-script](https://docsify.js.org/#/plugins?id=外链脚本-external-script) 插件。 



## mergeNavbar

小屏设备下合并导航栏到侧边栏。 

```js
window.$docsify = {
  mergeNavbar: true
};
```



## formatUpdated

可以通过 **{docsify-updated}** 变量显示文档更新日期. 并且通过 `formatUpdated` 配置日期格式。参考 https://github.com/lukeed/tinydate#patterns 

```js
window.$docsify = {
  formatUpdated: '{MM}/{DD} {HH}:{mm}',

  formatUpdated: function(time) {
    // ...
    return time;
  }
};
```



## routerMode

```js
window.$docsify = {
  routerMode: 'history' // default: 'hash'
};
```



## fallbackLanguages

 一个语言列表。 倒退机制时使用。



## notFoundPage

加载正确的本地化过的404页面:

```js
window.$docsify = {
  notFoundPage: {
    '/': '_404.md',
    '/de': 'de/_404.md'
  }
};
```

!>  注意: 配置过`fallbackLanguages`选项的页面与选项`notFoundPage`冲突。 

