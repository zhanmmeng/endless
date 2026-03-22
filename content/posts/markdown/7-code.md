---
title: "代码语法"
date: 2026-03-22T00:00:00+08:00
draft: true
slug: md-code
weight: 7
---

###### Markdown代码语法
----------------------

### 行内代码

使用反引号 `` ` `` 包裹代码。

| Markdown 语法 | 渲染效果 |
|--------------|----------|
| <code>`\`const x = 1;\``</code> | `const x = 1;` |

#### 示例

```markdown
使用 `print()` 函数输出内容。
在 JavaScript 中用 `console.log()` 打印日志。
```

#### 渲染效果

使用 `print()` 函数输出内容。
在 JavaScript 中用 `console.log()` 打印日志。

---
### 代码块

使用三个反引号 <code>```</code> 包裹代码块。

#### 示例

````
```python
def hello():
    print("Hello, World!")
```
````

#### 渲染效果

```python
def hello():
    print("Hello, World!")
```

---
### 语法高亮

在代码块开头的反引号后指定语言。

#### 支持的语言示例

| 语言 | 标识符 | 示例 |
|------|--------|------|
| Python | `python` / `py` | <code>```python</code> |
| JavaScript | `javascript` / `js` | <code>```javascript</code> |
| Java | `java` | <code>```java</code> |
| C/C++ | `c` / `cpp` | <code>```cpp</code> |
| Bash | `bash` / `sh` | <code>```bash</code> |
| JSON | `json` | <code>```json</code> |
| CSS | `css` | <code>```css</code> |
| HTML | `html` | <code>```html</code> |

#### 示例

````
```javascript
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet('World');
```
````

#### 渲染效果

```javascript
function greet(name) {
  console.log(`Hello, ${name}!`);
}

greet('World');
```

---
### 缩进代码块

使用 **4 个空格** 或 **1 个 Tab** 缩进的文本会被识别为代码块（这是原始 Markdown 语法）。

#### 示例

```markdown
这是一段普通文字。

    def hello():
        print("Indented code block")

这又回到了普通文字。
```

#### 渲染效果

这是一段普通文字。

    def hello():
        print("Indented code block")

这又回到了普通文字。

**注意**：这种语法在现代编辑器中较少使用，推荐使用围栏代码块（三个反引号）。

---
### 转义反引号

要在行内代码中显示反引号，使用多个反引号包裹。

#### 示例

```markdown
使用 `` ` `` 可以表示行内代码。
```

#### 渲染效果

使用 `` ` `` 可以表示行内代码。

---
### 代码块中的特殊字符

代码块中的特殊字符（如 `<`、`>`、`*`）会被原样显示，无需转义。

#### 示例

````
```html
<div class="container">
  <p>这是一个段落</p>
</div>
```
````

#### 渲染效果

```html
<div class="container">
  <p>这是一个段落</p>
</div>
```

---
### 注意事项

1. **语法高亮**
   - 语言标识符小写
   - 不同平台支持的语言列表不同
   - 常见语言基本都支持

2. **代码块内空行**
   - 代码块内可以有空行
   - 不会被误认为代码块结束

3. **复制代码**
   - 许多编辑器会在代码块右上角显示复制按钮
   - 方便读者复制代码

4. **行号**
   - 标准 Markdown 不支持行号
   - 某些编辑器（如 GitHub）通过扩展支持

5. **最佳实践**
   - 始终指定语言以启用语法高亮
   - 使用围栏代码块（三个反引号）而非缩进
   - 代码示例要简洁、可运行
