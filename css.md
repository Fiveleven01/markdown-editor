# 排版样式完全指南

## 使用方式
1. 点击工具栏 **「自定义CSS」**，右侧弹出样式面板
2. 复制下面任意代码粘贴进去，右边立刻看到效果
3. 改数字和颜色来调整
4. 点 **「保存当前」** 起名字，刷新不丢失

---

## 一、标题样式

### 一级标题 H1（文章大标题）

**居中 + 底部短装饰线（推荐）**
```css
h1 {
  font-size: 22px;
  text-align: center;
  border-bottom: none;
}
h1::after {
  content: '';
  display: block;
  width: 50px;           /* 线长，改数字 */
  height: 3px;           /* 线粗细 */
  background: #2ab1ee;   /* 线颜色 */
  margin: 12px auto 0;
  border-radius: 2px;
}
```

**左对齐 + 通栏下划线**
```css
h1 {
  font-size: 22px;
  text-align: left;
  padding-bottom: 10px;
  border-bottom: 2px solid #2ab1ee;
}
```

**居中无装饰**
```css
h1 { font-size: 22px; text-align: center; border-bottom: none; }
```

### 二级标题 H2（章节标题）

**左侧竖线（默认）**
```css
h2 {
  font-size: 18px;
  font-weight: 600;
  padding-left: 14px;
  border-left: 4px solid #2ab1ee;
  color: #2c3e50;
}
```

**居中 + 底部浅灰线**
```css
h2 {
  text-align: center;
  font-size: 18px;
  padding-bottom: 10px;
  border-bottom: 1px solid #e5e5e5;
  border-left: none;
  padding-left: 0;
}
```

### 三级标题 H3

```css
h3 { font-size: 16px; font-weight: 600; color: #444; }
```

---

## 二、正文段落

```css
p {
  font-size: 15px;        /* 字号 14小 15适中 16大 */
  line-height: 1.8;       /* 行距 1.6紧凑 1.8舒适 2.2宽松 */
  color: #333;            /* 文字颜色 */
  letter-spacing: 0.5px;  /* 字间距 */
}
```

---

## 三、代码块（macOS 深色风格）

代码块已经是 macOS 风格（黑底 + 红黄绿圆点）。

```css
/* 代码块背景 */
pre { background: #1e1e1e; border-radius: 10px; }

/* 代码文字 */
pre code { color: #d4d4d4; }

/* 行内代码（正文里的 `code`） */
p code, li code {
  background: #f0f0f0;
  color: #e056a0;
  border-radius: 3px;
  padding: 2px 6px;
}

/* 关掉三个圆点 */
pre::before { display: none; }

/* 改回浅色代码块 */
pre { background: #f5f5f5 !important; }
pre code { color: #333 !important; }
```

---

## 四、颜色速查

| 颜色 | 代码 | 颜色 | 代码 |
|------|------|------|------|
| 纯黑 | `#000000` | 纯白 | `#ffffff` |
| 深灰 | `#333333` | 浅灰 | `#999999` |
| 蓝色 | `#2ab1ee` | 红色 | `#e74c3c` |
| 绿色 | `#27ae60` | 橙色 | `#f39c12` |
| 紫色 | `#8e44ad` | 粉色 | `#e056a0` |

百度搜「颜色代码」有在线取色器。

---

## 五、链接

```css
a {
  color: #2ab1ee;
  text-decoration: none;
  border-bottom: 1px solid rgba(42,177,238,0.3);
}
```

---

## 六、引用块

```css
blockquote {
  border-left: 4px solid #2ab1ee;   /* 左边彩色竖线 */
  background: #f0f9ff;              /* 浅蓝底 */
  color: #555;
  padding: 12px 16px;
  margin: 16px 0;
  border-radius: 0 8px 8px 0;       /* 右侧圆角 */
}
```

---

## 七、图片

Markdown 插入图片写法：`![](图片网址)`

```css
img {
  max-width: 100%;
  border-radius: 8px;       /* 圆角：0无圆角 4小圆角 12大圆角 */
  margin: 16px auto;
  display: block;
  box-shadow: 0 2px 12px rgba(0,0,0,0.08); /* 阴影 */
}
/* 不要阴影 */
img { box-shadow: none; }
/* 不要圆角 */
img { border-radius: 0; }
```

---

## 八、表格

