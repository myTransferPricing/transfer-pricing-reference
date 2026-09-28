# Transfer pricing reference: OECD guidelines, country rules and methods

Plain-markdown reference material on transfer pricing, written to be read by people and by AI agents. Everything here is built from primary sources, mainly the OECD Transfer Pricing Guidelines and the OECD transfer pricing country profiles, and is free to reuse under the CC BY 4.0 licence.

Maintained by the team behind [myTransferPricing](https://mytransferpricing.com), an AI-first transfer pricing platform for in-house tax teams and advisory firms.

## What is here

| Folder | Contents | Primary source |
|---|---|---|
| `oecd-guidelines/` | Chapter-by-chapter explanations of the OECD Transfer Pricing Guidelines for Multinational Enterprises and Tax Administrations (2022 edition) | [OECD Transfer Pricing Guidelines](https://www.oecd.org/en/publications/oecd-transfer-pricing-guidelines-for-multinational-enterprises-and-tax-administrations-2022_0e655865-en.html) |
| `country-profiles/` | Country-by-country rules: arm's length principle, methods, documentation thresholds, penalties and deadlines | [OECD transfer pricing country profiles](https://www.oecd.org/en/topics/sub-issues/transfer-pricing/transfer-pricing-country-profiles.html) |
| `methods/` | Step-by-step guides to benchmarking, the arm's length range and the interquartile range | OECD Guidelines, Chapter III |
| `checklists/` | Master file and local file documentation checklists (BEPS Action 13) | OECD Guidelines, Chapter V |
| `prompts/` | Prompts and instructions for using AI agents on transfer pricing work | Our own practice |

Folders are added as material is published. An empty folder means the material is still being written.

## Where the country information comes from

Every country page is summarised from that country's entry in the OECD transfer pricing country profiles, which each tax administration completes and the OECD publishes. Where a page adds a local-law detail that is not in the profile, the page cites the national source. Profiles are updated by the OECD on a rolling basis, so each page states the profile date it was summarised from.

The same country rules are available in a browsable form at [mytransferpricing.com/country-profiles](https://mytransferpricing.com/country-profiles).

## Free tools

Two free tools apply the methods described here, with no signup:

- [Arm's length range generator](https://mytransferpricing.com/tools/arm-length-range) computes quartiles from a set of comparables and exports to Word.
- [Transfer pricing documentation checklist](https://mytransferpricing.com/tools/tp-documentation-checklist) covers the BEPS Action 13 master file and local file contents by role.

## Using this with an AI agent

The files are plain markdown with no front matter beyond a title and source line, so they can be dropped into a context window, a retrieval index or an agent's skills folder as they are. When you cite them, cite the primary OECD source named at the top of each file as well.

## Contributing

Corrections are welcome as pull requests. Cite the OECD paragraph, the country profile question number or the national law article that supports the change.

## Licence

[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You may copy, adapt and redistribute this material, including commercially, as long as you credit myTransferPricing and link back to this repository.

This material is general information, not tax advice. Check the current OECD text and national law before relying on it.
