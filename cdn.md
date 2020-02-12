# CDN

保守又兼顾性能的做法：指定版本的压缩版。

乐观又兼顾性能的做法：最新版本的压缩版。



## 最新版本

根据 UNPKG 的规则，不指定特定版本号时将引入最新版。

 

## 指定版本

如果担心版本更新可能引入未知 Bug，可以使用具体的版本。规则是 `//unpkg.com/docsify@VERSION/` 

```html
<!-- 引入 css -->
<link rel="stylesheet" href="//unpkg.com/docsify@2.0.0/themes/vue.css">

<!-- 引入 script -->
<script src="//unpkg.com/docsify@2.0.0/lib/docsify.js"></script>
```



## 压缩版

 CSS 的压缩文件位于 `/lib/themes/` 目录下 

```html
<link rel="stylesheet" href="//unpkg.com/docsify/lib/themes/vue.css">
```

JS 的压缩文件是原有文件路径的基础上加 `.min`后缀

```html
<script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
```



## 其他 CDN

- http://www.bootcdn.cn/docsify (支持国内) 