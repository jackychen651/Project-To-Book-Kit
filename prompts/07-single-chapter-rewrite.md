# 单章重写提示词

```text
请只重写指定章节，让它更像“给初学者读的源码课”，同时保持事实准确。

参数：
- 目标项目路径：{{TARGET_PROJECT_PATH}}
- 输出目录：{{BOOK_OUTPUT_DIR}}
- 章节文件：{{CHAPTER_FILE}}
- 重写目标：{{REWRITE_GOAL}}

先阅读：
- `project-to-book-kit/templates/chapter.template.md`
- `{{BOOK_OUTPUT_DIR}}/meta/project-profile.json`
- `{{BOOK_OUTPUT_DIR}}/meta/book-plan.json`
- `{{CHAPTER_FILE}}`
- 该章引用的源码文件

重写要求：
1. 保留原章节讨论的主题边界，不要发散到整本书。
2. 提升初学者可读性。
3. 增强真实源码锚点。
4. 增加或优化类比、图、小结、练习。
5. 删除空话、重复话、脱离源码的判断。
6. 如果原章节里有不确定信息，要明确标注或修正。
```

