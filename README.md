# novel-writing-skills

中文网文创作 Hermes Agent 技能集 — 用于番茄小说等平台的网文创作工作流。

## 完整技能列表

| 技能 | 分类 | 说明 |
|------|------|------|
| **novel-topic** | 选题 | 生成番茄小说爆款选题方案，一次3个供选 |
| **novel-settings** | 设定 | 核心设定、角色档案、等级体系、标签简介 |
| **novel-outline** | 大纲 | 分卷大纲→剧情单元→分章大纲，三层结构 |
| **novel-cover** | 封面 | 生成小说封面AI提示词 |
| **novel-batch-writer** | 批量写 | **核心引擎**：5章一批迭代写作+自动核验防漂移 |
| **novel-writer** | 单章写 | 单章正文写作（2500字+），防漂移和字数门 |
| **novel-review** | 审核 | 编剧视角审稿：剧情连贯性、质量、字数、节奏 |
| **novel-reader-review** | 读者审 | 挑剔读者视角：检视5章单元的连贯性、爽点、Bug |
| **novel-editor** | 修改 | 修复逻辑漏洞/人设崩坏、扩写细节/强化冲突 |
| **stop-slop-cn** | 过滤 | 中文网文去AI腔调过滤器 |
| **novel-evolve** | 另类 | 探索式协作写作，对话驱动、故事在写作中发现 |

## 标准工作流

```
选题（novel-topic）
  → 设定（novel-settings）
  → 大纲（novel-outline）
  → 批量写（novel-batch-writer Part A→Part B）
  → 审核（novel-review / novel-reader-review）
  → 修改（novel-editor）
  → 去AI腔过滤（stop-slop-cn）
```

## 项目参数

- 全书：300章，5卷，每卷60章
- 每卷：12个剧情单元（每个单元=5章）
- 大纲/正文批次：每批5章
- 正文硬性要求：每章2500字以上
