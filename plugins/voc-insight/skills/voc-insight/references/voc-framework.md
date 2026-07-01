# VOC Framework / 客户之声分析框架

## Coding Schema / 编码字段

Use this schema when the user needs repeatable coding, a spreadsheet-ready taxonomy, or a formal report. 当用户需要可复用编码、表格化分类或正式报告时，使用这套字段。

| Field / 字段 | Meaning / 含义 | Examples / 示例 |
| --- | --- | --- |
| feedback_id / 反馈编号 | Stable row or quote id / 稳定记录或引文编号 | ticket-1031, interview-07 |
| source / 来源 | Origin of feedback / 反馈来源 | support, survey, review, interview / 客服、问卷、评论、访谈 |
| segment / 分群 | User or account group / 用户或账号分组 | enterprise admin, free user, churned / 企业管理员、免费用户、流失用户 |
| journey_stage / 旅程阶段 | Where the issue appears / 问题出现环节 | discovery, onboarding, activation, renewal / 发现、入门、激活、续费 |
| product_area / 产品模块 | Affected module or workflow / 受影响模块或流程 | billing, dashboard, export, mobile / 计费、仪表盘、导出、移动端 |
| sentiment / 情绪 | Emotional valence / 情绪倾向 | positive, neutral, mixed, negative / 正向、中性、混合、负向 |
| theme / 主题 | Normalized topic label / 归一化主题标签 | slow setup, unclear pricing, missing export / 配置慢、定价不清、缺少导出 |
| user_need / 用户需求 | Desired outcome in the user's language / 用户想达成的结果 | "I need to compare branches quickly" / “我想快速比较门店” |
| pain_point / 痛点 | Concrete friction / 具体摩擦 | dashboard filters reset unexpectedly / 筛选条件意外重置 |
| severity / 严重度 | Impact level / 影响等级 | low, medium, high, critical / 低、中、高、关键 |
| evidence_type / 证据类型 | Support for the code / 编码依据 | quote, count, rating, behavior, revenue / 原话、数量、评分、行为、收入 |
| confidence / 置信度 | Confidence in interpretation / 对解读的信心 | low, medium, high / 低、中、高 |
| recommendation / 建议 | Action the team can take / 团队可执行动作 | simplify onboarding checklist / 简化新手清单 |

## Severity Rubric / 严重度标准

Critical / 关键:
- blocks core task completion / 阻断核心任务完成
- causes churn, refund, compliance, or safety risk / 导致流失、退款、合规或安全风险
- affects high-value users or many accounts / 影响高价值用户或大量账号

High / 高:
- creates repeated workarounds / 需要反复绕路
- delays activation, purchase, or renewal / 延迟激活、购买或续费
- strongly negative sentiment with clear evidence / 有明确证据的强烈负面情绪

Medium / 中:
- causes confusion or extra support contact / 造成困惑或额外客服咨询
- affects a subset of users or a secondary workflow / 影响部分用户或次级流程
- fix has plausible but unproven business impact / 修复可能有业务影响但证据尚不足

Low / 低:
- cosmetic issue / 视觉或文案类小问题
- isolated preference / 孤立偏好
- evidence is weak or not tied to a meaningful outcome / 证据弱或未关联重要结果

## Priority Score / 优先级评分

Use a 1-5 scale for each factor and explain assumptions. 每个因素使用 1-5 分，并说明假设：

priority = impact + frequency + urgency + confidence - effort

Where / 含义:
- impact / 影响：解决后对用户或业务的价值
- frequency / 频次：在样本中出现的频率
- urgency / 紧急度：等待的风险
- confidence / 置信度：证据质量与一致性
- effort / 成本：实现或流程调整成本

Avoid false precision. Use the score to structure discussion, not to pretend certainty. 避免虚假精确；评分用于组织讨论，不是假装确定。

## Report Template / 报告模板

```markdown
# VOC Analysis Report / 客户之声分析报告

## Executive Summary / 核心摘要

- Finding 1
- Finding 2
- Finding 3

## Data Reviewed / 数据范围

- Source / 来源:
- Records / 记录数:
- Period / 时间范围:
- Segments / 分群:
- Limitations / 限制:

## Theme Summary / 主题汇总

| Rank / 排名 | Theme / 主题 | Mentions / 提及 | Share / 占比 | Severity / 严重度 | Segment / 分群 | Representative Quote / 代表原话 | Implication / 含义 |
| --- | --- | ---: | ---: | --- | --- | --- | --- |

## Top Pain Points / 主要痛点

1. Pain point / 痛点
   Evidence / 证据:
   Likely root cause / 可能根因:
   Business implication / 业务含义:

## Opportunities / 机会点

| Opportunity / 机会 | User Need / 用户需求 | Evidence / 证据 | Impact / 影响 | Effort / 成本 | Recommended Owner / 建议负责人 |
| --- | --- | --- | --- | --- | --- |

## Recommended Actions / 建议行动

- Immediate / 立即:
- Next 30 days / 未来 30 天:
- Later / 后续:

## Open Questions / 待确认问题

- Question 1
- Question 2
```

## Analysis Notes / 分析注意事项

- For multilingual feedback, code themes in the reporting language but preserve quote language when possible. 对多语言反馈，用报告语言编码主题，但尽量保留原话语言。
- For duplicate comments from the same account, count both "mentions" and "unique accounts" if account identifiers exist. 对同账号重复评论，若有账号标识，同时统计提及次数和唯一账号数。
- For star ratings or NPS, compare themes across rating bands rather than only averaging all feedback together. 对星级或 NPS 数据，按评分区间比较主题，不只看整体平均。
- For interviews, do not over-count long conversations. Prefer participant-level evidence unless each statement is a distinct event. 对访谈不要因对话长而过度计数，优先按参与者层面统计。
- For social listening, call out sampling bias and platform-specific norms. 对社媒数据，说明样本偏差和平台语境。
