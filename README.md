# 我的英文原著词汇库

个人使用备忘。

## 访问地址

```
https://konnais.github.io/reading/
```

## 文件结构

```
reading/
├── index.html                                      ← 书库首页
├── README.md                                       ← 本文件
├── 001-the-last-three-minutes/
│   ├── 001_Preface_Notes.html                      ← 带原文，点击生词弹出卡片+自动朗读
│   └── 001_Preface_Cards.html                      ← 词卡平铺，点击自动朗读
├── 002-SPQR-a-history-of-ancient-rome/
│   ├── 001_xxx_Notes.html
│   └── 001_xxx_Cards.html
└── 003-why-evolution-is-true/
    ├── 001_xxx_Notes.html
    └── 001_xxx_Cards.html
```

## 文件命名规则

- 文件夹：`00X-书名`（如 `001-the-last-three-minutes`）
- 文件：`00X_章节名_Notes.html` 和 `00X_章节名_Cards.html`

## 使用流程

1. 用微信读书或 Kindle 阅读英文原著
2. 遇到生词，在 Markdown 编辑器中用 **加粗** 标注
3. 发给 Claude 处理，获得带音标、词性、释义的词汇列表
4. Claude 同步生成 `_Notes.html` 和 `_Cards.html`
5. 放入对应书目文件夹，在 `index.html` 中添加章节链接
6. GitHub Desktop：Commit → Push
7. iPad Safari 访问 `index.html`，开始学习
8. 配合 Kindle Whispersync 听读强化

## 在 index.html 中添加新章节

每本书的章节列表用 `<li>` 条目表示，格式如下：

```html
<li class="chapter-item">
  <div class="chapter-info">
    <div class="chapter-name"><span class="chapter-num">002</span>Chapter 1 — The Beginning</div>
    <div class="chapter-words">65 词</div>
  </div>
  <div class="chapter-btns">
    <a class="chapter-btn primary" href="001-the-last-three-minutes/002_Chapter1_Notes.html">📖 Notes</a>
    <a class="chapter-btn" href="001-the-last-three-minutes/002_Chapter1_Cards.html">🗂 Cards</a>
  </div>
</li>
```

## 快捷键

- **空格键**：关闭弹出的单词卡片（Notes 和 Cards 均支持）

## 注意事项

- 已掌握状态保存在浏览器本地（localStorage），换设备后需重新标记
- 词汇释义仅保留原文中的含义，不是词典的全部释义
- 需要联网加载 Google 字体；离线时字体降级，但功能完全正常
