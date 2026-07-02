# 阶段 3：前言包提示词

```text
请根据已经生成的书籍规划，为目标项目生成前言包。

参数：
- 输出目录：{{BOOK_OUTPUT_DIR}}
- 书名：{{BOOK_TITLE}}

先阅读：
- `{{BOOK_OUTPUT_DIR}}/meta/project-profile.json`
- `{{BOOK_OUTPUT_DIR}}/meta/book-plan.json`
- `project-to-book-kit/templates/preface.template.md`
- `project-to-book-kit/templates/roadmap.template.md`
- `project-to-book-kit/templates/glossary.template.md`

任务要求：
1. 生成 `docs/part00-preface/README.md`
2. 生成 `docs/part00-preface/roadmap.md`
3. 生成 `docs/part00-preface/glossary.md`
4. 前言要告诉读者：
   - 这本书是什么
   - 谁适合读
   - 整体结构
   - 怎么使用
5. 路线图要至少给出 3 种读者路径：
   - 零基础新手
   - 有开发经验的人
   - 对该项目所在领域感兴趣的人
6. 术语表优先收录：
   - 项目专属术语
   - 书里高频出现的工程术语
   - 初学者最容易卡住的缩写

约束：
- 用中文解释术语。
- 保留英文标识符和缩写原文。
- 不要写成营销文案。
```

