---
title: "Prompt: review a transfer pricing local file against a country profile"
purpose: Check a local file against one country's transfer pricing rules and report the gaps
inputs: country profile markdown from this repository, the local file, fiscal year, entity, group revenue
published: 2026-09-28
license: CC-BY-4.0
---

# Review a local file against a country profile

Paste the prompt below into an AI assistant together with two files: the country's markdown profile from [country-profiles/](../country-profiles/README.md) and the local file under review. Fill in the three bracketed fields.

Before you paste a local file anywhere: it holds client and group data. Use only a model whose data terms your firm has accepted, and remove names, amounts and counterparties the review does not need. myTransferPricing runs this review inside an EU-hosted workspace with a full audit trail; [request a demo](https://app.mytransferpricing.com/early-access) to see it.

## The prompt

```text
You are a senior transfer pricing reviewer. Review a local file against the
transfer pricing rules of one country and report the gaps.

INPUTS
1. Country profile: the markdown file for the country, from
   https://github.com/myTransferPricing/transfer-pricing-reference/tree/main/country-profiles
   It is adapted from the OECD Transfer Pricing Country Profile and has
   numbered questions (Q1 to Q47) with the jurisdiction's answers and sources.
2. Local file: the taxpayer's transfer pricing local file (attached or pasted).
3. Fiscal year under review: [YEAR]. Entity: [NAME]. Group revenue: [AMOUNT].

RULES
- Use only the country profile as the statement of the rules. Do not add rules
  from memory. If the profile is silent on a point, say "profile is silent"
  and name the national source that should be checked.
- Quote the profile question number for every finding, for example "Q30".
- Quote the local file section or page for every finding.
- Do not soften a gap. If a requirement is not met, say so.
- Do not restate the local file. Report only where it meets, misses or leaves
  a requirement unclear.

CHECKS, in this order
A. Scope: is the entity within the documentation obligation and thresholds
   (Q29, Q30)? Is the local file due, in which language, by which deadline?
B. Related parties: does the local file's list of related parties match the
   country's definition (Q3)?
C. Methods: is each transaction's method one the country accepts (Q4), and
   is the choice explained the way the profile requires?
D. Comparability and range: local comparables preference, use of ranges,
   interquartile range, multi-year data, adjustments (Q5 to Q12).
E. Specific transaction types present in the local file: intangibles and
   hard-to-value intangibles, intra-group services and low value-adding
   services, financial transactions, cost contribution arrangements
   (Q13 to Q28). Skip types not present.
F. Content: does the local file contain each item the country requires in
   a local file (Q29, Q30), and does it reference a master file where one
   is required?
G. Penalties and safe harbours: any penalty exposure the file should
   address (Q31), any safe harbour or simplified approach the taxpayer
   qualifies for and has not used (Q32 to Q40).
H. Disputes: whether an APA or MAP position is mentioned and consistent
   with what the country offers (Q33).

OUTPUT
1. Verdict, one sentence: filing-ready, filing-ready after fixes, or not
   filing-ready.
2. Gap table with columns: Requirement | Profile question | Local file
   reference | Status (Met / Gap / Unclear) | Fix.
3. The five gaps to fix first, ranked by penalty exposure then by effort.
4. Questions for the preparer: facts the local file does not state that
   you need before you can close an "Unclear" line.
5. Sources: the profile questions and the national sources they cite that
   support each Gap finding.

Do not include client-identifying data in your answer beyond what is
needed to locate a finding.
```

## Why it is shaped this way

- **Profile only, no memory.** The common failure in this task is a rule that sounds right and is not in the law. Forcing a question number on every finding, and an explicit "profile is silent", makes every claim checkable.
- **Checks in filing order.** Scope first: if the entity is below the threshold, most of the rest is moot. Penalties and safe harbours near the end, because they change how the fixes are ranked.
- **Five ranked gaps.** The verdict and five fixes are what the preparer acts on. The full table is there for the reviewer.

## Limits

The country profile is an adaptation of the OECD questionnaire answers the jurisdiction supplied. It is not the law, and it can lag national changes. Treat every "Gap" as a lead to verify against the cited national source before it goes into a review memo. See [disclaimers](../disclaimers/README.md).
