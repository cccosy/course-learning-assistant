# Course Learning Assistant · 课程学习助手

**用中文理解专业知识，用英文连接课程学习。**

**Understand your subject in Chinese. Build confidence studying in English.**

一个面向英文课程材料的学习 Skill：以中文讲清概念，持续强化英文术语，并为每个知识模块标注准确的文件名与 PDF 页码或幻灯片编号。通过直觉、推理、例子和常见误区帮助学习者理解与应用知识。

A tutoring skill for English-language course materials. It explains concepts in Chinese, reinforces English terminology throughout each lesson, and cites the exact file and PDF pages or slides for each teaching block. It builds understanding through intuition, reasoning, examples, and common misconceptions.

---

## 适用人群 · Who this is for

适用于**母语为中文、需要使用英文学习的大学生和研究生**，涵盖本科、硕士和博士阶段，包括但不限于：

For **native Chinese-speaking students who study in English**, at undergraduate, master's, and doctoral levels. This includes, but is not limited to:

- **海外留学生**：使用英文教材、课件或修读英文授课课程。  
  **International students** studying with English-language textbooks, slides, or courses.
- **中外合作办学及联合培养项目学生**：包括国际学院及其他双语、英文授课项目。  
  **Students in Chinese-foreign cooperative education and joint degree programs**, including international colleges and other bilingual or English-medium programs.
- **国内高校学生**：需要阅读英文课程资料或学术材料的本科生与研究生。  
  **Undergraduate and graduate students at domestic universities** who work with English-language course or academic materials.

无论是否出国，只要希望借助中文理解专业知识，同时掌握英文术语和课程表达，都可以使用。讲解深度会随课程层次、材料难度和学习者基础调整。

You do not need to be studying abroad. The skill supports learners who want to understand their subject in Chinese while developing familiarity with English terminology and course language. Teaching depth adapts to the course level, source material, and learner's background.

## 核心功能 · Key features

### 中文讲解与英文强化 · Chinese explanations, English reinforcement

用清楚的中文解释概念，并在首次及后续重要讲解中持续保留英文术语、缩写、公式名称和考试表达，帮助理解知识与阅读英文材料相互衔接。

Explains concepts in clear Chinese and repeatedly reinforces English terms, abbreviations, formula names, and useful exam language, connecting subject understanding with the ability to read English course materials.

### 精确来源引用 · Precise source citations

为讲解、例子、公式、图表、总结和练习标注文件与页码；区分材料明确内容、合理推断及课外补充。无法确认来源或读取图示时明确说明。

Cites the file and pages or slides for explanations, examples, formulas, visuals, summaries, and exercises. Distinguishes explicit source content from reasonable inferences and supplementary material, and flags unconfirmed locations or unreadable visuals.

### 理解优先的教学 · Understanding through reasoning

解释概念是什么、为什么重要、如何运作、何时适用，以及与其他知识的联系。结合例子、反例和常见误区；学习者仍有困难时，更换解释方式。

Explains what a concept means, why it matters, how it works, when it applies, and how it connects to related ideas. Uses examples, counterexamples, and common misconceptions, and changes the explanation when the learner needs another approach.

### 图表与公式讲解 · Visual and formula walkthroughs

结合材料中的图示、表格和截图解释关系；对公式说明符号、推理步骤、假设、适用条件和常见错误。

Walks through diagrams, tables, and screenshots from the source material. Explains formula notation, reasoning steps, assumptions, conditions of use, and common errors.

### 多种学习模式 · Flexible learning modes

支持预习、详细教学、零基础入门、当前页跟学、复习、考试准备、针对性答疑、费曼检验和考前速记。

Supports previews, detailed lessons, beginner explanations, page-focused study, review, exam preparation, targeted questions, Feynman checks, and concise revision notes.

### 按需练习与反馈 · Practice and feedback on request

