---
name: prompts
description: 列出我所有的提示词(清单模式,不做推荐/预览)
---

(用户输入: $ARGUMENTS)

## 你的任务

### 第一步:扫描仓库
读取 /Users/yigaoming/Documents/GitHub/my-prompts/ 目录的所有子文件夹(排除 .git 和 prompts 自己)。
对每个子文件夹,用 Read 工具读其中的 SKILL.md,提取 frontmatter(---之间的 YAML)里的 `name` 和 `description`。

### 第二步:按 7 大分类整理

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
不管 $ARGUMENTS 是空还是有内容,都按下面这个格式列出全部(本 skill 不做推荐、不做预览):

```
📋 我的提示词库(共 N 个)

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

💡 用法:直接输入 /<名字> <你的内容> 就能调用。
   例:/vis-ppt 我的PPT主题是 XXX
   想看完整正文:打开 ~/Documents/GitHub/my-prompts/<文件夹>/SKILL.md
```

不要执行任何提示词,只列清单。
