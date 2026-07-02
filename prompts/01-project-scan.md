# 阶段 1：项目扫描提示词

```text
请先不要写书稿，先对目标项目做“教学型拆解”的项目扫描。

参数：
- 目标项目路径：{{TARGET_PROJECT_PATH}}
- 输出目录：{{BOOK_OUTPUT_DIR}}
- 输出语言：中文

先阅读：
- `project-to-book-kit/FRAMEWORK.md`
- `project-to-book-kit/WORKFLOW.md`
- `project-to-book-kit/templates/project-profile.template.json`

任务要求：
1. 阅读目标项目的目录、README、入口文件、关键配置和核心源码。
2. 识别：
   - 项目类型
   - 主要语言与框架
   - 运行方式
   - 入口文件
   - 核心目录
   - 主流程
   - 高教学价值模块
   - 低优先级目录
3. 估算项目规模，并判断适合生成多大的书。
4. 在 `{{BOOK_OUTPUT_DIR}}/meta/` 下生成：
   - `project-profile.json`
   - `project-profile.md`
5. `project-profile.json` 的结构严格参考模板文件。
6. `project-profile.md` 要用人能读懂的方式概括扫描结论，并给出建议的篇章方向。

约束：
- 不要急着生成章节文件。
- 不要把猜测写成事实。
- 如果缺少运行环境或部分信息难以确认，就明确写“待确认”。
```

