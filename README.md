# VOC Insight Hub / VOC 洞察中枢

Public bilingual WorkBuddy/CodeBuddy marketplace for VOC analysis and customer insight skills.

面向 WorkBuddy/CodeBuddy 的中英双语 VOC 分析与客户洞察技能市场。

## 中文说明

### 包含技能

| 插件 | 技能 | 能力 |
| --- | --- | --- |
| `voc-insight` | `voc-insight` | 将用户反馈、访谈、客服工单、评论、问卷开放题、NPS/CSAT 评论和社媒评论转成结构化 VOC 洞察、痛点归因和优先级建议。 |

### 在 WorkBuddy 中安装

1. 打开 WorkBuddy。
2. 进入 `专家` -> `技能` -> `套件`。
3. 点击 `+` 添加市场源。
4. 输入：

```text
Arianassskm/VOC-Insight-Hub
```

5. 提交并等待市场同步。
6. 从 VOC Insight Hub 市场安装 `voc-insight`。

安装后，可以直接让 WorkBuddy 分析“客户之声、用户反馈、访谈记录、客服工单、问卷开放题、NPS/CSAT 评论、痛点和机会点”等内容。

### 在 CodeBuddy Code 中安装

```text
/plugin marketplace add Arianassskm/VOC-Insight-Hub
/plugin install voc-insight@voc-insight-hub
/reload-plugins
```

## English

### Included Skill

| Plugin | Skill | What it does |
| --- | --- | --- |
| `voc-insight` | `voc-insight` | Turns customer feedback, interviews, tickets, reviews, surveys, NPS/CSAT comments, and social comments into structured VOC insights, pain-point diagnosis, and prioritized recommendations. |

### Install In WorkBuddy

1. Open WorkBuddy.
2. Go to `Experts` / `专家` -> `Skills` / `技能` -> `Suites` / `套件`.
3. Click `+` to add a marketplace.
4. Enter:

```text
Arianassskm/VOC-Insight-Hub
```

5. Submit and wait for the marketplace to sync.
6. Install `voc-insight` from the VOC Insight Hub marketplace.

After installation, ask WorkBuddy to analyze VOC or customer feedback data, or invoke the skill from the plugin namespace if your WorkBuddy build exposes manual skill invocation.

### Install In CodeBuddy Code

```text
/plugin marketplace add Arianassskm/VOC-Insight-Hub
/plugin install voc-insight@voc-insight-hub
/reload-plugins
```

## Repository Structure / 仓库结构

```text
.
├── .codebuddy-plugin/
│   └── marketplace.json
└── plugins/
    └── voc-insight/
        ├── .codebuddy-plugin/
        │   └── plugin.json
        └── skills/
            └── voc-insight/
                ├── SKILL.md
                └── references/
                    └── voc-framework.md
```

## Direct Download / 直接下载

You can download the repository as a ZIP from GitHub, or use the packaged release asset named `voc-insight-hub-workbuddy-marketplace.zip` when available.

你也可以直接下载 GitHub ZIP，或下载 Release 中的 `voc-insight-hub-workbuddy-marketplace.zip`。

## Compatibility / 兼容性

This marketplace follows the CodeBuddy/WorkBuddy plugin marketplace layout. 本市场遵循 CodeBuddy/WorkBuddy 插件市场结构：

- marketplace file: `.codebuddy-plugin/marketplace.json`
- plugin manifest: `.codebuddy-plugin/plugin.json`
- skill directory: `skills/<skill-name>/SKILL.md`

## License

MIT
