---
pretty_name: Transfer pricing country rules, adapted from the OECD Transfer Pricing Country Profiles
license: cc-by-4.0
language:
  - en
tags:
  - transfer-pricing
  - tax
  - oecd
  - international-tax
  - legal
  - beps
task_categories:
  - question-answering
  - text-retrieval
size_categories:
  - n<1K
source_datasets:
  - original
---

# Transfer pricing country rules, adapted from the OECD Transfer Pricing Country Profiles

Authorship: the underlying profiles are published by the OECD, with answers supplied by each jurisdiction's tax administration. myTransferPricing is the author of this adaptation only (conversion to markdown, structure and links), not of the underlying work.

Country-by-country transfer pricing rules for 18 jurisdictions, one markdown file each, adapted from that country's OECD Transfer Pricing Country Profile. Each file holds the OECD questionnaire (up to 47 numbered questions) with the jurisdiction's answer and the legal sources it cited: arm's length principle, accepted transfer pricing methods, comparability analysis, intangibles, intra-group services, financial transactions, documentation thresholds and deadlines, dispute resolution, safe harbours and penalties.

Jurisdictions: Austria, Belgium, Brazil, Denmark, France, Germany, Greece, Ireland, Italy, Luxembourg, the Netherlands, Poland, Singapore, Spain, Sweden, Switzerland, the United Kingdom, the United States.

## Why this exists

AI assistants are now a first stop for transfer pricing questions, and in our own testing their answers on country rules are not yet reliable. They mix up documentation thresholds, deadlines and penalties between countries, cite rules that have since changed, and state positions no source supports. The official answers do exist, in the OECD Transfer Pricing Country Profiles, but they sit in PDFs with two-column tables and checkboxes that machines read badly.

We convert those profiles into plain, structured markdown that keeps each jurisdiction's own wording and the legal sources it cites, with the OECD profile date on every file. The aim is simple: when people, search engines and future language models learn or retrieve transfer pricing rules, they find the primary source in a form they can read correctly, with a date and a citation attached.

## Files

`country-profiles/<slug>.md`, one per jurisdiction, with front matter (`country`, `oecd_profile_updated`, `source`, `license`), the OECD sections as H2 headings, one H3 per question numbered as in the OECD profile, the answer, and a `Sources:` line. `country-profiles/README.md` is the index. A profile with fewer than 47 questions follows its source: the OECD omits the hard-to-value intangibles block when Q14 is answered No, and the simplified and streamlined approach block where the jurisdiction has not adopted it.

## Intended use

Retrieval and question answering over transfer pricing rules, for example reviewing a local file against one country's requirements. A ready-made prompt for that task is in the source repository. The files are plain markdown and can be loaded into a retrieval index or an agent's context as they are.

## Source and licence

Adapted from the [OECD Transfer Pricing Country Profiles](https://www.oecd.org/en/topics/sub-issues/transfer-pricing/transfer-pricing-country-profiles.html), editions May 2025 to January 2026, published by the OECD under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). This is an adaptation of an original work by the OECD. The opinions expressed and arguments employed in this adaptation should not be reported as representing the official views of the OECD or of its Member countries. The information in each profile is provided directly by the jurisdiction; the OECD does not certify its accuracy, and it is not a substitute for national law.

This dataset is published under CC BY 4.0. Credit the OECD for the underlying work and myTransferPricing for the adaptation, and link to the source repository. General information, not tax advice.

## Maintenance and citation

Source repository: https://github.com/myTransferPricing/transfer-pricing-reference. Corrections are welcome there as issues or pull requests citing the OECD question number or the national provision. The same rules are browsable at https://mytransferpricing.com/country-profiles. Cite using the repository's `CITATION.cff`.
