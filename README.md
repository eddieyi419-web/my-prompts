# my-prompts

我的 AI 提示词库 — 在 Claude Code / Codex 里通过 `/xxx` 一键调用。

## 分类索引

### 🔍 平台内容 (xhs- / dy- / wx- / wb- / bili- / zh-)
*(暂无,等你加)*

### ✍️ 通用文案 (copy-)
*(暂无,等你加)*

### 🎯 策略洞察 (str-)
*(暂无,等你加)*

### 🎨 视觉设计 (vis-)
- [`vis-ppt`](vis-ppt/) — 为 PPT 主题生成 5 个艺术视觉风格方向(不是用途分类)

### 📄 提案方案 (prop-)
*(暂无,等你加)*

### 🔍 审稿改稿 (rev-)
*(暂无,等你加)*

### 🗃️ 杂项 (misc-)
- [`misc-kickoff`](misc-kickoff/) — 项目启动前先逐个提问澄清需求

## 使用方式

### 调用某个提示词
```
/<命令名> <你的内容>
```
例:`/vis-ppt 我的 PPT 主题是 AI 在营销中的应用`

### 查看所有提示词
```
/prompts
```

### 推荐合适的提示词
```
/prompts 我想改一篇温柔风的小红书种草文案
```

## 添加新提示词

1. 找到合适分类的前缀(参考上方索引)
2. 在仓库根目录新建 `<命令名>/` 文件夹
3. 文件夹内创建 `SKILL.md`,包含:
   - YAML frontmatter:`name` 和 `description`
   - Markdown 正文:实际的提示词内容
4. `git add` + `git commit` + push
5. CC Switch 自动同步

## 命名规范

- 平台内容:`<平台>-<动作>`,如 `xhs-check`、`dy-hook`
- 通用类型:`<类型>-<动作>`,如 `copy-slogan`、`str-competitor`
- 名字一律小写 + 短横线,不用中文
