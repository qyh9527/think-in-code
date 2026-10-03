# think-in-code

让 AI 编程助手在本地用命令或脚本处理大量数据（测试与构建输出、日志、多文件、JSON/CSV、git 历史），只把结论和可回查的证据位置带回上下文，而不是把原始输出整段读进对话。

## 安装

把本仓库作为一个技能目录放进 Claude Code / Codex 的 skills 目录（仓库根即技能根，入口为 `SKILL.md`），或在 [cc-switch](https://github.com/farion1231/cc-switch) 中以 `qyh9527/think-in-code` 添加。

## 建议：在 CLAUDE.md / AGENTS.md 加一行

技能是否被调用，取决于 AI 拿技能描述去比对当前情境。本技能最需要的时刻往往没有用户原话可比：AI 自己准备跑测试、翻日志，或刚看到「输出已截断」。在常驻指令里加一行指针，能让这些时刻更稳定地触发：

```markdown
- 跑测试或构建、翻日志、扫多个文件或 git 历史之前，或工具提示输出过大、已截断、已存到文件时，调用 `think-in-code` 技能：本地算完，只带回结论和 `路径:行号` 证据。
```

保持一行即可，细则留在技能里，避免两处规则不一致。

## 版本

技能文件推到 `main` 后由 GitHub Actions 自动发 release，附打包好的技能 zip。默认升 patch 版本；提交标题里写 `[minor]` 或 `[major]` 升对应级别，写 `[skip release]` 则这次不发。

## 致谢

「Think in Code」的说法与思路最早见于 [mksglu/context-mode](https://github.com/mksglu/context-mode)。本技能为独立编写，未使用其代码。

## 许可

[MIT](LICENSE)
