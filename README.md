# Course Learning Assistant · 课程学习助手

一个面向英文课程材料的学习 Skill：用中文讲清知识，持续强化英文术语，并为每个知识模块标注准确的文件名和 PDF 页码或幻灯片编号。

它以理解和应用为目标，通过直觉、推理、例子、反例和常见误区帮助学习，而不是逐页翻译或复述 PPT。

## 适用人群

适用于**母语为中文、需要使用英文学习的大学生和研究生**，包括但不限于：

- 在海外留学、使用英文教材或修读英文授课课程的学生。
- 中外合作办学项目、联合培养项目及国际学院的学生。
- 在国内高校修读英文授课课程、阅读英文课件和学术材料的本科生、硕士生与博士生。

无论是否出国，只要希望借助中文理解专业知识，同时掌握英文术语和课程表达，都可以使用本 Skill。讲解深度应随课程层次、材料难度和学习者基础调整。

## 核心功能

- **中文教学与英文强化**：用清楚的中文解释概念，保留重要英文术语、缩写、公式名称和考试表达，并在后续讲解中持续强化。
- **精确来源引用**：为讲解、例子、公式、图表、总结和练习标注文件与页码；区分课件内容、合理推断和课外补充，无法确认来源时明确说明。
- **理解优先的教学**：解释概念是什么、为什么重要、如何运作、何时适用及与其他知识的联系；遇到理解困难时更换解释方式。
- **图表与公式讲解**：结合材料中的图示、表格和截图解释关系；对公式说明符号、推理步骤、假设、适用条件和常见错误。
- **多种学习模式**：支持预习、详细教学、零基础入门、当前页跟学、复习、考试准备、针对性答疑、费曼检验和考前速记。
- **按需练习与反馈**：在用户要求测试、复习或备考时出题，逐步提示、定位错误原因，并用变式题检查理解。
- **学习进度追踪**：在当前项目或工作区维护 Markdown 进度文档，记录知识点、来源、已学与待学内容、下一步和需要复习的项目；继续学习时复用已有记录。

## 文件结构

```text
course-learning-assistant/
├── SKILL.md                     # 核心教学规则与工作流程
├── agents/
│   └── openai.yaml              # Skill 展示信息与默认提示词
├── references/
│   └── learning-modes.md        # 学习模式与练习反馈规则
└── README.md
```

## 使用方式

将本目录作为完整 Skill 添加到支持 `SKILL.md` 的智能助手环境，保留 `agents/` 和 `references/` 的相对位置。具体加载方式取决于所使用的客户端。

提供 PDF、PPT/PPTX 或具体学习主题后，可以使用下面的请求：

```text
使用 $course-learning-assistant 帮我学习这份英文课件。
请用中文讲解，保留重要英文术语，并标注每个知识模块的文件名和页码。
先建立课程知识点清单，再从第一部分开始。
```

其他示例：

```text
我没有相关基础，请先补充必要的前置知识，再讲第 8–12 页。
```

```text
帮我复习这一章，整理概念区别、常见误区和中英术语表，每一项标注来源。
```

```text
针对刚学的内容出三道题，先不要给答案；我回答后再分析错误。
```

```text
继续上次的学习，读取已有学习进度，跳过例行提问，讲快一点。
```

## 能力边界

这是教学行为与工作流程的指令集。PDF、演示文稿和图像的实际读取能力由运行它的助手及可用工具提供；遇到无法读取的图示或无法确认的页码，应明确说明。

本仓库仅包含通用 Skill 文件和使用说明，不包含个人课件、作业答案或个人学习进度。

## English overview

A course tutoring skill for native Chinese-speaking undergraduate and graduate students who need to study in English, including but not limited to international students and students in Chinese-foreign cooperative education or joint degree programs. It supports learning from English-language PDFs and presentations. It teaches in Chinese while reinforcing English terminology, cites exact source pages or slides for each teaching block, adapts explanations to the learner, supports review and practice, and maintains a reusable learning progress document in the current workspace.
