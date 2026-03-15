# 我的英文原著词汇库

个人使用备忘。

## 访问地址

```
https://konnais.github.io/reading/
```

## 当前进度

| 书目 | 章节 | 词汇数 |
|------|------|--------|
| The Last Three Minutes | Preface | 77 |
| The Last Three Minutes | Chapter 1: Doomsday | 107 |
| **合计** | | **184** |

## 文件结构

```
reading/
├── index.html                                        ← 书库首页
├── README.md                                         ← 本文件
├── 001-the-last-three-minutes/
│   ├── 001_Preface_Notes.html                        ← 带原文，点击生词弹出卡片+自动朗读
│   ├── 001_Preface_Cards.html                        ← 词卡平铺，点击自动朗读
│   ├── 002_Ch01_Notes.html                           ← Chapter 1 阅读版
│   └── 002_Ch01_Cards.html                           ← Chapter 1 词卡版
├── 002-SPQR-a-history-of-ancient-rome/               ← 即将开始
└── 003-why-evolution-is-true/                        ← 即将开始
```

## 文件命名规则

- 文件夹：`00X-书名`（如 `001-the-last-three-minutes`）
- 文件：`00X_章节名_Notes.html` 和 `00X_章节名_Cards.html`

## 卡片弹窗内容

每个单词弹窗显示（字体均为28px）：

- 单词（大字标题）
- 音标
- 词性
- 英文释义
- 中文释义
- 近义词（≈ 开头）

## 功能说明

| 功能 | Notes | Cards |
|------|-------|-------|
| 点击生词弹出卡片 | ✓ | ✓ |
| 自动朗读 | ✓ | ✓ |
| 空格键关闭弹窗 | ✓ | ✓ |
| 标记已掌握 | ✓ | ✓ |
| 标记待复习 | — | ✓ |
| 随机排列 | — | ✓ |
| 仅显示英文 | — | ✓ |
| 筛选（全部/已掌握/待复习/未标记）| — | ✓ |

## 使用流程

1. 用微信读书或 Kindle 阅读英文原著
2. 遇到生词，在 Markdown 编辑器中用 **加粗** 标注
3. 发给 Claude 处理，获得带音标、词性、释义、近义词的词汇列表
4. Claude 同步生成 `_Notes.html` 和 `_Cards.html`
5. 放入对应书目文件夹，在 `index.html` 中添加章节链接
6. GitHub Desktop：Commit → Push
7. iPad/iPhone Safari 访问 `index.html`，开始学习
8. 配合 Kindle Whispersync 听读强化

## 在 index.html 中添加新章节

在对应书目的 `<ul class="chapter-list">` 内添加：

```html
<li class="chapter-item">
  <div class="chapter-info">
    <div class="chapter-name"><span class="chapter-num">003</span>Chapter 2 — 章节名</div>
    <div class="chapter-words">XX 词</div>
  </div>
  <div class="chapter-btns">
    <a class="chapter-btn primary" href="001-the-last-three-minutes/003_Ch02_Notes.html">📖 Notes</a>
    <a class="chapter-btn" href="001-the-last-three-minutes/003_Ch02_Cards.html">🗂 Cards</a>
  </div>
</li>
```

同时更新顶部统计中的累计词汇数。

## 注意事项

- 已掌握状态保存在浏览器本地（localStorage），换设备后需重新标记
- 词汇释义仅保留原文中的含义，不是词典的全部释义
- 近义词为文中语境下的近义参考，帮助记忆
- 需要联网加载 Google 字体；离线时字体降级，功能完全正常
