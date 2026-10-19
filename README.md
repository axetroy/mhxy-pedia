# 梦幻西游游戏百科

一个面向中文用户的 Agent Skill：查询梦幻西游的版本、活动、玩法和游戏规则时，尽可能实时核验官方资料，并清楚标注适用版本、服务器、时间和来源。

主 `SKILL.md` 仅作为专题目录，具体规则维护在 `references/` 下的独立文件中。最新维护信息在回答时实时核验，不固化易过期公告。

## 能力范围

- 查询版本更新、活动、维护、门派、技能、玩法、道具、任务、召唤兽、养成、战斗和游戏内经济规则。
- 对易变信息检索当前公开来源，说明版本、服务器、时间及来源可信度。

## 时效与边界

实时核验依赖使用该 Skill 的 Agent 当次可用的联网搜索或浏览工具。本项目不提供实时数据库、自动抓取或持续监控；无法联网时，Skill 必须说明无法核验，不得将旧知识描述成最新结论。

本 Skill 仅覆盖游戏百科，不提供法律、商业经营或现实交易合规分析。活动安排和游戏数值等易变信息，以已核实来源及其适用范围为准。

## 使用方法

使用 Skills CLI 安装（需要 Node.js 和 npm/npx）：

```sh
npx skills add axetroy/mhxy-pedia --skill mhxy-pedia
```

安装后可以这样提问：

> 查一下本周梦幻西游的维护公告，标明公告日期和适用服务器。
>
> 解释当前版本召唤兽内丹效果，并说明适用范围和资料来源。

卸载命令：

```sh
npx skills remove mhxy-pedia
```

## 项目规划

当前版本聚焦于可靠的检索与回答流程，不内置游戏数据或自动更新服务。技能指令采用专题文件维护：维护公告、版本与活动、玩法知识、来源与回答规范分别更新，主 `SKILL.md` 只负责导航。最新维护信息需在回答时实时核验，不把易过期公告写成永久事实。

## 项目文件

```text
.
├── .agents/skills/mhxy-pedia/
│   ├── SKILL.md
│   └── references/
│       ├── gameplay.md
│       ├── maintenance.md
│       ├── sources-and-answering.md
│       └── version-and-events.md
├── .github/workflows/validate-skill.yml
├── LICENSE
└── README.md
```

本项目无需运行时依赖或构建步骤。CI 会校验 Skill 和项目文档。

## 许可证

本项目采用 [MIT 许可证](LICENSE)。
