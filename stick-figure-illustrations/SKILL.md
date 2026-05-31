---
name: stick-figure-illustrations
description: |
  Turn creator content into emotionally expressive neutral stick-figure sketch illustrations for
  articles, newsletters, social carousels, slides, product docs, tutorials, courses, open-source
  explainers, SaaS empty states, feature visuals, shot lists, image prompts, and visual-system
  extensions. Default to simple line-body stick figures with readable emotion, one brandable accent
  color, and no mascot identity, recognizable character IP, or imitation of specific third-party styles.
---

# Stick Figure Illustrations

## 核心定位

把创作者内容里的观点、流程、状态、对比和隐喻，转成清晰、轻量、可复用的火柴人草图解释插画。

这不是某个角色 IP，也不是个人作者风格复刻。默认人物必须是匿名火柴人：圆头、线条身体、简单四肢、无品牌身份、无固定名字，但不能是无表情站桩。默认要用极简眉眼、嘴线、头部倾斜、手势和身体姿态传达情绪。除非用户明确要求“不要人物”“只要图标”“只要抽象图形”，否则生成图里应该以火柴人为主要视觉主体。

文章配图的目标是提升阅读观感、节奏和理解，不是把图堆进文章。只有当插图能让读者停顿、看懂、记住或缓解长文疲劳时才建议加入；如果没有合适位置，应该明确建议少配或不配。

## 硬性边界

- 不出现特定作者名、特定案例名或任何外部参考措辞。
- 不画固定吉祥物、高识别度角色、块状填充人物或表情包角色。
- 不要求固定多色批注系统。默认只用黑色线稿加 1 个点缀色。
- 不复刻任何已知创作者、插画师、品牌、IP 或公开示例的构图与语气。
- 不把图做成复杂 PPT 信息图、正式架构图、海报 KV、儿童卡通或商业矢量插画。

## 先读这些参考

按任务需要读取，不要一次塞满上下文：

- `references/visual-system.md`：火柴人视觉规范、色彩、文字和禁忌。
- `references/use-cases.md`：不同创作者场景的输出建议。
- `references/presets.md`：按 article、carousel、slides、docs、course、README、SaaS 等场景快速选择画幅、密度和交付形式。
- `references/shot-list-schema.md`：shot list 的固定输出结构、优先级和质量门槛。
- `references/scene-patterns.md`：构图模式、隐喻生成方法和避重规则。
- `references/prompt-template.md`：单张生图与改图提示词模板。
- `references/qa-checklist.md`：生成后检查和迭代规则。

## 工作流

### 1. 读内容，找视觉锚点

先读用户给的文章、Markdown、文档、截图、主题或链接内容。提炼：

- 核心观点
- 读者卡住的地方
- 能改善阅读观感和节奏的停顿点
- 适合被画出来的动作、状态、对比或路径
- 不适合配图、只适合文字解释的部分

不要平均配图。优先选真正帮助理解或传播的视觉锚点：关键判断、前后对比、步骤转换、输入输出、常见错误、决策分岔、角色困境、成果展示。

### 2. 先出 shot list

除非用户明确说“直接生成 / 现在生图 / 不要规划”，否则先输出 shot list。每张图写清楚：

- 放置位置或使用渠道
- 画幅
- 图的主题
- 核心意思
- 场景类型
- 火柴人在做什么
- 火柴人是什么情绪
- 主要元素
- 建议短标注
- 优先级

默认 3-6 张候选。短内容可以 0-2 张；长文或课程可扩到 8-10 张，但必须说明每张的用途。不要为了凑数量而推荐装饰图。

shot list 格式优先使用 `references/shot-list-schema.md`。如果用户指定场景模式，先读取 `references/presets.md` 再规划。

每次输出 shot list 后，必须追加 `下一步` 区块，告诉用户现在可以直接回复什么。不要让输出停在表格。至少给出：

- 推荐先生成哪一张，以及一句原因。
- 可直接复制的回复命令，例如 `生成 #1`、`生成 #1 和 #2`、`调整 #1：不要文字，用蓝色点缀色`、`先不生成，重新检查插图位置`。
- 如果不建议加图，给出 `不生成，保持文章原样` 或 `重新检查另一版文章` 这类下一步。

### 3. 单张生成

如果用户明确要求“生成 / 输出 / 做图 / 直接画”，直接为每张图单独调用图像生成工具。不要把多张图拼在一张里，除非用户要求轮播总览或分镜板。

每张图只表达一个核心意思。提示词必须包含：

- 目标渠道和画幅
- 有情绪的中性火柴人角色，且默认作为画面主体
- 用极简表情和姿态把情绪读清楚
- 简洁黑色线稿
- 一个可替换的品牌点缀色
- 大量留白
- 少量短标注，或完全无文字版本
- 禁止第三方 IP、固定角色、特定作者风格、复杂 PPT 感

### 4. 文章观感优化配图

如果用户要求“给文章找插图位置并同时生成图片 / 一键配图 / 直接给插入位置和图片”，目标是让文章观感更好，而不是塞满插图。不要停在 shot list。先快速完成视觉锚点和阅读节奏筛选，再为 `P0` 和明确能改善阅读体验的 `P1` 图片逐张生成。如果没有合适位置，明确说不建议强行加图。

每张图交付时必须包含：

- 具体插入位置：章节名，或插在某段/某句之后。
- 生成后的图片展示；如果当前环境不能生图，改为给出可直接用于生图的完整提示词，并明确说明未生成。
- Markdown 插入代码，例如 `![图片说明](./assets/article-slug-illustrations/01-topic.png)`。
- 一句话说明这张图如何改善阅读观感、节奏或理解。

### 5. 按场景调整

根据用户目标选择输出形态：

- 文章/Newsletter：正文解释图，信息密度低，帮助读者停顿理解。
- 社媒轮播：每页一个动作或对比，文字更短，主体更大。
- PPT/Keynote：可作为章节过渡、观点旁图、轻量流程图，避免喧宾夺主。
- 产品文档：强调状态、路径、错误恢复和用户任务。
- 教程/课程：一步一图，动作明确，可复用同一人物比例。
- 开源项目：突出安装、贡献、issue、release、维护者协作。
- SaaS 界面：空状态、错误页、成功页、加载页、权限页、导入页。

更多场景见 `references/use-cases.md`。

### 6. 检查与迭代

生成后读取 `references/qa-checklist.md`。如果出现以下问题，重生成或局部编辑：

- 人物像某个固定 IP 或吉祥物
- 画面太像 PPT 模板
- 文字太多
- 元素太满
- 点缀色超过一个主色
- 火柴人只是装饰，没有承担动作
- 火柴人没有可读情绪，像无表情占位符
- 可被看出在模仿某个现成风格

### 7. 保存交付

如果用户在 workspace 内工作，把最终图保存到：

```text
assets/<project-or-article-slug>-illustrations/
```

按顺序命名：

```text
01-topic-name.png
02-topic-name.png
```

不要覆盖已有资产，除非用户明确要求替换。

## 输出口径

策略输出要短、可执行。生成后的交付包含：

- 生成了几张
- 每张图适合放在哪里
- 每张图的 Markdown 插入代码
- 保存路径
- 是否有需要重画或删字的图

只输出规划时，也必须包含下一步操作提示，避免用户不知道接下来该如何生成或调整。

不要讲风格理论。创作者要的是能马上用的图。
