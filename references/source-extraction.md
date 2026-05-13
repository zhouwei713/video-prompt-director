# Source Extraction

Use this reference when the user provides materials, links, files, product descriptions, or asks the agent to find information before writing a video prompt.

## Priority Order

1. User-provided material.
2. Official product website, docs, help center, GitHub repo, changelog, release notes.
3. Primary or authoritative sources for non-product topics.
4. English-language reputable sources for background context.

Avoid Chinese websites unless the user directly provides them or explicitly asks to use them.

## Extract These Items

1. Name
   Product, topic, feature, person, event, or organization.

2. One-line definition
   What it is in plain language.

3. Core functions or claims
   The top 3 to 6 capabilities that the video should show.

4. User action
   Commands, prompts, clicks, uploads, selections, typed input, API calls, or setup steps.

5. Output
   What the tool or process creates: PPT, video, report, chart, dashboard, lesson, plan, artifact.

6. Differentiator
   Why this matters compared with a generic workflow.

7. Evidence
   Numbers, dates, versions, status, license, supported platforms, source quotes, or documented behavior.

8. Visual hooks
   UI surfaces, icons, documents, maps, cards, timelines, screenshots, graphs, before-and-after states.

9. Screen text
   Exact words that must appear in the video.

10. Constraints
   What cannot be claimed, shown, or implied.

## Convert Information Into Video Content

For each extracted item, decide how it appears:

1. Product function becomes a typed command, feature chip, UI card, generated artifact, or narration sentence.
2. A workflow step becomes cursor movement, click, upload, progress state, or timeline marker.
3. A number becomes a large stat, badge, counter, or comparison row.
4. A document becomes a paper panel, page preview, highlighted sentence, or source card.
5. A historical event becomes a date marker, map, document, symbol, or motion path.

## Handling Weak Sources

If a source is incomplete, do not invent specifics. Use `创意假设` for plausible staging choices and keep factual claims conservative.

If a claim is uncertain, phrase it as a direction for the video, not as a fact.

If the user wants a real product interface, preserve real UI labels and avoid imaginary controls unless they are clearly marked as stylized.

## Minimum Source Summary

Before writing the final prompt, create a compact extraction summary:

1. 主题
2. 目标观众
3. 关键事实
4. 必须出现的屏幕文字
5. 可视化素材
6. 不应声称的内容

This summary should feed the final video prompt directly.
