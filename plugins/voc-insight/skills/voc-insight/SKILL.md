---
name: voc-insight
description: Bilingual Chinese/English VOC and customer insight analysis. Analyze Voice of Customer (VOC), 客户之声, 用户反馈, 访谈记录, 客服工单, 应用商店评论, 问卷开放题, NPS/CSAT 评论, 社媒评论, 销售记录, 流失原因, pain points, product opportunities, and customer sentiment. Use when the user asks in Chinese or English to classify feedback, extract themes, 归纳主题, 发现痛点, quantify evidence, 生成 VOC 报告, identify product opportunities, or turn messy customer text into prioritized recommendations.
---

# VOC Insight / 客户之声洞察

Treat VOC work as evidence synthesis, not just summarization. 将 VOC 工作视为“证据综合”，而不只是摘要。Preserve the user's voice while turning messy feedback into decisions a product, growth, customer success, or operations team can act on.

Default to the user's language. If the request or data is Chinese, respond in Chinese; if it is English, respond in English; if it is mixed, produce bilingual headings or a bilingual summary when useful.

## Workflow / 工作流

1. Clarify the business objective / 明确业务目标:
   - product improvement / 产品改进
   - churn reduction / 降低流失
   - onboarding optimization / 新手引导优化
   - pricing or packaging feedback / 定价与套餐反馈
   - competitive intelligence / 竞品洞察
   - service quality improvement / 服务质量改进
   - opportunity discovery / 机会点发现
2. Inspect the data shape / 检查数据形态:
   - source type: interviews, surveys, tickets, reviews, social posts, call transcripts, CRM notes, or mixed sources
   - 来源类型：访谈、问卷、客服工单、评论、社媒、通话转写、CRM 记录或混合数据
   - fields: segment, account, product area, channel, date, rating, revenue, region, status, and free text
   - 字段：用户分群、账号、产品模块、渠道、日期、评分、收入、地区、状态、文本内容
3. Normalize only enough to analyze / 只做必要清洗:
   - keep original wording for evidence / 保留原话作为证据
   - merge exact duplicates / 合并完全重复记录
   - keep rare negative or outlier feedback visible / 不因少数或极端反馈而删除
4. Code feedback into themes / 将反馈编码成主题:
   - pain point / 痛点
   - desired outcome / 期望结果
   - blocker or friction / 阻碍与摩擦
   - feature request / 功能诉求
   - sentiment / 情绪倾向
   - journey stage / 旅程阶段
   - severity / 严重程度
   - segment or persona / 分群或用户画像
5. Quantify themes transparently / 透明量化:
   - mention count and share / 提及次数与占比
   - share within segment / 分群内占比
   - links to rating, NPS, churn, revenue, or ticket severity when available / 与评分、NPS、流失、收入或工单等级的关联
6. Separate facts, interpretations, and recommendations / 区分事实、解读和建议:
   - facts: quotes, counts, ratings, timestamps / 事实：原话、数量、评分、时间
   - interpretations: root causes, hypotheses, opportunity sizing / 解读：根因、假设、机会大小
   - recommendations: actions and expected impact / 建议：行动与预期影响
7. Prioritize with a simple frame / 用简单框架排序:
   - user impact / 用户影响
   - business impact / 业务影响
   - frequency / 频次
   - urgency or severity / 紧急度或严重度
   - confidence / 证据可信度
   - estimated effort / 预估成本

## Output / 输出格式

Default to a concise report. 默认输出一份简洁报告：

- Executive summary / 核心摘要：3-5 个最重要发现
- Theme table / 主题表：主题、证据数量/占比、影响分群、严重度、代表性原话、含义
- Top pain points / 主要痛点：按优先级列出证据、可能根因和影响
- Opportunities / 产品或流程机会：改什么、为什么现在改、预期收益
- Open questions / 待确认问题：还缺哪些数据
- Recommended actions / 建议行动：立即、短期、长期

When the user asks for product strategy, add opportunity map, persona implications, roadmap candidates, experiment ideas, and success metrics. 当用户要产品策略时，补充机会地图、人群/画像启示、路线图候选、实验想法和成功指标。

When the user asks for customer success or operations, add escalation triggers, response playbooks, retention risks, service process fixes, and knowledge-base gaps. 当用户要客户成功或运营建议时，补充升级触发条件、响应话术/流程、留存风险、服务流程修复和知识库缺口。

## Evidence Standards / 证据标准

- Use short representative quotes, not long transcripts. 使用短代表性原话，不粘贴长转写。
- Label low-confidence themes when sample size is small or source bias is high. 样本小或来源偏差高时，标注低置信度。
- Do not infer demographics, intent, or commercial impact unless the data supports it. 不在证据不足时推断人群属性、意图或商业影响。
- Prefer "mentions" over "users" unless each record maps cleanly to one unique user. 除非记录能唯一对应用户，否则用“提及次数”而不是“用户数”。
- State whether percentages are based on coded records, unique users, accounts, or all feedback. 明确百分比的分母：编码记录、唯一用户、账号或全部反馈。
- Keep contradictory feedback visible; tension often signals segmentation or job-to-be-done differences. 保留矛盾反馈，它通常提示分群或使用场景差异。

## Reference / 参考

For a deeper bilingual coding rubric, report templates, and priority scoring guidance, read `${CODEBUDDY_SKILL_DIR}/references/voc-framework.md` when the task needs a detailed methodology or reusable scoring model. 如需更完整的双语编码表、报告模板和优先级评分方法，读取该参考文件。