```css
table { width: 100%; border-collapse: collapse; margin: 16px 0; }
th {
  background: #f5f5f5;
  font-weight: bold;
  padding: 8px 12px;
  border: 1px solid #ddd;
}
td {
  padding: 8px 12px;
  border: 1px solid #ddd;
}
```

---

## 九、分割线

```css
hr {
  border: none;
  height: 1px;
  background: #e5e5e5;
  margin: 32px 0;
}
```

---

## 十、列表

```css
ul, ol { padding-left: 24px; margin: 12px 0; }
li { margin: 4px 0; line-height: 1.8; }
```

---

## 十一、粗体强调

```css
strong { color: #000; font-weight: 600; }
```

---

## 十二、一键预设主题

复制整段到自定义CSS即可切换风格。

### 🌊 清新蓝（默认）

```css
h1 { font-size:22px; font-weight:700; margin:32px 0 18px; padding-bottom:12px; border-bottom:2px solid #2ab1ee; color:#2c3e50; text-align:left; }
h2 { font-size:18px; font-weight:600; margin:28px 0 14px; padding-left:14px; border-left:4px solid #2ab1ee; color:#2c3e50; }
h3 { font-size:16px; font-weight:600; margin:22px 0 10px; color:#444; }
p { font-size:15px; line-height:1.8; color:#333; }
a { color:#2ab1ee; text-decoration:none; border-bottom:1px solid rgba(42,177,238,0.3); }
blockquote { border-left-color:#2ab1ee; background:#f0f9ff; }
```

### 🍊 暖橙色

```css
h1 { font-size:22px; font-weight:700; margin:32px 0 18px; padding-bottom:12px; border-bottom:2px solid #e67e22; color:#2c3e50; text-align:left; }
h2 { font-size:18px; font-weight:600; margin:28px 0 14px; padding-left:14px; border-left:4px solid #e67e22; color:#2c3e50; }
h3 { font-size:16px; font-weight:600; margin:22px 0 10px; color:#444; }
p { font-size:15px; line-height:1.8; color:#333; }
a { color:#e67e22; text-decoration:none; border-bottom:1px solid rgba(230,126,34,0.3); }
blockquote { border-left-color:#e67e22; background:#fef9f3; }
```

### 🍇 优雅紫

```css
h1 { font-size:22px; font-weight:700; margin:32px 0 18px; text-align:center; border-bottom:none; color:#2c3e50; }
h1::after { content:''; display:block; width:50px; height:3px; background:#8e44ad; margin:12px auto 0; border-radius:2px; }
h2 { font-size:18px; font-weight:600; margin:28px 0 14px; padding-left:14px; border-left:4px solid #8e44ad; color:#2c3e50; }
h3 { font-size:16px; font-weight:600; margin:22px 0 10px; color:#444; }
p { font-size:15px; line-height:1.8; color:#333; }
a { color:#8e44ad; text-decoration:none; border-bottom:1px solid rgba(142,68,173,0.3); }
blockquote { border-left-color:#8e44ad; background:#f9f5fb; }
```

### ⚫ 极简黑白

```css
h1 { font-size:22px; font-weight:700; margin:32px 0 18px; color:#000; text-align:left; border-bottom:none; }
h2 { font-size:18px; font-weight:600; margin:28px 0 14px; color:#000; border-left:none; padding-left:0; }
h3 { font-size:16px; font-weight:600; margin:22px 0 10px; color:#000; }
p { font-size:15px; line-height:1.8; color:#333; }
a { color:#000; text-decoration:underline; border-bottom:none; }
blockquote { border-left:2px solid #000; background:#fafafa; color:#555; }
```

---

## 常见问题

**Q: 改了没效果？**
A: CSS 所有符号必须是英文的。检查分号 `;`、冒号 `:`、花括号 `{}` 是否是英文半角。

**Q: 怎么让标题居中？**
A: 加 `text-align: center;`

**Q: 怎么让标题恢复左对齐？**
A: 加 `text-align: left;`

**Q: 代码块圆点去不掉？**
A: `pre::before { display: none; }`

**Q: 代码块改回白色？**
A: `pre { background: #f5f5f5 !important; } pre code { color: #333 !important; }`

**Q: 字体怎么换微软雅黑？**
A: `* { font-family: "微软雅黑", sans-serif; }`
