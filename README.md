# think-in-code

本地算，按需回：用命令或脚本把大量数据算成派生结果（计数、Top N、差异、分组、校验），只带回结论和可回查的证据位置。用于批量处理多文件、日志、JSON/CSV、测试或构建输出、git 历史时；阅读或修改具体源码时不用。

## 安装

把本仓库作为一个技能目录放进 Claude Code / Codex 的 skills 目录（仓库根即技能根，入口为 `SKILL.md`），或在 [cc-switch](https://github.com/farion1231/cc-switch) 中以 `qyh9527/think-in-code` 添加。

## 版本

技能文件推到 `main` 后由 GitHub Actions 自动发 release，附打包好的技能 zip。默认升 patch 版本；提交标题里写 `[minor]` 或 `[major]` 升对应级别，写 `[skip release]` 则这次不发。

## 致谢

「Think in Code」的说法与思路最早见于 [mksglu/context-mode](https://github.com/mksglu/context-mode)。本技能为独立编写，未使用其代码。

## 许可

[MIT](LICENSE)
