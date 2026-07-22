---
name: prompts
description: 列出我所有的提示词,或根据需求推荐合适的提示词
---

(用户输入: $ARGUMENTS)

## 你的任务

### 第一步:扫描我的提示词库
- 用 Read 工具读 /Users/yigaoming/Documents/GitHub/my-prompts/ 目录
- 列出所有子文件夹(每个文件夹 = 一个提示词,排除 .git 和 prompts 自己)
- 对每个子文件夹,用 Read 工具读其中的 SKILL.md
- 提取每个 SKILL.md 顶部的 frontmatter(---之间的 YAML),得到 `name` 和 `description`

### 第二步:按以下 7 大分类整理(用命令名前缀判断)
| 分类 | 前缀 |
|---|---|
| 平台内容 | xhs- / dy- / wx- / wb- / bili- / zh- |
| 通用文案 | copy- |
| 策略洞察 | str- |
| 视觉设计 | vis- |
| 提案方案 | prop- |
| 审稿改稿 | rev- |
| 杂项 | misc- |

### 第三步:输出格式
如果用户没带具体需求(只输入 /prompts),用以下格式列出全部:
```
📋 你的提示词库(共 N 个)

🔍 平台内容(xhs-/dy-/wx-...)
  [name] — [description]
  ...

✍️ 通用文案(copy-)
  ...

🎯 策略洞察(str-)
  ...

🎨 视觉设计(vis-)
  [name] — [description]
  ...

📄 提案方案(prop-)
  ...

🔍 审稿改稿(rev-)
  ...

🗃️ 杂项(misc-)
  [name] — [description]
  ...

💡 不知道用哪个?直接说"我要做 X",我帮你挑。
```

### 第四步:如果用户带了具体需求
- 用户输入内容在 $ARGUMENTS 里
- 根据每个提示词的 description,推荐最合适的 1-3 个
- 说明推荐理由
