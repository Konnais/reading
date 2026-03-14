# 我的英文原著词汇库

个人使用备忘。

## 文件结构

```
reading/
├── index.html                                    ← 书目首页，从这里进入
├── README.md                                     ← 本文件
├── 001-the-last-three-minutes/
│   ├── 001_Preface_Notes.html                    ← 带原文的阅读版
│   └── vocab_cards.html                          ← 纯词卡版
├── 002-SPQR-a-history-of-ancient-rome/
│   ├── 001_xxx.html
│   └── vocab_cards.html
└── 003-why-evolution-is-true/
    ├── 001_xxx.html
    └── vocab_cards.html
```

## 访问地址

```
https://konnais.github.io/reading/
https://konnais.github.io/reading/001-the-last-three-minutes/001_Preface_Notes.html
```

## 使用流程

1. 用微信读书或Kindle阅读英文原著
2. 遇到生词，在Markdown编辑器中用 **加粗** 标注
3. 发给Claude处理，获得带音标、词性、释义的词汇列表
4. Claude同步生成 reading.html 和 vocab_cards.html
5. 上传到对应书目文件夹，更新 index.html 的书目信息
6. iPad Safari访问 index.html，开始学习
7. 配合Kindle Whispersync听读强化

## 添加新书步骤

1. 在本地仓库新建文件夹，命名规则：`00X-书名`（如 `002-SPQR-a-history-of-ancient-rome`）
2. 把 reading.html 和 vocab_cards.html 放入文件夹，按章节命名（如 `001_Chapter1.html`）
3. 在 index.html 中把对应的占位卡片改为正式卡片，填入链接
4. 更新顶部统计数字
5. GitHub Desktop：Commit → Push

## 注意事项

- 已掌握状态保存在浏览器本地（localStorage），换设备后需重新标记
- 词汇释义仅保留原文中的含义，不是词典的全部释义
- reading.html 点击生词会自动朗读（需要网络加载Google字体，离线时字体降级但功能正常）
