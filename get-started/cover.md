# 封面

 通过设置 `coverpage` 参数，开启渲染封面。 



## 基本用法

在 `index.html` 文件中添加

```html
<script>
  window.$docsify = {
    coverpage: true
  }
</script>
```

 在文档根目录创建 `_coverpage.md` 文件。

```markdown
# docsify 中文简约指南

>  一个神奇的文档站点生成器。 

-  简单轻巧（~12kb压缩）
-  多个主题 
-  不建立静态HTML文件 
```



## 自定义背景
默认背景是随机生成的渐变色，可以自定义背景色或者背景图。` _coverpage.md `

```markdown
<!-- 背景图片 -->

![](_media/bg.png)

<!-- 背景色 -->

![color](#f0f0f0)
```



## 封面作为首页

默认情况下封面和首页是同时出现的，你可以通过设置将封面独立出来作为首页。



## 多个封面

通过配置显式指定

```js
window.$docsify = {
  coverpage: {
    '/': 'cover.md',
    '/zh-cn/': 'cover.md'
  }
};
```

