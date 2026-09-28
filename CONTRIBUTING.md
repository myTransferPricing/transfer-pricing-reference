# Contributing

Corrections and additions are welcome. The bar is the same for both: every claim must trace to a primary source.

## Report an error

Open an issue with the file name, the question number (for country profiles) and the source that shows the correct position: the OECD paragraph, the country profile question, or the national provision with a link. A report without a source is closed with a request for one.

## Propose a change

1. Fork the repository and branch from `main`.
2. Edit the markdown. Keep the file's structure: front matter, sections as H2, one H3 per question, answer, then a `Sources:` line.
3. If the change comes from a newer OECD profile, update `oecd_profile_updated` in the front matter and the date in the "Source and licence" section.
4. Open a pull request with one change per pull request and a title that says what changed and why, written for a reader who will see it in the public history.

## Add a country

Convert the jurisdiction's OECD Transfer Pricing Country Profile PDF into the same structure as an existing file, for example `country-profiles/germany.md`. Preserve the jurisdiction's wording; fix only extraction artefacts. Record the PDF's "Updated" month in the front matter. Add the row to `country-profiles/README.md`.

## Licence

By contributing you agree that your contribution is published under [CC BY 4.0](./LICENSE), with attribution to the OECD for the underlying material where it applies.
