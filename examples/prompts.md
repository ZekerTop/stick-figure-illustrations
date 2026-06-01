# Prompt 示例

把这些提示词复制到 Codex 里，再替换占位内容。示例只保留用户需要提供的内容和目标；画幅、视觉风格、火柴人情绪、标注密度和质量检查由 skill 默认处理。

## 最佳起手式

```text
Use $stick-figure-illustrations 阅读下面内容，先不要生图。

<粘贴内容>
```

## 生成观点图

```text
Use $stick-figure-illustrations 为这个观点生成一张图：

“好的工具会把混乱收起来，把下一步摆到你面前。”
```

默认就是有表现力的观点图，不需要在提示词里额外写“有表现力”。

## 文章配图

```text
Use $stick-figure-illustrations 阅读下面文章，先不要生图。

<粘贴文章>
```

## 文章观感优化 + 直接生成插图

```text
Use $stick-figure-illustrations 为下面文章找适合插图的位置，并直接生成能改善阅读观感的图片。

<粘贴文章>
```

## 社媒轮播

```text
Use $stick-figure-illustrations 用 carousel preset 把这个主题设计成社媒轮播，先不要生图。

主题：一个人如何把 AI 变成日常工作流
```

## PPT / Keynote

```text
Use $stick-figure-illustrations 用 slides preset 为这个演讲大纲规划插图。

用途：
- 章节过渡页
- 关键观点旁图
- 结尾行动页

<粘贴大纲>
```

## SaaS 空状态

```text
Use $stick-figure-illustrations 用 saas-state preset 生成空状态插图：

状态：用户还没有创建任何项目。
```

## 开源 README

```text
Use $stick-figure-illustrations 用 readme preset 为这个开源项目 README 规划插图。

场景：
1. 安装
2. 配置
3. 提交 issue
4. 发起 PR
```

## 教程 / 课程

```text
Use $stick-figure-illustrations 用 course preset 处理下面教程，先输出规划，然后生成第 1 张。

<粘贴教程>
```

## 复杂概念

```text
Use $stick-figure-illustrations 为这个概念生成一张图：

“信任不是说服出来的，而是证据一块一块铺出来的。”
```

## 功能发布

```text
Use $stick-figure-illustrations 为这个功能发布规划 3 张方案，先不要生图。

功能：自动把会议录音整理成任务清单。
```

## 改图 / 重画

```text
Use $stick-figure-illustrations 这张图方向对，但太像流程图。
请重生成一版：

- 保留核心意思
- 改成自然场景
- 删除大标题和多余节点
```
