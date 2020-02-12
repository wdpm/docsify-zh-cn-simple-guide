# 兼容 Vue

可以直接在 Markdown 文件里写 Vue 代码，它将被执行。



## 基础用法

`index.html` 引入 Vue。

```html
<script src="//unpkg.com/vue"></script>
```

 默认会执行 `new Vue({ el: '#main' })` 创建示例。 

 或者，手动初始化 Vue，自定义一些配置。 

```markdown
# Vue 的基本用法

<div>hello {{ msg }}</div>

<script>
  new Vue({
    el: '#main',
    data: { msg: 'Vue' }
  })
</script>
```

!>  一个 Markdown 文件里只有第一个 `script` 标签内的内容会被执行。 