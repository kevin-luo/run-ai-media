# run-ai-media

把 AI 热点、实测和产品进展，写成有人愿意停下来看的帖子。

`run-ai-media` 是一个给 Codex 使用的 AI 自媒体运营 Skill，覆盖热点核验、选题、真人感文案、热帖回复、配图、发布和复盘。仓库自带一套适合 AI / Codex 账号的写作口味，也可以改成你自己的账号。

> 这个仓库负责选题和账号运营。Codex + Remotion 的视频生产流水线会单独整理，不在这个 Skill 里。

## 它能做什么

- 搜索并核验当前 AI 热点，区分已证实信息和传闻
- 一次给出 3 个值得写的方向，再根据你的选择成稿
- 把发布会口吻改成人话，删掉模板味和空洞总结
- 写 X 主帖、热门帖子回复、干货帖和 Build in Public 内容
- 为截图、流程图或信息卡给出配图方案
- 记录发布链接，并按 2 小时 / 24 小时复盘

它不会编造测试结果、播放量、粉丝或收入，也不会逐句模仿某位创作者。

## 安装

### Windows

在 PowerShell 中运行：

```powershell
git clone https://github.com/kevin-luo/run-ai-media.git "$env:USERPROFILE\.codex\skills\run-ai-media"
```

### macOS / Linux

```bash
git clone https://github.com/kevin-luo/run-ai-media.git ~/.codex/skills/run-ai-media
```

安装完成后，请确认文件在这个位置：

```text
~/.codex/skills/run-ai-media/SKILL.md
```

如果 Codex 已经打开，新建一个任务或重启后再调用。

### 不使用 Git

1. 点击仓库右上角 `Code` → `Download ZIP`。
2. 解压后，把整个文件夹放到 `.codex/skills/run-ai-media`。
3. 确认 `SKILL.md` 直接位于 `run-ai-media` 目录下，别多套一层 `run-ai-media-main`。

## 30 秒上手

在 Codex 中直接说：

> 使用 $run-ai-media，把今天最值得写的 AI 话题整理成 3 个发帖方向。先别发布。

选好方向后：

> 使用 $run-ai-media 写成一条 X 主帖。说人话，给具体证据，删掉“不是……而是……”这类 AI 句式。

更多例子：

- `使用 $run-ai-media，把这段产品更新改成一条 200 字以内的真人感帖子。`
- `使用 $run-ai-media，找一条 12 小时内的热门 AI 帖，写一个有信息增量的回复。`
- `使用 $run-ai-media，把这个项目写成 Build in Public 帖，不能虚构用户和收入。`
- `使用 $run-ai-media，为这条干货帖设计一张暖白、黑字、酸橙绿点缀的信息卡。`
- `使用 $run-ai-media，复盘我最近 10 条帖子的钩子、证据和互动表现。`

## 改成你的账号

打开 `references/account-voice.md`，重点替换这几项：

- `Position`：你是谁，长期写什么
- `Reader promise`：关注你能得到什么
- `Voice`：语气、句长、常用表达
- `House visual`：固定配图风格
- `Hard limits`：坚决不说什么、不编什么

`references/creator-patterns.md` 存的是可以借鉴的内容结构，例如钩子、证据、反差和收尾。借结构，不复制句子，也不冒充任何创作者。

## 仓库结构

| 文件 | 用途 |
| --- | --- |
| `SKILL.md` | 完整工作流和写作规则 |
| `agents/openai.yaml` | Skill 在 Codex 中的展示信息 |
| `references/account-voice.md` | 账号定位、语气和禁区 |
| `references/creator-patterns.md` | 可组合的内容结构和写作模式 |
| `assets/social-card-template.svg` | 可编辑的信息卡模板 |

## 更新

进入已安装的目录后运行：

```bash
git pull
```

如果你改过自己的 `account-voice.md`，更新前先备份这份文件。

## License

MIT