# 完整安装清单

> 核对日期：2026 年 11 月 16 日。
> 「来源」一栏有链接的，是找到了资料的；写着 **待核实** 的，是没找到官方文档的，照着做可能不生效。
> 照着装不生效，请改用 [README 里的方法一](README.md)（让助手自己装），或本页的方法四（直接贴文字）。

---

## 先分清你手上的是哪个压缩包

这个仓库里会出现**两个**压缩包，名字很像，但用途不同：

| 你手上的文件 | 解压后看到什么 | 该拿它做什么 |
|---|---|---|
| `github-easy-guide.zip`（小，约 6 千字节） | 一个 `github-easy-guide` 文件夹，里面**只有** `SKILL.md` | 这才是要装进助手的技能包。方法二上传它，方法三放文件夹也用它 |
| 整个仓库的压缩包（名字带 `repo`，比如 `github-easy-guide-repo-v4.zip`，约 19 千字节） | 一个 `github-easy-guide` 文件夹，里面有 `README.md`、`INSTALL.md`、`SKILL.md`、`LICENSE` 和上面那个小压缩包 | 这是给别人看说明用的**资料包**，不是拿来上传的技能包。要看说明就解压它；要装技能，请用里面那个小的 `github-easy-guide.zip` |

两者解压出来的文件夹都叫 `github-easy-guide`，容易套错。区分办法：打开文件夹，**里面只有一个 `SKILL.md` 的**是技能包；**里面有 `README.md`、`INSTALL.md` 等好几个文件的**是资料包。手动放文件夹（方法三）时两者都能用，因为 `SKILL.md` 都在第一层；界面里「上传技能」建议用那个小的技能包，多带文件会不会被接受，各助手不一样，本页未核实。

---

## 方法二：在助手界面里点按钮

| 助手 | 点哪里 | 来源 |
|---|---|---|
| WorkBuddy（腾讯） | 左侧「技能」→「添加技能」→「上传技能」→ 拖入 `github-easy-guide.zip` | 待核实 |
| TRAE（字节） | 右上角 ⚙ 设置 →「规则和技能」（新版可能叫「技能与命令」）→ 技能 →「创建」→ 选「全局」→ 上传 zip 或 SKILL.md →「确认」 | 原第三方教程链接已于 2026-11-16 核实为打不开（两次访问都显示页面不存在），暂未找到可替代的在读资料；菜单名称与上传入口均待核实 |
| CodeBuddy（腾讯） | 设置页「导入 Skill」，或在命令面板搜「CodeBuddy: Install Skill」 | 待核实 |
| Qoder（阿里） | 设置 → Plugins（插件）→ Marketplace（市场） | [Qoder 官方文档](https://docs.qoder.com/extensions/plugins)，2026-11-16 核实可打开 |
| Claude 网页版 / App | 设置 → 功能（Capabilities）→ Skills → 上传 zip。**这类服务在中国通常打不开，先确认能打开再往下做** | 待核实 |

---

## 方法三：手动放文件夹

把解压出来的**整个** `github-easy-guide` 文件夹放进下表对应的位置。注意是整个文件夹，不是里面的 `SKILL.md`，也不是压缩包。放好后**重新打开**助手。

放好后的样子必须是这样，不能多套一层：
```
skills
└── github-easy-guide
    └── SKILL.md
```

**关于 `~` 和以点开头的文件夹：**
- `~` 就是你的用户文件夹：Windows 是 `C:\Users\你的用户名\`，苹果电脑是 `/Users/你的名字/`
- 名字以点开头的文件夹默认是隐藏的：Windows 打开任意文件夹 → 上方「查看」→「显示」→ 勾选「隐藏的项目」；苹果电脑在访达里同时按 `Command + Shift + .`
- 文件夹不存在就自己新建一个，名字要一字不差

### 3.1 中国常用的助手

| 助手 | 放到哪个文件夹 | 来源 |
|---|---|---|
| WorkBuddy | `~/.workbuddy/skills/` | [第三方教程](https://gitcode.csdn.net/6aa0e45d1a35784c8420ae91.html)，2026-11-16 核实可打开；**另在本机核实：该目录确实存在且已有多个技能在用**（2026-11-16），是目前最可靠的一条。另有资料说新版改用插件目录，待核实 |
| TRAE | `~/.trae/skills/`（全局）；项目里的 `.trae/skills/` | [第三方资料](https://cdn.jsdelivr.net/npm/aegis-method-pack@2.9.2/docs/README.trae.md)，2026-11-16 核实可读取，文中明确列出这两个路径 |
| TRAE 中国版 | `~/.trae-cn/skills/` | 待核实 |
| CodeBuddy | 项目里的 `.codebuddy/skills/`；全局 `~/.codebuddy/skills/` 待核实 | 原标注的「腾讯云官方文档」链接已于 2026-11-16 核实为打不开（两次访问都显示页面不存在），暂未找到可替代的在读资料；路径本身待核实 |
| Qoder | `~/.qoderwork/skills/` | [第三方教程](https://aicoding.csdn.net/6a55b02710ee7a33f28d3f8b.html)，2026-11-16 核实可打开 |
| 通义灵码 | `~/.lingma/skills/` | 待核实 |
| Qwen Code | `~/.qwen/skills/` | 待核实 |
| Kimi Code CLI | `~/.kimi-code/skills/` | 待核实 |
| 其他（文心快码等） | `~/.agents/skills/` | 待核实 |
| **拿不准就放这** | `~/.agents/skills/`：很多新工具都会读这个文件夹 | 待核实 |

### 3.2 中国以外常用的助手

**这类服务在中国通常打不开，能不能用以它当前的官方说明为准，先确认能打开再往下做。** Claude 网页版 / App 不用放文件夹，见方法二。

| 助手 | 放到哪个文件夹 | 来源 |
|---|---|---|
| Claude Code | `~/.claude/skills/`；项目里的 `.claude/skills/` | 待核实 |
| OpenAI Codex | `~/.agents/skills/`（部分版本是 `~/.codex/skills/`） | 待核实 |
| Cursor | `~/.cursor/skills/`；项目里的 `.cursor/skills/` | 待核实 |
| Gemini CLI | `~/.gemini/skills/`；项目里的 `.gemini/skills/` | 待核实 |
| VS Code / GitHub Copilot | `~/.copilot/skills/`；项目里的 `.github/skills/` | 待核实 |
| Windsurf、OpenCode 等 | 多数读 `~/.agents/skills/` | 待核实 |

---

## 方法四：助手没有「上传技能」入口怎么办

豆包、腾讯元宝、DeepSeek、Kimi、通义千问、WPS 灵犀这类聊天或办公 App，没查到上传技能的入口（不代表以后不会有）。可以换个办法：

1. 用记事本打开解压出来的 `SKILL.md`
2. 删掉最开头 `---` 到第二个 `---` 之间那几行
3. 把剩下的全部复制，粘到新对话的最开头，前面加一句：

```
下面是一份工作说明，从这个对话起请照着它回答我：
```

4. 通常可以在当前对话里使用；换新对话要重新贴一次。App 有「自定义指令」「智能体设定」之类的功能的话，存进去就不用每次贴了

---

## 怎么确认装好了

新开一个对话，**不要附任何文件**，只发这句：

```
你现在有没有一个叫 github-easy-guide 的技能？有的话，用一句话告诉我它是干嘛的。
```

它答得出「把 GitHub 项目拆成大白话步骤」就是装好了。答不上来，按顺序检查：
1. 重启助手
2. 看文件夹是不是多套了一层、里面有没有 `SKILL.md`
3. 还不行，就用方法四直接贴文字
