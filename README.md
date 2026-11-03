# Skills

个人自建 AI skill 集合，逐步收录、维护和迭代。GitHub 仓库公开可见。

## Skill 索引

| Skill | 用途 | 调用示例 |
| --- | --- | --- |
| [房间里的大象](skills/elephant-in-the-room/SKILL.md) | 通过对话识别被忽略的重要问题；支持具体事件、整体扫描、已知问题深挖三种入口。 | `使用 $elephant-in-the-room，帮我看看当前可能忽略了什么。` |

## 目录结构

```text
skills/
  elephant-in-the-room/
    SKILL.md
    agents/
      openai.yaml
```

每个 skill 独立成包，必需文件为 `SKILL.md`；按实际需要添加 `agents/`、`references/`、`scripts/` 或 `assets/`。这些是供 AI 读取的指令和资源，不是独立运行的应用。

## 本地使用

克隆仓库后，可以把所需 skill 目录复制到支持该格式的工具的技能目录。当前这台机器的 Codex 已通过符号链接使用本仓库中的「房间里的大象」，修改源文件即可同步。

在 macOS / Linux 上，为 Codex 手动建立链接的示例（请先进入本仓库目录）：

```sh
mkdir -p "$HOME/.codex/skills"
ln -s "$PWD/skills/elephant-in-the-room" "$HOME/.codex/skills/elephant-in-the-room"
```

目标路径已存在时，先检查现有内容，不要直接覆盖。

## 添加新的自建 skill

1. 确认是自己创建或有权收录的内容；第三方安装的 skill 不自动归入自建集合。
2. 在 `skills/<skill-name>/` 中加入实际文件，名称使用小写字母、数字和连字符。
3. 在 `SKILL.md` 的 YAML 头部填写 `name` 和 `description`，正文写清使用情境、行为和边界。
4. 如有 `agents/openai.yaml`，保持其界面信息和调用名称与 skill 一致。
5. 更新本页索引，验证文件格式与代表性对话，再提交并推送。

上传前检查凭据、个人信息、内部项目资料及脚本运行输出。请勿将整个本机技能目录批量复制到仓库。

## 当前验证范围

「房间里的大象」已通过 skill 格式校验及六个首轮对话场景检查；长对话效果仍需实际使用验证。

## 许可

暂未指定开源许可证；公开可见不代表已授予开源使用许可，向他人授权使用前另行确定。
