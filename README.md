# AI Code Alignment

最小化 GitHub PR 相对 base 的 diff：剥离与功能无关的格式化 / 风格噪声，只保留真正的功能改动，并生成一个干净的新 commit，从而减轻人工代码审查的负担。

## 工作方式

AI agent 进入本目录时会自动加载指令文件：

- **[AGENTS.md](./AGENTS.md)** —— 面向所有 agent 的完整工作指令（唯一权威源）。
- **[CLAUDE.md](./CLAUDE.md)** —— Claude Code 专属入口，通过 `@AGENTS.md` 导入，与所有 agent 共享同一份指令。

## 使用

把一个 PR 地址丢给任意支持 AGENTS.md 的 AI agent 即可，例如：

```
https://github.com/owner/repo/pull/123
```

Agent 会分析该 PR，剥离相对 base 的格式噪声，产出一个只含功能改动的新 commit，供人工审核。
