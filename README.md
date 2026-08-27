# Journal Submission Requirements Dataset

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22134469.svg)](https://doi.org/10.5281/zenodo.22134469)

Normalized submission requirements for **7,239 academic journals**, collected from
each journal's own author guidelines and mapped to fields via
[OpenAlex](https://openalex.org).

Maintained by [Scraiber](https://scraiber.com). Interactive analysis:
**[scraiber.com/journal-statistics](https://scraiber.com/journal-statistics)** ·
Per-journal pages: [scraiber.com/journals](https://scraiber.com/journals)

## What's inside

| File | Rows | Description |
|---|---|---|
| `data/journals.csv` | 7,239 | One row per journal: name, publisher, ISSNs, homepage, OpenAlex id, domain/field/subfield, h-index, citation and work counts, manuscript types, number of tracked requirement rules |
| `data/requirements.csv` | 44,114 | One row per published requirement value: journal slug, manuscript type, category, key (e.g. `word_limit`, `abstract_word_limit`, `reference_limit`), value, unit, source URL |
| `stats/stats.json` | — | Aggregates used on the analysis page: medians, quartiles, histograms, per-field breakdowns |

### Headline numbers (2026-08-27)

- Median article **word limit**: 7,500 words (1,692 journals publish one)
- Median **abstract word limit**: 250 words; 91% of the 4,715 journals with a
  published abstract limit use one of just four values: 150, 200, 250 or 300 words
- Median **reference limit**: 50 references
- Field coverage via OpenAlex: 100% of journals mapped to a primary field
  (26 fields across 4 domains)

## Method

Scraiber collects the author guidelines each journal publishes on its own website
and normalizes them into typed, per-manuscript-type rules (a superset of this
dataset powers [Scraiber's](https://scraiber.com) manuscript reformatting). This
export contains the published subset: journal metadata plus numeric limits and
normalized token values, each with its source URL. Free-text prose from publisher
pages is not included. Fields and domains come from matching each journal's ISSNs
to its OpenAlex source record and taking the field of its primary topic.

Requirement `category` values: `LENGTH`, `CITATION`, `FIGURE`, `TABLE`,
`POLICY`, `OTHER`. Published values are numeric limits with a `unit`.

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free to share and
adapt with attribution. Please cite Scraiber and link to
<https://scraiber.com/journal-statistics>.

## Citation

> Scraiber (2026). Journal Submission Requirements Dataset.
> https://doi.org/10.5281/zenodo.22134469

See `CITATION.cff` for machine-readable citation metadata.