在用户要求测试、复习或备考时出题，逐步提示、定位错误原因，并用变式题检查理解。每道题及其解析都标注适用来源。

Creates exercises when the learner requests testing, review, or exam preparation. Offers graduated hints, diagnoses mistakes, and checks understanding with a related question. Questions and answer explanations include applicable source citations.

### 学习进度追踪 · Learning progress tracking

在当前项目或工作区维护 Markdown 进度文档，记录知识点、来源、已学与待学内容、下一步和复习项目。继续学习时复用已有记录。

Maintains a Markdown progress document in the current project or workspace, recording topics, source locations, completed and pending learning, next steps, and review items. Reuses the existing document when learning resumes.

## 文件结构 · Repository structure

```text
course-learning-assistant/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   └── learning-modes.md
└── README.md
```

- [SKILL.md](SKILL.md)：核心教学规则与工作流程。  
  Core teaching instructions and workflow.
- [agents/openai.yaml](agents/openai.yaml)：Skill 展示信息与默认提示词。  
  Skill display metadata and default prompt.
- [references/learning-modes.md](references/learning-modes.md)：学习模式与练习反馈规则。  
  Learning modes and practice feedback guidance.

## 使用方式 · Getting started

将本目录作为完整 Skill 添加到支持 `SKILL.md` 的智能助手环境，保留 `agents/` 和 `references/` 的相对位置。具体加载方式取决于所使用的客户端。

Add this directory as a complete skill in an assistant environment that supports `SKILL.md`. Keep `agents/` and `references/` in their relative locations. The loading procedure depends on your client.

提供 PDF、PPT/PPTX 或具体学习主题后，可以选择中文或英文提示词启动。以下两种写法表达相同的学习目标。

Provide a PDF, PPT/PPTX, or a specific topic, then start with a Chinese or English prompt. Both versions below express the same learning goal.

### 开始学习 · Start a lesson

**中文提示词 · Chinese prompt**

```text
使用 $course-learning-assistant 帮我学习这份英文课件。
请用中文讲解，保留重要英文术语，并标注每个知识模块的文件名和页码。
先建立课程知识点清单，再从第一部分开始。
```

**英文提示词 · English prompt**

```text
Use $course-learning-assistant to help me study these English course materials.
Explain in Chinese, retain key English terms, and cite the file and pages or slides for each teaching block.
Create a course topic checklist, then begin with the first section.
```

### 其他请求示例 · More example requests

**补充基础 · Build prerequisites**

> 我没有相关基础，请先补充必要的前置知识，再讲第 8–12 页。

> I am new to this subject. Explain the necessary prerequisites before teaching pages 8–12.

**复习整理 · Review a chapter**

> 帮我复习这一章，整理概念区别、常见误区和中英术语表，每一项标注来源。

> Help me review this chapter. Summarize key distinctions and common misconceptions, and create a Chinese–English glossary. Cite the source for each item.

**练习反馈 · Practice with feedback**

> 针对刚学的内容出三道题，先不要给答案；我回答后再分析错误。

> Give me three questions about what we just learned. Withhold the answers until I respond, then explain any mistakes.

**继续学习 · Resume learning**

> 继续上次的学习，读取已有学习进度，跳过例行提问，讲快一点。

> Resume from my existing progress document. Skip routine comprehension checks and teach at a faster pace.

## 能力边界 · Scope and limitations

这是教学行为与工作流程的指令集。PDF、演示文稿和图像的实际读取能力由运行它的助手及可用工具提供；遇到无法读取的图示或无法确认的页码，应明确说明。

This skill defines teaching behavior and workflow. Reading PDFs, presentations, and images depends on the host assistant and its available tools. Unreadable visuals and unconfirmed page locations should be stated explicitly.

本仓库仅包含通用 Skill 文件和使用说明，不包含个人课件、作业答案或个人学习进度。

This repository contains reusable skill files and usage instructions. It does not include personal course materials, assignment answers, or individual learning records.
