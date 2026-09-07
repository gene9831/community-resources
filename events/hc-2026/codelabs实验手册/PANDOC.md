# 使用 Pandoc 导出 Word 文档

本项目使用 Pandoc 将 `README.md` 转换为 Word 文档，并通过 `reference.docx`
统一页面、标题、正文、代码块、表格、图注、页眉和页脚样式。

## 准备

安装 [Pandoc](https://pandoc.org/installing.html)，并确认命令可用：

```bash
pandoc --version
```

## 转换

在项目根目录执行：

```bash
pandoc README.md \
  --from=markdown+yaml_metadata_block \
  --to=docx \
  --resource-path=. \
  --reference-doc=reference.docx \
  --syntax-highlighting=tango \
  --output=OpenTiny-Next-集成手册.docx
```
