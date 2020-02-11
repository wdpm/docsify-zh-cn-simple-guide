# 定制导航栏

## 方法一

直接在 `index.html` 文件中添加，注意链接要以 `#/` 开头。

```html
<nav>
    <a href="#/">EN</a>
    <a href="#/zh-cn/">中文</a>
</nav>
```

## 方法二

通过配置文件配置。

`index.html` 配置 `loadNavbar`

```html
<script>
  window.$docsify = {
    loadNavbar: true
  }
</script>
```

根目录创建文件 `_navbar.md` 

```markdown
- [En](/)
- [中文](/zh-cn/)
```

 `_navbar.md` 加载逻辑和 `sidebar` 文件一致，从每层目录下获取。例如当前路由为 `/zh-cn/custom-navbar` 那么是从 `/zh-cn/_navbar.md` 获取导航栏。 

