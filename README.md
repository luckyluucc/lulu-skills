# 露露 Skills

一组可以独立使用的 Agent Skills。每个 Skill 放在 `skills/` 下的独立文件夹中；安装整包时，各 Skill 会分别出现在支持的 Agent 中。

## 已收录

| Skill | 用途 |
| --- | --- |
| [`situated-decision-guide`](skills/situated-decision-guide/SKILL.md) | 从具体处境中发现值得回答的问题，并结合个人目标、约束和证据给出决策建议。 |

## 安装

需要 Node.js 环境。

```bash
npx skills add luckyluucc/lulu-skills --all -g -a codex -y
```

这条命令一次安装仓库中的所有 Skill，供 Codex 在各项目中使用。使用其他支持的 Agent 时，替换 `-a codex`；也可以省略 `-a codex`，按安装程序提示选择。

想先查看整包内容：

```bash
npx skills add luckyluucc/lulu-skills --list
```

以后新增 Skill，重新执行整包安装命令，才能把新成员也安装进来。已有 Skill 可使用 `npx skills update -g` 更新。

## 使用

安装后，可以直接说出你的问题，让 Agent 按 Skill 描述判断何时使用；也可以明确指定 `situated-decision-guide`。这套仓库的“整包”指一次安装多个独立 Skill，目前没有统一的总入口或固定调用顺序。

## 增加 Skill

在 `skills/` 下新建一个文件夹，放入带有 `name` 和 `description` YAML 头部的 `SKILL.md`。文件夹名与 `name` 保持一致，例如：

```text
skills/
  situated-decision-guide/
    SKILL.md
  another-skill/
    SKILL.md
```

发布前检查 Skill 中是否有私人信息、密钥、本地绝对路径、未经授权的客户材料或对外写入行为。
