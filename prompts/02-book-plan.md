# 阶段 2：书籍规划提示词

```text
请基于已有的项目扫描结果，为目标项目设计一本“零基础友好源码书”的完整结构。

参数：
- 目标项目路径：{{TARGET_PROJECT_PATH}}
- 输出目录：{{BOOK_OUTPUT_DIR}}
- 书名：{{BOOK_TITLE}}
- 主要读者：{{TARGET_AUDIENCE}}

先阅读：
- `project-to-book-kit/FRAMEWORK.md`
- `project-to-book-kit/templates/book-plan.template.json`
- `{{BOOK_OUTPUT_DIR}}/meta/project-profile.json`
- `{{BOOK_OUTPUT_DIR}}/meta/project-profile.md`

任务要求：
1. 基于项目规模和复杂度，自适应决定篇数和章节数。
2. 每一篇都要说明：
   - 为什么要有这一篇
   - 这一篇解决读者的什么问题
   - 难度等级
3. 每一章都要定义：
   - 标题
   - 教学问题
   - 对应关键文件
   - 前置知识
4. 生成 `{{BOOK_OUTPUT_DIR}}/meta/book-plan.json`。
5. 书籍规划必须遵循“先大图景，再主流程，再模块深挖，最后亮点/扩展”的顺序。
6. 不要按源码目录机械平铺；要把多个零散目录组织成读者能理解的叙事。

输出标准：
- `book-plan.json` 结构严格参考模板文件。
- 章节命名要稳定、可排序、易读。
- 如果项目太小，就减少篇数和章节数，不要硬凑。
```

