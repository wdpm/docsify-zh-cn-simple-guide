# 多页文档

假设多页文档的目录结构如下：

- demo/
  - README.md
  - guide.md
  - zh-cn/
    - README.md
    - guide.md

那么访问路由为

```
demo/README.md        => http://localhost:3000/#/
demo/guide.md         => http://localhost:3000/#/guide
demo/zh-cn/README.md  => http://localhost:3000/#/zh-cn/
demo/zh-cn/guide.md   => http://localhost:3000/#/zh-cn/guide
```

路由和文件目录非常类似。



## 定制侧边栏

1. 配置 ` loadSidebar `选项。

   ```html
   <script>
     window.$docsify = {
       loadSidebar: true
     }
   </script>
   ```

2.  创建 `_sidebar.md` 文件 

   ```
   - [首页](zh-cn/)
   - [指南](zh-cn/guide)
   ```

`_sidebar.md` 加载逻辑是从每层目录下获取文件，如果当前目录不存在该文件则回退到上一级目录。例如当前路径为 `/zh-cn/more-pages` 则从 `/zh-cn/_sidebar.md` 获取文件，如果不存在则从 `/_sidebar.md` 获取。

3. 【可选】显式配置alias避免回退

   ```html
   <script>
     window.$docsify = {
       loadSidebar: true,
       alias: {
         '/.*/_sidebar.md': '/_sidebar.md'
       }
     }
   </script
   ```

   `/.*/_sidebar.md ` 为 key ，`/_sidebar.md ` 为 value ，说明直接以 `/_sidebar.md` 该文件作为侧边栏配置。

开启侧边栏之后，你会发现访问 localhost:3000 时没有见到侧边栏的目录。



## 重新显示目录

 设置 `subMaxLevel` 配置项 

```html
<script>
  window.$docsify = {
    loadSidebar: true,
    subMaxLevel: 2 //这个值的含义后面会细讲
  }
</script>
```



## 忽略副标题

 当设置了 `subMaxLevel` 时，默认情况下每个标题都会自动添加到目录中 。

你可以忽略特定的副标题

```markdown
# Getting Started
## Header {docsify-ignore}
```

你也可以忽略所有标题

```markdown
# Getting Started {docsify-ignore-all}
## Header
```

