# VOC Framework

## Coding Schema

Use this schema when the user needs repeatable coding, a spreadsheet-ready taxonomy, or a formal report.

| Field | Meaning | Examples |
| --- | --- | --- |
| feedback_id | Stable row or quote id | ticket-1031, interview-07 |
| source | Origin of feedback | support, survey, review, interview |
| segment | User or account group | enterprise admin, free user, churned |
| journey_stage | Where the issue appears | discovery, onboarding, activation, renewal |
| product_area | Affected module or workflow | billing, dashboard, export, mobile |
| sentiment | emotional valence | positive, neutral, mixed, negative |
| theme | normalized topic label | slow setup, unclear pricing, missing export |
| user_need | desired outcome in user's language | "I need to compare branches quickly" |
| pain_point | concrete friction | dashboard filters reset unexpectedly |
| severity | impact level | low, medium, high, critical |
| evidence_type | support for the code | quote, count, rating, behavior, revenue |
| confidence | confidence in interpretation | low, medium, high |
| recommendation | action the team can take | simplify onboarding checklist |

## Severity Rubric

Critical:
- blocks core task completion
- causes churn, refund, compliance, or safety risk
- affects high-value users or many accounts

High:
- creates repeated workarounds
- delays activation, purchase, or renewal
- strongly negative sentiment with clear evidence

Medium:
- causes confusion or extra support contact
- affects a subset of users or a secondary workflow
- fix has plausible but unproven business impact

Low:
- cosmetic issue
- isolated preference
- evidence is weak or not tied to a meaningful outcome

## Priority Score

Use a 1-5 scale for each factor and explain assumptions:

priority = impact + frequency + urgency + confidence - effort

Where:
- impact: user/business value if solved
- frequency: how often it appears in the analyzed set
- urgency: risk of waiting
- confidence: quality and consistency of evidence
- effort: estimated implementation or process cost

Avoid false precision. Use the score to structure discussion, not to pretend certainty.

## Report Template

```markdown
# VOC Analysis Report

## Executive Summary

- Finding 1
- Finding 2
- Finding 3

## Data Reviewed

- Source:
- Records:
- Period:
- Segments:
- Limitations:

## Theme Summary

| Rank | Theme | Mentions | Share | Severity | Segment | Representative Quote | Implication |
| --- | --- | ---: | ---: | --- | --- | --- | --- |

## Top Pain Points

1. Pain point
   Evidence:
   Likely root cause:
   Business implication:

## Opportunities

| Opportunity | User Need | Evidence | Impact | Effort | Recommended Owner |
| --- | --- | --- | --- | --- | --- |

## Recommended Actions

- Immediate:
- Next 30 days:
- Later:

## Open Questions

- Question 1
- Question 2
```

## Analysis Notes

- For multilingual feedback, code themes in the reporting language but preserve quote language when possible.
- For duplicate comments from the same account, count both "mentions" and "unique accounts" if account identifiers exist.
- For star ratings or NPS, compare themes across rating bands rather than only averaging all feedback together.
- For interviews, do not over-count long conversations. Prefer participant-level evidence unless each statement is a distinct event.
- For social listening, call out sampling bias and platform-specific norms.
