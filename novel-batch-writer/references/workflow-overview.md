# 小说创作工程 — 完整工作流概览

## 四个阶段

```
第一阶段：规划（一次性完成）
  Step 1 选题策划      → novel-topic      → 1-选题.txt
  Step 2 核心设定      → novel-settings   → 2-核心设定.txt
  Step 3 标签与简介    → novel-settings   → 3-标签简介.txt
  Step 4 分卷大纲      → novel-outline    → 4-分卷大纲.txt
  Step 5 剧情单元      → novel-outline    → 5-第X卷-剧情单元.txt
  Step — 封面提示词    → novel-cover      → 6-封面提示词.txt

第二阶段：大纲批量生成（novel-batch-writer Part A）
  每5章一批 → 5-第{N}-{N+4}章-分章大纲.txt

第三阶段：正文批量写作（novel-batch-writer Part B）
  每5章一批 → 8-正文-第{N}章.txt + 7-批量核验-第{N}-{N+4}章.txt

第四阶段：审稿修改
  编剧审稿 → novel-review
  读者审稿 → novel-reader-review
  修改修复 → novel-editor
```

## 文件命名规范

| 文件 | 说明 |
|------|------|
| `1-选题.txt` | 书名 + 简介 + 核心卖点 |
| `2-核心设定.txt` | 世界观、等级、角色、行文风格 |
| `3-标签简介.txt` | 平台标签 + 500字黄金简介 |
| `4-分卷大纲.txt` | 5卷 × 60章宏观规划 |
| `5-第X卷-剧情单元.txt` | 12个单元/卷，每个5章 |
| `5-第{N}-{N+4}章-分章大纲.txt` | 每5章一个独立大纲文件 |
| `6-封面提示词.txt` | AI绘图提示词 |
| `7-批量核验-第{N}-{N+4}章.txt` | 正文核验报告 |
| `8-正文-第{N}章.txt` | 逐章正文 |

## 总规划参数

- 全书：300章，5卷，每卷60章
- 每卷：12个剧情单元（每个单元=5章）
- 大纲批次：每批5章
- 正文批次：每批5章
