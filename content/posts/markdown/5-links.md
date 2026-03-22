---
title: "链接"
date: 2026-03-22T00:00:00+08:00
draft: false
slug: md-links
weight: 5
---

###### Markdown链接语法
----------------------

### 基本链接

| Markdown 语法 | 渲染效果 |
|--------------|----------|
| <code>`[链接文本](https://example.com)`</code> | [链接文本](https://example.com) |
| <code>`[链接文本](https://example.com "标题")`</code> | [链接文本](https://example.com "标题")（鼠标悬停显示标题） |

#### 示例

```markdown
[GitHub](https://github.com)  
[Google 搜索](https://google.com "点击搜索")
```

#### 渲染效果

[GitHub](https://github.com)  
[Google 搜索](https://google.com "点击搜索")

---
### 相对路径链接

在纯 Markdown 文件中，可以使用相对路径链接到同一项目内的其他文件。

#### 示例

```markdown
[查看标题语法](../md-headings)

[返回上级](../_index.md)
```

#### 渲染效果

[查看标题语法](../md-headings)

[返回上级](../)


---
### 引用式链接

将链接 URL 和标题定义在文档末尾，正文中通过引用 ID 使用。

#### 示例

```markdown
这是 [GitHub][gh] 的链接。  
这是 [Google][goog] 的链接。

[gh]: https://github.com "GitHub"  
[goog]: https://google.com "Google"
```

#### 渲染效果

这是 [GitHub][gh] 的链接。  
这是 [Google][goog] 的链接。

[gh]: https://github.com "GitHub"  
[goog]: https://google.com "Google"

**优点**：
- 链接集中管理，便于维护
- 文档更易读
- 重复使用的链接只需定义一次

---
### 邮箱链接

#### 示例

```markdown
[联系我](mailto:example@email.com)
<example@email.com>
```

#### 渲染效果

[联系我](mailto:example@email.com)  
<example@email.com>

---
### 锚点链接

链接到文档内的某个标题（大多数 Markdown 编辑器自动生成锚点）。

#### 示例

```markdown
[跳转到基本链接](#基本链接)
```

#### 渲染效果

[跳转到基本链接](#基本链接)

**注意**：锚点规则因平台而异（GitHub 会将标题转为小写并替换空格为 `-`）。

---
### URL 作为链接

可以直接使用 URL，Markdown 会自动转换为链接。

#### 示例

```markdown
访问 https://github.com 了解更多。
```

#### 渲染效果

访问 https://github.com 了解更多。

---
### 注意事项

1. **特殊字符**
   - 链接 URL 中的空格应编码为 `%20`
   - 圆括号等特殊字符需要转义或使用 URL 编码

2. **安全性**
   - 链接标题使用双引号包裹


3. **兼容性**
   - 基本链接和引用式链接都是 **CommonMark 核心规范**
   - 所有 Markdown 编辑器都支持

