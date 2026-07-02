# 阶段 4：正文批量生成提示词

```text
请根据已有的书籍规划，批量生成一部分正文章节。

参数：
- 目标项目路径：{{TARGET_PROJECT_PATH}}
- 输出目录：{{BOOK_OUTPUT_DIR}}
- 本次生成范围：{{PART_OR_CHAPTER_RANGE}}

先阅读：
- `{{BOOK_OUTPUT_DIR}}/meta/project-profile.json`
- `{{BOOK_OUTPUT_DIR}}/meta/book-plan.json`
- `project-to-book-kit/FRAMEWORK.md`
- `project-to-book-kit/templates/chapter.template.md`

任务要求：
1. 只生成本次范围内的章节，不要重写整本书。
2. 每章都要尽量包含：
   - 学习目标
   - 生活类比
   - 回到项目本身
   - 关键源码片段说明
   - Mermaid 图
   - 小结
   - 动手练习
3. 章节内容必须锚定到真实源码文件。
4. 讲解顺序要优先帮助初学者建立理解，不要一上来钻最深的实现细节。
5. 如果某章依赖前文知识，要明确写出前置概念。
6. 生成后同步更新：
   - 需要新增的 `partNN-*` 目录
   - 本批次涉及的文件链接

约束：
- 不要为了“显得专业”而堆术语。
- 不要用大段源码代替解释。
- 不要把类比写成正文主体，类比之后必须回到真实代码。
```

