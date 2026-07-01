---
name: voc-analysis
description: Analyze Voice of Customer (VOC), user feedback, interviews, support tickets, app reviews, survey open text, NPS/CSAT comments, social comments, sales notes, or churn reasons. Use this skill when the user asks to classify feedback, extract themes, find pain points, quantify evidence, generate product opportunities, create a VOC report, or turn messy customer text into prioritized recommendations.
---

# VOC Analysis

Treat VOC work as evidence synthesis, not just summarization. Preserve the voice of users while turning messy feedback into decisions a product, growth, customer success, or operations team can act on.

## Workflow

1. Clarify the business objective if it is missing:
   - product improvement
   - churn reduction
   - onboarding optimization
   - pricing/package feedback
   - competitive intelligence
   - service quality improvement
   - opportunity discovery
2. Inspect the available data shape:
   - source type: interview notes, survey responses, tickets, reviews, social posts, call transcripts, CRM notes, or mixed sources
   - fields: user segment, account, product area, channel, date, rating, revenue, region, status, and free text
   - sample size and obvious bias
3. Normalize only enough to analyze:
   - keep original wording for evidence
   - merge duplicated records when exact duplicates are present
   - avoid deleting negative or outlier feedback just because it is rare
4. Code feedback into themes:
   - pain point
   - desired outcome
   - blocker or friction
   - feature request
   - emotional sentiment
   - affected journey stage
   - severity
   - segment or persona
5. Quantify themes with transparent denominators:
   - count of records mentioning the theme
   - share of analyzed records
   - share within relevant segment when segment data exists
   - rating, NPS, churn, revenue, or ticket severity association when available
6. Separate facts from interpretations:
   - facts: observed quotes, counts, ratings, timestamps
   - interpretations: root causes, hypotheses, opportunity sizing
   - recommendations: actions and expected impact
7. Prioritize with a simple decision frame:
   - user impact
   - business impact
   - frequency
   - urgency or severity
   - confidence in evidence
   - estimated effort when enough context exists

## Output

Default to a concise report with these sections:

- Executive summary: 3-5 bullets with the strongest findings
- Theme table: theme, evidence count/share, affected segment, severity, representative quote, implication
- Top pain points: ranked list with evidence and likely root cause
- Product or process opportunities: what to change, why now, expected benefit
- Open questions: what needs more data before deciding
- Recommended next actions: immediate, short-term, and longer-term

When the user asks for product strategy, add:

- opportunity map
- ICP/persona implications
- roadmap candidates
- experiment ideas
- success metrics

When the user asks for customer success or operations, add:

- escalation triggers
- response playbooks
- retention risks
- service process fixes
- knowledge-base gaps

## Evidence Standards

- Use short representative quotes, not long transcripts.
- Label low-confidence themes when sample size is small or source bias is high.
- Do not infer demographics, intent, or commercial impact unless the data supports it.
- Prefer "mentions" over "users" unless each record maps cleanly to one unique user.
- State when percentages are based on coded records rather than the full customer base.
- Keep contradictory feedback visible; tension often signals segmentation or job-to-be-done differences.

## Reference

For a deeper coding rubric, report templates, and priority scoring guidance, read `${CODEBUDDY_SKILL_DIR}/references/voc-framework.md` when the task needs a detailed methodology or reusable scoring model.
