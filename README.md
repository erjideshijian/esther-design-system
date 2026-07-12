# 🍃 莉亚学ai · 个人品牌设计系统

一套给 AI 看的个人品牌设计系统，基于「森林墨（Forest Ink）」暖调知性风格。

把审美写成操作手册，AI 每次帮你做页面时必须翻这本手册，不能自由发挥。**限制 AI 的自由度 = 保证输出质量。**

> ⚠️ **使用前请先确认配置：** 品牌色已配置为森林墨配色。放入你自己的头像到 `assets/avatar.jpg` 即可开始使用。

---

## 🎨 品牌 DNA

| 色名 | 色值 | 作用 |
|------|------|------|
| 🌲 森林绿 — 主色 | `#2D5A3D` | 标题、链接、重点标记（60%） |
| 🌟 暖金色 — 强调色 | `#E8C99B` | 装饰、badges、高亮（30%） |
| 🍅 陶土红 — 点缀色 | `#C4716B` | CTA、标签、小面积亮点（10%） |

**气质**: 温暖知性 · 森林感 · 学习陪伴 · 不像 AI · 简洁有细节

---

## 核心逻辑

```
SKILL.md(流程 - AI 按什么步骤干活)
    ↓
brand-dna.md + references/*(规范 - 能用什么不能用什么)
    ↓
assets/template-*.html(起点 - 从模板改,不从零写)
```

- AI 不能随便发明布局 → 只能从 16 种里选
- AI 不能随便用颜色 → 只能用你定义的品牌色 + 扩展规则
- AI 不能随便写样式 → 必须从组件库里选
- AI 做完要自检 → 对照 checklist 逐条过，P0 不过就打回

---

## 文件结构

```
esther-design-system/
├── SKILL.md                    ← 7步工作流(大脑)
├── brand-dna.md                ← 品牌基因:颜色/字体/气质/禁忌(需配置)
├── assets/                     ← 模板骨架(起点)
│   ├── template-tutorial.html      教程页模板
│   ├── template-landing.html       活动页模板
│   ├── template-app.html           App型模板
│   ├── template-cards.html         小红书卡片模板
│   ├── html2canvas.min.js          卡片导出依赖
│   ├── avatar-placeholder.svg      占位头像(可替换为你自己的 avatar.jpg)
│   └── avatar.jpg                  ← 你的头像(需自行放入,仓库未附带)
└── references/                 ← 规则和零件(知识库)
    ├── layouts.md                  16种布局模式(附完整代码)
    ├── components.md               组件库(51组件,完整HTML+CSS)
    ├── checklist.md                质量检查清单(P0/P1/P2)
    ├── scene-tutorial.md           教程场景规范
    ├── scene-landing.md            活动页场景规范
    ├── scene-app.md                App型场景规范
    ├── scene-cards.md              小红书卡片场景规范
    └── scene-wechat.md             公众号排版场景规范
```

---

## 7 步工作流

AI 每次做设计必须按这个顺序走：

| # | 做什么 | 为什么 |
|---|--------|--------|
| 1 | 问 5 个问题(类型/受众/几屏/素材/约束)。类型含：教程/活动页/App/卡片/**公众号** | 不自作主张 |
| 2 | 读 brand-dna + 对应场景文件 | 先学规矩再动手 |
| 3 | 从 assets/ 复制对应模板 | 从半成品开始，不从零写 |
| 4 | 从 layouts.md 选 3-5 种布局 | 每个 section 不能一样 |
| 5 | 从 components.md 选组件 | 禁止用 HTML 默认样式 |
| 6 | 对照 checklist 自检 | P0 不过就打回 |
| 7 | 交付 HTML 文件 | 浏览器打开就能看 |

---

## 品牌基因速览

### 三色（森林墨 Forest Ink）

| 颜色 | 色值 | 比例 |
|------|------|------|
| 主色 | `#2D5A3D` | 60% |
| 强调色 | `#E8C99B` | 30% |
| 点缀色 | `#C4716B` | 10% |

### 字体

| 用途 | 字体 |
|------|------|
| 中文标题 | 汇文明朝体 / Noto Serif SC |
| 中文正文 | Noto Sans SC |
| 英文装饰 | Fraunces italic |
| 手写/注释 | Caveat |
| 代码/终端 | Fira Code |

### 气质关键词

温暖知性 · 森林感 · 学习陪伴 · **不像 AI** · 简洁有细节 · 一看就是「莉亚学ai」

### 禁忌

蓝紫渐变 · glassmorphism · neon · bounce 动画 · Inter/Roboto · 所有 section 居中 · HTML 默认样式 · 看起来像 AI 生成的通用模板

---

## 质量检查

**P0(必须全过)**

品牌三色比例 · 无禁忌元素 · 无 HTML 默认样式 · 暖底背景 · 衬线+无衬线混搭 · 响应式 · 每 section 布局不同 · clamp() fluid sizing · 截图发社交媒体不会被说"又是 AI 做的"

**P1(应过)**

至少一个视觉惊喜 section · 字号对比极端 · Scroll Reveal 动效 · 大装饰数字/英文

**P2(加分)**

图片溢出容器 · 深色面板打破节奏 · 装饰元素克制 · prefers-reduced-motion

---

## 怎么用

1. 克隆本仓库
2. 放入你的头像 `assets/avatar.jpg`
3. 把 `assets/template-cards.html` 中的作者名替换成你自己的
4. 把仓库链接发给你的 AI Agent，跟它说：

> 帮我读这个设计系统，以后做页面按这个规范来。

核心不是这些文件本身，是**你的审美判断力**。文件只是把你的判断写成了 AI 能执行的规则。

---

## 继承说明

本仓库 fork 自 [esthersjw/esther-design-system](https://github.com/esthersjw/esther-design-system)，在不二原版基础上将品牌色改为「森林墨（Forest Ink）」暖调知性配色，适配「莉亚学ai」自媒体创作者身份。方法和框架完全继承原版，详见 Credits。

---

## Credits

- 原版设计系统：**ESTHER不二 (esthersjw)** — [esthersjw/esther-design-system](https://github.com/esthersjw/esther-design-system)
- 方法论灵感来源于 [归藏](https://github.com/guizang) 的 PPT Skill——“限制AI的自由度 = 保证输出质量”这个核心思路参考了他的设计
- 品牌色「森林墨（Forest Ink）」配色灵感来源于 [莉亚学ai](https://github.com/erjideshijian) 的「普通人学习AI半年」分享PPT

---

## License

[![CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

本仓库基于 [esthersjw/esther-design-system](https://github.com/esthersjw/esther-design-system) 修改，遵循 CC BY-NC-SA 4.0 协议。

- ✅ 可自由使用、修改、分享
- ✅ **必须署名原作**：ESTHER不二 (esthersjw) + 莉亚学ai (erjideshijian)
- ❌ 禁止商用
- 🔄 修改后必须以相同协议分享
