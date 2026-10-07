# Vaakhu (വാക്ക്)

Offline lexical analysis and qualitative coding for Malayalam, Manglish and English text.

**Open the app:** https://sachinrajeevcodes.github.io/Vaakhu/

Vaakhu is a single-page tool for researchers working with open-ended survey answers and interview transcripts in Malayalam, in Malayalam typed in English letters (Manglish), and in English. It combines corpus-style lexical analysis with a qualitative coding workspace, and it runs entirely in your browser.

It was built for a doctoral study on alcohol addiction and its portrayal in Malayalam cinema. That study needed tools that handle Malayalam word endings, mixed-language answers and responses collected both online and on paper.

## Your data stays on your device

- Vaakhu makes no network requests. Nothing you import or type is uploaded anywhere.
- Your project is saved in your browser's local storage on the device you are using.
- Use **Save project** to keep a backup file, and to move your work between devices.
- Exported files contain your research data, so store them as your ethics approval requires.

## Getting started

**Online:** open the link above in Chrome, Edge or Safari. On a phone, use Share → Add to Home Screen to get an app icon.

**Offline:** download `index.html` and open it in Chrome or Edge on your computer.

File previews, such as the iPhone Files app, switch JavaScript off and cannot run Vaakhu. Open it in a browser instead.

To explore before importing real data, go to **Responses → Sample data**. It loads twelve made-up answers, example word lists and a small demo codebook.

## Bringing data in

- **Spreadsheets:** import a CSV, for example from Google Sheets (File → Download → Comma-separated values). You choose which columns hold answers, and where the participant ID, group and item come from.
- **Paper forms:** type or paste answers. Ctrl + Enter adds one and keeps the ID, group and item ready for the next.
- **Interview transcripts:** import plain-text (.txt) files, one per interview.

Each answer becomes one response, tagged with a group, item, language and mode (online, paper or transcript). Language is detected automatically and can be corrected by hand.

## Handling Malayalam and Manglish

- **Normalisation:** text is converted to a standard Unicode form, and old-style chillu sequences (for example ന് + zero-width joiner) are treated as the same letter as atomic chillus (ൻ). The same word typed on different keyboards therefore counts once.
- **Word forms:** Malayalam attaches endings to words, so കുടിയൻ, കുടിയന്റെ and കുടിയനെ would otherwise count as three words. Vaakhu suggests likely groupings for Malayalam, Manglish and English endings, and you approve each one.
- **Stopwords:** separate editable lists for English, Malayalam and Manglish. Negations (no, not, ഇല്ല, അല്ല, illa, alla) are left off on purpose, because they matter when reading attitudes.

## Lexical analysis

| View | What it does |
| --- | --- |
| Overview | Responses, words, unique words, type-token ratio and standardised type-token ratio (per 100 words) by group |
| Word frequency | Words and 2–4 word phrases, counts per 1,000 words by group, as a table, chart or word cloud |
| Concordance | Every occurrence of a search term in context. Supports `*` and `?` wildcards, alternatives with `\|`, regular expressions, a "nearby word" filter and sorting by neighbouring words |
| Collocates | Words that occur near a search term, ranked by logDice, mutual information, T-score or log-likelihood |
| Keyness | Words one group, language, item or mode uses more or less than another, with log-likelihood significance and log ratio |
| Word lists | Your own categories of terms (for example words for a feeling, a stance or a topic) counted by group. Four general example lists are included |
| Dispersion | Where a term appears across responses, with DP and normalised DP |
| Co-occurrence | How often chosen terms appear together in a response, a sentence or a window of words |

## Qualitative coding

| View | What it does |
| --- | --- |
| Coding workspace | Select words in a response and apply codes. Keys 1–9 apply codes, and `[` `]` move between responses. Star essential passages, add memos to passages, and write a wholistic statement for each response. A line-by-line mode supports detailed reading |
| Codebook | Themes and codes with definitions, include and exclude rules and example quotes. Merge or delete codes, and import or export the codebook as CSV |
| Coded segments | All passages for a code or theme side by side, filterable to essential passages |
| Code analysis | Codes by group (passages, % of responses, or passages per response) and a code co-occurrence matrix |
| Memos & journal | Dated analytic memos and a reflexive journal, plus all wholistic statements in one place |

The wholistic, selective and line-by-line views follow van Manen's three approaches to isolating themes in hermeneutic phenomenology.

## Exports

Every table and list downloads as a UTF-8 CSV that opens in Excel with Malayalam intact. The whole project, including responses, codes, passages, memos, word lists and settings, saves as a single JSON file.

## Statistics used

- **Normalised frequency:** occurrences per 1,000 words.
- **Log-likelihood (G²):** Dunning (1993), applied to corpus comparison following Rayson and Garside (2000). Critical values: 3.84 (p < .05), 6.63 (p < .01), 10.83 (p < .001), 15.13 (p < .0001).
- **Log ratio:** the binary log of the ratio of relative frequencies (Hardie, 2014).
- **Collocation:** mutual information, T-score, log-likelihood and logDice (Rychlý, 2008).
- **Dispersion:** deviation of proportions, DP (Gries, 2008).

With small samples, treat every statistic as a pointer to read the passages, not as proof.

## Limitations

- Word-form grouping uses suggested suffix rules. Check each suggestion, since endings can mislead.
- Manglish spelling varies widely, so counts for Manglish text undercount.
- Vaakhu is single-user. Inter-coder agreement (Cohen's kappa) is not yet built in.
- Browser storage is limited (often around 5 MB). For large projects, rely on **Save project** files.

## Planned

- Optional AI-assisted coding suggestions, for de-identified text only and where participant consent allows
- Cohen's kappa for agreement between coders, or between a coder and AI suggestions

## How to cite

Rajeev, S. (2026). *Vaakhu: Offline lexical analysis and qualitative coding for Malayalam, Manglish and English* [Computer software]. https://github.com/sachinrajeevcodes/Vaakhu

## References

- Dunning, T. (1993). Accurate methods for the statistics of surprise and coincidence. *Computational Linguistics, 19*(1), 61–74.
- Gries, S. Th. (2008). Dispersions and adjusted frequencies in corpora. *International Journal of Corpus Linguistics, 13*(4), 403–437.
- Hardie, A. (2014). *Log Ratio: An informal introduction*. ESRC Centre for Corpus Approaches to Social Science (CASS), Lancaster University.
- Rayson, P., & Garside, R. (2000). Comparing corpora using frequency profiling. In *Proceedings of the Workshop on Comparing Corpora* (pp. 1–6). Association for Computational Linguistics.
- Rychlý, P. (2008). A lexicographer-friendly association score. In *Proceedings of Recent Advances in Slavonic Natural Language Processing (RASLAN 2008)* (pp. 6–9).
- van Manen, M. (1990). *Researching lived experience: Human science for an action sensitive pedagogy*. State University of New York Press.

## Author

Sachin Rajeev
