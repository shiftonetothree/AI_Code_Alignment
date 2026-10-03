# CLAUDE.md

本项目的核心工作：当用户提供一个 GitHub PR 地址时，分析该 PR 相对 base 的改动，剥离与功能无关的格式化 / 风格噪声，只保留真正的功能改动，并基于该 PR 的 commit 生成一个更干净的新 commit，以最小化 diff、减轻人工审查负担。用户给出 PR 地址即视为启动该任务。

完整指令与所有 agent 共享同一份（AGENTS.md），通过下方导入加载：

@AGENTS.md
