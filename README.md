# Mapping Thirty Years of Author Trajectories at CSCL (1995–2026)

Data and analysis code for the paper *Mapping Thirty Years of Author Trajectories at CSCL (1995–2026)*


## Dataset at a glance

| | |
| :- | :- |
| Conferences | 19 CSCL conferences, 1995–2026 |
| Papers | 2,419 |
| Authorships | 8,800 |
| Unique authors | 4,441 |
| Included paper types | [TODO: e.g., long, short, symposium, poster] |

## Data sources

- **ISLS Repository** (https://repository.isls.org/): bibliographic records and PDFs for all conferences except 2003. PDFs were downloaded on [TODO: date].
- **Springer**: records for the 2003 proceedings, which were published as a book (Wasson et al., 2003).
- **DBLP**: [TODO: describe use, e.g., author identifiers and session headings used to supplement track labels].

## Processing pipeline

1. **Collect records.** Scrape paper titles, authors and links from each conference's ISLS Repository collection, following pagination.
2. **Download PDFs.** Resolve the file path for each paper and download its PDF. The 2003 proceedings PDF is split into individual papers.
3. **Normalize names.** Standardize author names and institutions. [TODO: describe disambiguation rules and spot-check error rate.]
4. **Extract paper features.** Parse each PDF for page length.
5. **Map affiliations.** Map author institutions to countries and countries to world regions.
6. **Build networks.** Convert the author–paper table into co-authorship graph data.

## Repository structure

[TODO: replace with the actual layout]

```
data/
  raw/            # scraped records and source files
  processed/      # cleaned author–paper table, country/region mappings
  graphs/         # co-authorship network files
scripts/          # collection, cleaning and analysis scripts
figures/          # figures reported in the paper
```

## Limitations

- Track labels in the ISLS Repository are incomplete; [TODO: describe how post-2021 CSCL papers were identified].
- Author matching may miss name changes or merge different people with the same name.
- Participation is measured through authorship only, not attendance, reviewing or committee service.

## License

[TODO: e.g., code under MIT, data under CC BY 4.0]

## Citation

[TODO: add after review]
