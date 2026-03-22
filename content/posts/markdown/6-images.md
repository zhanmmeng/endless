---
title: "图片语法"
date: 2026-03-22T00:00:00+08:00
draft: true
slug: md-images
weight: 6
---

###### Markdown图片语法
----------------------

### 基本图片语法

图片语法与链接类似，但在前面加上感叹号 `!`。

| Markdown 语法 | 渲染效果 |
|--------------|----------|
| <code>`![替代文本](图片URL)`</code> | 显示图片 |
| <code>`![替代文本](图片URL "图片标题")`</code> | 鼠标悬停显示标题 |

#### 示例

```markdown
![风景图](https://picsum.photos/400/200)
![带有标题的图片](https://picsum.photos/400/200 "这是一张风景图")
```

#### 渲染效果

![风景图](https://picsum.photos/400/200)
![带有标题的图片](https://picsum.photos/400/200 "这是一张风景图")

---
### 相对路径图片

引用项目内的图片文件。

#### 示例

```markdown
![本地图片](./images/photo.png)
![子目录图片](../assets/banner.jpg)
```

#### 渲染效果

![本地图片](./images/photo.png)
![子目录图片](../assets/banner.jpg)

**推荐目录结构**：
```
project/
├── images/
│   └── photo.png
└── docs/
    └── article.md
```

---
### 引用式图片

与引用式链接类似，将图片 URL 定义在文档末尾。

#### 示例

```markdown
这是 ![风景图][img1]。
这是 ![头像][img2]。

[img1]: https://picsum.photos/400/200 "风景"
[img2]: https://picsum.photos/100/100 "头像"
```

#### 渲染效果

这是 ![风景图][img1]。
这是 ![头像][img2]。

[img1]: https://picsum.photos/400/200 "风景"
[img2]: https://picsum.photos/100/100 "头像"

---
### 带链接的图片

将图片嵌入链接中，点击图片可跳转。

#### 示例

```markdown
[![风景图](https://picsum.photos/200/100)](https://example.com)
```

#### 渲染效果

[![风景图](https://picsum.photos/200/100)](https://example.com)

---
### HTML 设置图片尺寸

标准 Markdown 不支持设置图片尺寸，但可以使用 HTML。

#### 示例

```markdown
<img src="https://picsum.photos/400/200" width="200" height="100" alt="缩小的图片">
```

#### 渲染效果

<img src="https://picsum.photos/400/200" width="200" height="100" alt="缩小的图片">

---
### 注意事项

1. **替代文本**
   - 始终提供有意义的替代文本
   - 用于屏幕阅读器和图片加载失败时显示
   - 避免使用"图片"、"图像"等无意义文本

2. **图片格式**
   - 常用格式：PNG、JPG、GIF、SVG
   - SVG 支持无损缩放，适合图标和插图
   - WebP 格式压缩率高，但兼容性稍差

3. **图片优化**
   - 压缩图片文件大小
   - 使用适当的分辨率（不用高清图显示小缩略图）
   - 考虑使用 CDN 加速图片加载

4. **兼容性**
   - 基本图片语法是 **CommonMark 核心规范**
   - HTML 扩展支持因平台而异

5. **最佳实践**
   - 使用相对路径引用项目内图片
   - 将图片集中存放在 `images/` 或 `assets/` 目录
   - 为大图提供缩略图版本
