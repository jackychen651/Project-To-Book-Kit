# Project To Book Kit

你是否想短期理解别人写的项目，抑或是想读一读网上开源的大型项目？你或许会考虑使用该工具包。

这个工具包把任意代码项目整理成一套“零基础也能读懂”的源码书。

目标不是生成一份普通技术文档，而是生成一套有教学节奏的 Markdown 书稿：

- 先帮读者建立全局地图
- 再按主题拆解源码
- 每章用类比、图、代码锚点、练习来降低理解门槛
- 最终产出一套可继续维护的 `docs/` 目录

## 核心结论

从样例项目可以提炼出 4 个关键模式：

1. 它写的是“教学型源码书”，不是 API 手册。
2. 它按“读者理解顺序”组织内容，而不是照着源码目录硬翻译。
3. 它每章都遵守固定节奏：学习目标、类比、源码解析、图、练习、小结。
4. 它有完整的书籍配套：导读、路线图、术语表、侧边栏、源码索引。

这个工具包就是把这 4 点做成可直接复用的模板。

## 目录说明

```text
project-to-book-kit/
├─ README.md
├─ FRAMEWORK.md
├─ WORKFLOW.md
├─ prompts/
│  ├─ 00-master-orchestrator.md
│  ├─ 01-project-scan.md
│  ├─ 02-book-plan.md
│  ├─ 03-preface-pack.md
│  ├─ 04-chapter-batch.md
│  ├─ 05-navigation-and-appendix.md
│  ├─ 06-quality-pass.md
│  └─ 07-single-chapter-rewrite.md
└─ templates/
   ├─ project-profile.template.json
   ├─ book-plan.template.json
   ├─ chapter.template.md
   ├─ preface.template.md
   ├─ roadmap.template.md
   ├─ glossary.template.md
   ├─ source-index.template.md
   ├─ docs-readme.template.md
   ├─ sidebar.template.md
   ├─ coverpage.template.md
   └─ further-reading.template.md
```

## 推荐用法

### 用法一：整本生成

适合中小型项目，直接使用：

- [prompts/00-master-orchestrator.md](./prompts/00-master-orchestrator.md)

这个提示词会要求 Codex：

- 阅读目标项目
- 先做项目画像
- 再生成书籍大纲
- 再按模板落地 `meta/` 和 `docs/` 文件
- 最后做一致性检查

### 用法二：分阶段生成

适合大型项目、单仓多包项目、你希望人工插手调整时。

按顺序使用：

1. [prompts/01-project-scan.md](./prompts/01-project-scan.md)
2. [prompts/02-book-plan.md](./prompts/02-book-plan.md)
3. [prompts/03-preface-pack.md](./prompts/03-preface-pack.md)
4. [prompts/04-chapter-batch.md](./prompts/04-chapter-batch.md)
5. [prompts/05-navigation-and-appendix.md](./prompts/05-navigation-and-appendix.md)
6. [prompts/06-quality-pass.md](./prompts/06-quality-pass.md)

## 推荐输出结构

建议让 Codex 最终把内容写到一个单独目录，例如：

```text
generated-books/my-project-book/
├─ meta/
│  ├─ project-profile.json
│  └─ book-plan.json
└─ docs/
   ├─ README.md
   ├─ _sidebar.md
   ├─ _coverpage.md
   ├─ part00-preface/
   ├─ part01-*/
   ├─ part02-*/
   └─ appendix/
```

这样后续你只需要：

1. 指定目标项目路径
2. 指定输出目录和书名
3. 把对应 prompt 发给 Codex

## 使用原则

- 不强行套 `sample-project-claude-code` 的 12 篇结构。
- 书的结构要跟随项目规模、项目类型、读者难度自动调整。
- 所有源码结论都必须能追溯到具体文件或目录。
- 对不确定的信息，必须显式标注“待确认”，不能脑补。
- 章节按“问题驱动”组织，不按“文件夹顺序”堆砌。

## 你后续对 Codex 说什么

最短版本可以直接这么说：

```text
阅读当前项目，并严格按照 project-to-book-kit/ 下的框架、工作流、模板和 prompts/00-master-orchestrator.md，
为这个项目生成一本零基础也能看懂的 Markdown 书，输出到指定目录。
```

如果你想更稳一点，就分阶段执行 `prompts/` 里的文件。

