# 安装与使用 AI 论文写作 Skill

Skill 目录为 `skills/ai-paper-writing/`，包含 `SKILL.md` 与 `references/`。安装时复制整个目录。这个 Skill 通过指令和提示词运行，无额外脚本依赖。

## 在 Codex 中安装

先下载并解压整个 GitHub 仓库。以下命令均从解压后的资料仓库根目录运行。任选一种安装范围。

**当前项目（macOS / Linux）**

```bash
project_dir="/实际路径/你的论文项目"
mkdir -p "$project_dir/.agents/skills"
cp -R skills/ai-paper-writing "$project_dir/.agents/skills/"
```

**当前用户（macOS / Linux）**

```bash
mkdir -p "$HOME/.agents/skills"
cp -R skills/ai-paper-writing "$HOME/.agents/skills/"
```

**Windows**

在资源管理器里将整个 `skills\ai-paper-writing` 复制到论文项目下的 `.agents\skills\`，或个人目录 `%USERPROFILE%\.agents\skills\`。如果目标目录尚不存在，先创建目录。

安装后目录应为 `.agents/skills/ai-paper-writing/SKILL.md`，旁边有 `references/`。在论文项目中打开 Codex，使用 `$ai-paper-writing` 调用。若技能选择器未显示，检查目录层级并重启 Codex。Linux 和 macOS 路径区分大小写的环境中，保留 `SKILL.md` 的大写文件名。[Codex 官方 Skill 文档](https://developers.openai.com/codex/skills)

## 在 ChatGPT 中使用

若工作区提供 Skills 上传入口，在 `Plugins → Skills → Create → Upload from your computer` 选择 Skill 压缩包。可直接使用仓库的 [Skill 安装包](downloads/ai-paper-writing-skill.zip)，或自行将 `skills/ai-paper-writing/` 单独压缩，确保包内有 `SKILL.md` 与 `references/`。安装后在对话里输入 `@` 从列表中选择该 Skill。入口和可用性取决于账号与工作区设置。[ChatGPT Skills 官方说明](https://help.openai.com/en/articles/20001066-skills-in-chatgpt)

普通对话也可以直接使用。选择对应的 TXT，替换占位内容，粘贴到对话，同时提供本次允许使用的材料。审稿、改写或文献任务用精确的章节范围和作者已确认的资料。

## 三个调用示例

```text
$ai-paper-writing 使用 06 检查 outline.md。研究问题是【填写】，目标读者是【填写】。仅给建议，指出哪些小节证据不足。
```

```text
$ai-paper-writing 对 draft.md 中标为「讨论第 2 段」的文字使用 11。给三个版本及修改说明，保留全部数值和引文编号。把结果放在对话里。
```

```text
$ai-paper-writing 对 introduction.md 先执行 20，再用 34 核查其中引文。证据只用 refs/ 中可读取的论文，缺失来源请列待查项。
```

调用时可直接说任务，例如「使用论文写作 Skill 检查提纲」。若平台仅能用聊天提示词，直接附上对应的文本。使用 31 可把改写切换成建议，使用 32 可落实作者点选的修改。对于仅有需求和材料摘要的场景，先做提纲，待作者核对研究证据后再进入正文。

## 更新与移除

更新时，以新版本的完整 Skill 目录替换原目录，保留你另外备份的个人改动。移除时可从已安装位置移走 `ai-paper-writing` 文件夹。重启 Codex 或刷新技能面板后核对版本。
