# Video Prompt Director

把一句视频想法、产品简介、链接资料或研究主题，转成更有控制力的视频生成提示词。

This Codex skill turns a short video idea, product brief, source link, or research topic into a controlled video generation prompt.

## 中文说明

### 适合场景

1. 产品功能演示
2. 工具介绍
3. 教学短片
4. 社媒短视频
5. 历史或商业解读
6. 基于资料的视频脚本扩写

### 核心能力

1. 默认生成 30 秒视频提示词。
2. 支持从用户给定资料中提取重点信息。
3. 支持在需要时自行查找资料，并优先使用官方文档、英文资料、GitHub 仓库、论文、新闻源和其他权威来源。
4. 会把重点功能、命令、产品卖点、数据点、界面文字和视觉钩子转成视频文案。
5. 输出包含分镜、屏幕文字、旁白、镜头动作、动效控制、风格要求和禁止项。
6. 适合继续交给 HyperFrames 或其他视频生成工具执行。

### 使用示例

```text
$video-prompt-director 介绍一个能自动生成 PPT 和视频的工具
```

```text
$video-prompt-director 根据这个链接，为一个 GitHub 开源项目制作 30 秒介绍视频提示词：https://github.com/heygen-com/hyperframes
```

```text
$video-prompt-director 介绍一下豆包 APP 如果收费，对于国内大模型市场的影响
```

### 输出内容

1. 视频类型
2. 时长与画幅
3. 核心目标
4. 资料提取摘要
5. 叙事主线
6. 分镜提示词
7. 关键屏幕文字
8. 动效与镜头控制
9. 风格要求
10. 禁止项
11. 最终可复制提示词

### 资料处理原则

1. 优先使用用户提供的资料。
2. 如果用户提供链接或要求研究，会先提取来源中的关键事实。
3. 对产品类内容，重点提取产品名称、核心功能、用户动作、输出结果、差异化卖点和界面文字。
4. 对历史、商业和市场内容，重点提取时间、主体、事件、数据、因果关系和可视化线索。
5. 对不确定内容，会标记为创意假设，避免写成确定事实。

## English

### What It Does

Video Prompt Director converts a brief idea into a structured, source grounded video generation prompt. It is designed for Codex workflows that need a stronger prompt before creating videos with HyperFrames or another video tool.

### Best For

1. Product demos
2. Tool introductions
3. Teaching shorts
4. Social videos
5. Historical explainers
6. Market analysis videos
7. Source based video scripts

### Main Features

1. Uses 30 seconds as the default duration.
2. Extracts key facts from user provided materials.
3. Researches sources when needed, with preference for official docs, English language sources, GitHub repositories, papers, reputable news, and primary sources.
4. Converts functions, commands, product benefits, data points, UI labels, and visual hooks into video copy.
5. Produces scene by scene prompts with narration, screen text, motion direction, camera control, style rules, and negative constraints.
6. Works well as a prompt preparation step before HyperFrames video production.

### Example Prompts

```text
$video-prompt-director Create a 30 second prompt for a tool that can automatically generate slides and videos.
```

```text
$video-prompt-director Turn this GitHub repo into a product intro video prompt: https://github.com/heygen-com/hyperframes
```

```text
$video-prompt-director Explain how paid access for a leading AI app could affect the China large model market.
```

### Output Sections

1. Video type
2. Duration and aspect ratio
3. Core objective
4. Source extraction summary
5. Narrative through line
6. Scene prompts
7. Required screen text
8. Motion and camera control
9. Style requirements
10. Negative constraints
11. Final copy ready prompt

### File Structure

```text
video-prompt-director/
  SKILL.md
  README.md
  agents/
    openai.yaml
  references/
    prompt-patterns.md
    source-extraction.md
```

### Installation

Copy this folder into your Codex skills directory:

```text
$CODEX_HOME/skills/video-prompt-director
```

Then invoke it in Codex with:

```text
$video-prompt-director your video idea here
```

### Design Notes

This skill focuses on direction quality. A good output should clearly define what appears on screen, what moves, what text is shown, what the viewer hears, what facts are grounded in sources, and what the video generator must avoid.
