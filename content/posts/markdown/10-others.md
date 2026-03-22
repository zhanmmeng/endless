---
title: "其他语法"
date: 2026-03-22T00:00:00+08:00
draft: true
slug: md-others
weight: 10
---

###### Markdown其他语法
----------------------

### 分隔线

使用三个或更多的 `*`、`-` 或 `_` 创建分隔线。

#### 示例

```markdown
***

---

___
```

#### 渲染效果

***

---

___

**注意**：
- 符号之间可以有空格
- 每行只能使用一种符号

---

### 任务列表

使用 `- [ ]` 和 `- [x]` 创建任务列表（GFM 扩展）。

#### 示例

```markdown
- [x] 已完成的任务
- [ ] 未完成的任务
- [ ] 待办事项

### 任务嵌套

- [ ] 主任务
  - [x] 子任务1
  - [ ] 子任务2
```

#### 渲染效果

- [x] 已完成的任务
- [ ] 未完成的任务
- [ ] 待办事项

### 任务嵌套

- [ ] 主任务
  - [x] 子任务1
  - [ ] 子任务2

---

### 自动链接

使用 `< >` 包裹 URL 会自动转换为可点击链接。

#### 示例

```markdown
<https://github.com>
<example@email.com>
```

#### 渲染效果

<https://github.com>
<example@email.com>

---

### HTML 标签

Markdown 支持直接嵌入 HTML 标签。

#### 示例

```markdown
<div style="color: red;">
  这段文字是红色的。
</div>

<details>
<summary>点击展开</summary>
隐藏的内容
</details>
```

#### 渲染效果

<div style="color: red;">
  这段文字是红色的。
</div>

<details>
<summary>点击展开</summary>
隐藏的内容
</details>

**常用 HTML 标签**：
- `<br>` - 换行
- `<details>` / `<summary>` - 折叠内容
- `<kbd>` - 键盘按键样式
- `<mark>` - 高亮文本
- `<sub>` / `<sup>` - 下标/上标

---

### 转义字符

使用反斜杠 `\` 转义特殊字符，使其原样显示。

#### 可转义的字符

```
\   反斜杠
`   反引号
*   星号
_   下划线
{}  大括号
[]  中括号
()  小括号
#   井号
+   加号
-   减号
.   点号
!   感叹号
|   竖线
```

#### 示例

```markdown
\**不是粗体\*
\[不是链接\](不是URL)
```

#### 渲染效果

\**不是粗体\*
\[不是链接\](不是URL)

---

### Emoji

某些平台支持 `:emoji-code:` 格式的表情符号。

#### 示例

```markdown
:smile:
:heart:
:thumbsup:
```

#### 渲染效果

:smile:
:heart:
:thumbsup:

**注意**：这是平台特定功能，标准 Markdown 不支持。

---

### 脚注

某些编辑器支持脚注语法。

#### 示例

```markdown
这是一句话[^1]。

[^1]: 这是脚注内容。
```

**注意**：脚注不是标准 Markdown，支持程度因平台而异。

---

### 注意事项

1. **兼容性**
   - 分隔线和转义字符是 **CommonMark 核心规范**
   - 任务列表、脚注是 **扩展语法**
   - HTML 支持因平台安全策略而异

2. **最佳实践**
   - 优先使用标准语法
   - 扩展语法确认平台支持后再使用
   - 复杂格式考虑使用 HTML

3. **Markdown 变体**
   - GFM (GitHub Flavored Markdown)
   - CommonMark
   - Pandoc's Markdown
   - MultiMarkdown
   - 不同变体支持的扩展语法不同
