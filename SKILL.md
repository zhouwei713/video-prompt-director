---
name: video-prompt-director
description: Use when the user wants to turn a one-line video idea, rough brief, link, document, product description, feature list, or research material into a precise, source-grounded video generation prompt for HyperFrames or other video tools. The skill extracts key facts, product functions, commands, UI text, evidence, and visualizable details from provided or researched sources, then produces a controlled 30-second video prompt with shots, narration, screen text, motion, style, and constraints.
---

# Video Prompt Director

## Purpose

Turn a short idea into a high-control video generation prompt. The output must be ready to copy into HyperFrames or another video generation workflow, with clear duration, format, scenes, screen text, visual actions, motion, narration, and source-grounded details.

Default video length is 30 seconds unless the user requests another duration or the platform clearly implies a different length.

## Core Workflow

1. Identify the request type.
   Product demo, tool introduction, teaching short, social short, historical explainer, concept explainer, brand intro, event recap, or pitch video.

2. Gather source material.
   Use user-provided text first. If the user gives links, asks to research, or asks for current facts, inspect sources before writing. Prefer official websites, product docs, GitHub repositories, release notes, English documentation, academic or primary sources. Avoid Chinese websites unless the user supplied them or explicitly requested them.

3. Extract video-worthy facts.
   Pull the product name, core promise, top functions, commands, UI labels, workflow steps, outputs, audience, differentiators, numbers, limitations, and visual assets. See `references/source-extraction.md` when sources are involved.

4. Convert facts into scenes.
   Every important fact must become at least one visible item: screen text, typed input, UI chip, card, timeline marker, graph, icon, comparison row, cursor action, or narration line.

5. Write the controlled prompt.
   Use the output contract below. Keep it in Chinese when the user writes in Chinese. Include only facts that are grounded in provided or researched material. If a useful detail is inferred, label it as a creative assumption.

6. Check the prompt.
   Confirm the prompt has a clear goal, 4 to 6 scenes for 30 seconds, exact screen text, motion instructions, style constraints, audio guidance, and negative constraints.

## Output Contract

Return one copy-ready video prompt with these sections:

### 视频类型

Choose the best type and name it plainly.

### 时长与画幅

Default: 30 秒，16:9 横屏。 Adjust only if the user asks or the distribution channel implies it.

### 核心目标

One sentence: what the viewer should understand, remember, or do after watching.

### 资料提取摘要

List the facts that will be used in the video. Include commands, feature names, UI labels, data points, and outputs. If no source was available, list assumptions under `创意假设`.

### 叙事主线

One sentence describing the flow from opening to closing.

### 分镜提示词

Write 4 to 6 scenes. Each scene should include:

1. 时间段
2. 画面
3. 屏幕文字
4. 动作与镜头
5. 旁白
6. 转场

### 关键屏幕文字

List every exact phrase that must appear on screen. Preserve commands and product terms exactly. For command-like text, mark tags and regular input separately.

### 动效与镜头控制

Describe UI actions, typing, clicks, generation state, zooms, transitions, camera movement, progress, and object motion.

### 风格要求

Set visual tone, surface design, realism level, color direction, typography, and density.

### 禁止项

Include constraints that prevent drift: no unsupported claims, no overdone effects, no clutter, no tiny text, no fake UI if a real UI is required, no arbitrary feature invention.

### 最终可复制提示词

Provide a single consolidated prompt that can be pasted into a video generation agent.

## Defaults

1. Duration: 30 seconds.
2. Scenes: 5 scenes for most topics.
3. Opening: Show the central object or result within the first 3 seconds.
4. Ending: Repeat the product, topic, or key takeaway with one concise line.
5. Style: Clean, premium, controlled motion. For product and UI videos, use realistic interface behavior. For history and education, use timelines, maps, documents, diagrams, and labels.
6. Audio: Include concise narration and optional captions. Captions should match the narration.

## Source Handling

Use `references/source-extraction.md` when the prompt depends on provided material, links, documents, or web research.

Use `references/prompt-patterns.md` when selecting scene patterns or adapting the example prompt structure.

## Quality Bar

A good output should make the video feel directed, not merely described. It should say what appears, what moves, what text is typed or displayed, what the viewer hears, and what the model must avoid. The prompt must preserve grounded details such as `/鲸格skills 制作ppt` when they are central to the story.
