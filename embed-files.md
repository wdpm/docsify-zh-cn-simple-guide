# 文件嵌入

docsify 4.6 开始支持嵌入任何类型的文件到文档。可以将文件当成 `iframe`、`video`、`audio` 或者 `code block`，如果是 Markdown 文件，可以直接插入到当前文档。 



## 嵌入的类型

- **iframe** `.html`, `.htm`
- **markdown** `.markdown`, `.md`
- **audio** `.mp3`
- **video** `.mp4`, `.ogg`
- **code** other file extension



## 标签属性

如果嵌入文件是一个 `iframe`、`audio` 或 `video`，可以给这些标签设置属性。 

```markdown
[cinwell website](https://cinwell.com ':include :type=iframe width=100% height=400px')
```

