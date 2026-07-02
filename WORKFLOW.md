# 生成工作流

这套工作流默认产出两个区域：

- `meta/`: 规划文件，给后续生成使用
- `docs/`: 最终书稿

## 第 1 步：项目扫描

目标：先建立“项目画像”，不要急着写书。

要做的事：

- 识别项目类型：库、CLI、前端、后端、移动端、AI 项目、单仓多包等
- 找入口文件、核心目录、运行命令、关键配置
- 估算项目规模
- 提取可能适合教学的主流程和主模块
- 识别不需要重点覆盖的目录，例如构建产物、依赖、自动生成代码

产物：

- `meta/project-profile.json`
- `meta/project-profile.md`

## 第 2 步：书籍规划

目标：把“源码结构”翻译成“教学结构”。

要做的事：

- 决定篇数和章节数
- 决定哪些主题单独成篇，哪些合并
- 给每一章定义一个明确问题
- 为每章绑定关键文件
- 确定读者前置知识和阅读路径

产物：

- `meta/book-plan.json`

## 第 3 步：生成前言包

目标：先把整本书的入口搭好。

要做的事：

- 写总导读
- 写学习路线图
- 写术语表初稿

产物：

- `docs/part00-preface/README.md`
- `docs/part00-preface/roadmap.md`
- `docs/part00-preface/glossary.md`

## 第 4 步：按批次生成章节

目标：分批写正文，避免上下文失控。

建议做法：

- 每次只生成 1-2 篇或 4-10 章
- 先写“基础篇”和“架构篇”
- 后写系统深挖、工程质量、亮点总结
- 每写完一批，就刷新侧边栏和索引草稿

产物：

- `docs/part01-*/`
- `docs/part02-*/`
- 更多 `docs/partNN-*/`

## 第 5 步：生成导航与附录

目标：把零散章节整理成一本能顺着读的书。

要做的事：

- 写 `docs/README.md`
- 写 `docs/_sidebar.md`
- 写 `docs/_coverpage.md`
- 写 `docs/appendix/source-index.md`
- 写 `docs/appendix/further-reading.md`

## 第 6 步：一致性检查

目标：防止整本书出现“能看但不稳”的问题。

重点检查：

- 章节标题是否和文件名一致
- 侧边栏链接是否存在
- 术语是否前后统一
- 是否存在明显重复章节
- 是否把猜测写成结论
- 是否有“只讲概念，不落源码”的空段落

## 第 7 步：单章返工

适用场景：

- 某一章太难
- 某一章太像技术文档，不像教程
- 某一章代码锚点不足
- 某一章和前后章节重复

做法：

- 只针对一个文件重写
- 不要连带重写整书
- 重写后同步 glossary 和 source-index

## 推荐顺序

如果你只想最稳地完成一次生成，按这个顺序：

1. `01-project-scan.md`
2. `02-book-plan.md`
3. `03-preface-pack.md`
4. `04-chapter-batch.md`
5. `05-navigation-and-appendix.md`
6. `06-quality-pass.md`

如果项目不大，也可以直接用 `00-master-orchestrator.md`。

