# Business Requirements Document
## Loan application process improvement

**Prepared by:** Raja Vinay Kumar

**Date:** October 2026

**Status:** Draft, based on data analysis only

---

## 1. Background

A Dutch bank handles personal loan applications online and through its staff. In 2016 it received 31,509 applications. I analysed the full event log of these applications to see how they move through the process, where they slow down, and where customers are lost.

I didn't have access to anyone at the bank. Everything in this document comes from the data. Where I'm guessing at the reason behind a pattern, I say so.

## 2. Business problem

Almost half of all applications don't end in a loan. 33% are cancelled and 12% are denied. Most of the time an application spends in the process is time spent waiting on the customer, not on the bank.

The bank loses customers it was willing to lend to, and it doesn't currently have a clear view of where or why.

## 3. Objectives

1. Reduce the number of applications cancelled after an offer is sent.
2. Cut the time lost to missing or incomplete documents.
3. Understand and close the gap between online and staff-entered applications.
4. Give managers an ongoing view of process performance.

## 4. Scope

**In scope:** the application process from creation to final outcome (approved, cancelled or denied), including offers and document checks.

**Out of scope:** credit decision rules, pricing, interest rates, and anything after a loan is approved.

## 5. Stakeholders

These are the roles I'd expect to be involved. I haven't spoken to any of them.

| Role | Interest |
|---|---|
| Head of lending operations | Owns the process and the targets |
| Loan officers | Do the checks and chase documents day to day |
| Customer service | Talk to customers who are waiting or confused |
| Digital / online channel team | Own the online application form |
| Risk team | Make sure changes don't weaken credit checks |
| IT | Build reminders, form changes and reporting |
| Customers | Want a quick, clear answer |

## 6. What the data shows today

- Only about 15% of applications follow the clean path from start to approval with no detours.
- About 30% reach the offer stage and are then cancelled without being validated.
- 78% of those cancellations happen between 29 and 32 days after the offer. It looks like an automatic 30-day timeout.
- Around 70% of all waiting time happens after the bank sends an offer.
- 69% of applications that reach validation are sent back as incomplete at least once.
- Around 960 applications were cancelled while the bank was chasing documents.
- Online applications are approved less often (about 49% vs 65%) and cancelled more often (37% vs 26%) than staff-entered ones.
- The bank's own steps are quick. Most internal checks take under a day.
- A typical application takes about 19.5 days from start to outcome.

## 7. Business requirements

| ID | Requirement | Why | Priority |
|---|---|---|---|
| BR-01 | Send customers reminders after an offer, around day 7 and day 14 | Most cancellations happen at the 30-day mark with no contact in between | High |
| BR-02 | Show customers a clear document checklist when they apply | Most validated applications need rework for missing documents | High |
| BR-03 | Let customers upload documents and see what's still missing | Reduces back-and-forth during validation | Medium |
| BR-04 | Give online applicants a follow-up contact after the offer | Online applications are cancelled more often | Medium |
| BR-05 | Provide a dashboard of process KPIs, refreshed regularly | Managers can't currently see where applications get stuck | Medium |
| BR-06 | Report workload per staff member | Ten of 142 staff complete about 31% of tasks | Low |

## 8. Success measures

The targets below are my suggestions. The bank would need to agree them.

| Measure | Today | Suggested target |
|---|---|---|
| Cancellation rate | 33.2% | Under 28% |
| Applications needing document rework | 69% | Under 50% |
| Median days to outcome | 19.1 | Under 16 |
| Online approval rate | ~49% | Within 10 points of staff |

## 9. Assumptions and constraints

- The 30-day cancellation pattern is an automatic rule. I can't confirm this from the data.
- Customers can be contacted by email or SMS during the offer period.
- Changes must not lower credit standards.
- The data covers 2016 only. The process may have changed since.

## 10. Open questions for the bank

1. Is there a 30-day rule for cancelling offers? Can it be changed?
2. What does a requested amount of 0 mean? About 3,000 applications have it, and they're approved more often than average.
3. Why are online applications cancelled more often?
4. Why do a few staff handle so much more work than others? Different roles, or part-time staff?