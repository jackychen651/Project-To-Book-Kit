# 阶段 5：导航与附录提示词

```text
请为已经生成的书稿补齐导航和附录文件。

参数：
- 输出目录：{{BOOK_OUTPUT_DIR}}
- 书名：{{BOOK_TITLE}}

先阅读：
- `{{BOOK_OUTPUT_DIR}}/meta/book-plan.json`
- 已生成的 `docs/` 章节文件
- `project-to-book-kit/templates/docs-readme.template.md`
- `project-to-book-kit/templates/sidebar.template.md`
- `project-to-book-kit/templates/source-index.template.md`
- `project-to-book-kit/templates/coverpage.template.md`
- `project-to-book-kit/templates/further-reading.template.md`

任务要求：
1. 生成或更新：
   - `docs/README.md`
   - `docs/_sidebar.md`
   - `docs/_coverpage.md`
   - `docs/appendix/source-index.md`
   - `docs/appendix/further-reading.md`
2. `README.md` 要有全书概览、快速导航、推荐入口。
3. `_sidebar.md` 要和真实文件完全一致，不能挂死链接。
4. `source-index.md` 要把关键源码文件按模块分类，并映射到相关章节。
5. `further-reading.md` 要区分：
   - 项目官方文档
   - 值得对照阅读的核心源码
   - 相关框架/协议/标准
```

