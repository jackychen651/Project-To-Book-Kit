# 一次性总控提示词

把下面内容作为你给 Codex 的任务说明使用：

```text
请阅读目标项目，并严格遵循 `project-to-book-kit/FRAMEWORK.md`、`project-to-book-kit/WORKFLOW.md` 以及 `project-to-book-kit/templates/` 下的模板，
为该项目生成一套“零基础也能读懂”的 Markdown 书稿。

参数如下：
- 目标项目路径：{{TARGET_PROJECT_PATH}}
- 输出目录：{{BOOK_OUTPUT_DIR}}
- 书名：{{BOOK_TITLE}}
- 输出语言：中文
- 主要读者：{{TARGET_AUDIENCE}}

执行要求：
1. 先阅读 `project-to-book-kit/README.md`、`FRAMEWORK.md`、`WORKFLOW.md` 和 `templates/`。
2. 先做项目扫描，再做书籍规划，不要上来直接写章节。
3. 在 `{{BOOK_OUTPUT_DIR}}/meta/` 中生成：
   - `project-profile.json`
   - `book-plan.json`
4. 在 `{{BOOK_OUTPUT_DIR}}/docs/` 中生成完整书稿，至少包含：
   - `README.md`
   - `_sidebar.md`
   - `_coverpage.md`
   - `part00-preface/README.md`
   - `part00-preface/roadmap.md`
   - `part00-preface/glossary.md`
   - 若干 `partNN-*/**.md` 章节
   - `appendix/source-index.md`
   - `appendix/further-reading.md`
5. 书的篇数和章节数必须根据项目规模自适应，不要强行套用固定 12 篇结构。
6. 章节必须按“读者理解顺序”组织，不要按源码目录顺序堆砌。
7. 每章都要尽量包含：
   - 学习目标
   - 生活类比
   - 回到真实源码
   - 关键文件路径
   - Mermaid 图
   - 小结
   - 动手练习
8. 任何结论都要尽量锚定到真实文件、目录、函数、类型或配置。
9. 不确定的地方必须明确写“待确认”或“估算”，不要脑补。
10. 生成完成后，再做一次整书一致性检查，修复明显的术语不统一、坏链接、重复内容和过难表达。

写作风格要求：
- 面向初学者，但不要幼稚化
- 中文解释 + 英文代码标识符
- 优先解释“这个东西为什么存在”
- 类比只是桥梁，最终必须回到源码
- 不写空泛鸡汤

如果项目很大，请自动采用分批生成策略，但最终把文件持续写入 `{{BOOK_OUTPUT_DIR}}`，不要只停留在计划层。
```

