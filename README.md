# GETHAOP WorkBuddy Skills

Public WorkBuddy/CodeBuddy marketplace for the GETHAOP skill collection.

## Included Skills

| Plugin | Skill | What it does |
| --- | --- | --- |
| `voc-analysis` | `voc-analysis` | Turns customer feedback, interviews, tickets, reviews, surveys, NPS/CSAT comments, and social comments into structured VOC insights and prioritized recommendations. |

## Install In WorkBuddy

1. Open WorkBuddy.
2. Go to `专家` -> `技能` -> `套件`.
3. Click `+` to add a marketplace.
4. Enter:

```text
Arianassskm/GETHAOP
```

5. Submit and wait for the marketplace to sync.
6. Install `voc-analysis` from the GETHAOP marketplace.

After installation, ask WorkBuddy to analyze VOC/user feedback data, or invoke the skill from the plugin namespace if your WorkBuddy build exposes manual skill invocation.

## Install In CodeBuddy Code

```text
/plugin marketplace add Arianassskm/GETHAOP
/plugin install voc-analysis@gethaop
/reload-plugins
```

## Repository Structure

```text
.
├── .codebuddy-plugin/
│   └── marketplace.json
└── plugins/
    └── voc-analysis/
        ├── .codebuddy-plugin/
        │   └── plugin.json
        └── skills/
            └── voc-analysis/
                ├── SKILL.md
                └── references/
                    └── voc-framework.md
```

## Direct Download

You can download the repository as a ZIP from GitHub, or use the packaged release asset named `gethaop-workbuddy-marketplace.zip` when available.

## Compatibility

This marketplace follows the CodeBuddy/WorkBuddy plugin marketplace layout:

- marketplace file: `.codebuddy-plugin/marketplace.json`
- plugin manifest: `.codebuddy-plugin/plugin.json`
- skill directory: `skills/<skill-name>/SKILL.md`

## License

MIT
