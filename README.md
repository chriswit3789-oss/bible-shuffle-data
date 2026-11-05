# My Bible Shuffle — open language and history data

Structured bible-language data for the My Bible Shuffle iOS app.

## Contents

- `verses/<Book>.json` — every verse of that book, tokenized into original-language words
- `lexicon_hebrew.json` — Strong's Hebrew and Aramaic dictionary entries keyed by H-number
- `lexicon_greek.json` — Strong's Greek dictionary entries keyed by G-number
- `books.json` — book-level context: author, date, audience, place, genre, summary

## Verse file format

```json
{
  "book": "Jhn",
  "v": {
    "Jhn.3.16": [
      { "s": "G3779", "w": "ουτως", "t": "houtos", "g": "Thus", "m": "ADV" }
    ]
  }
}
```

- `s` Strong's number, `w` original-language word, `t` transliteration,
  `g` a short English gloss for that word in that verse, `m` morphology code

## Sources and licensing

- Hebrew and Greek tagged text: STEPBible.org, Translators Amalgamated Hebrew OT and
  Greek NT, CC BY 4.0. Reformatting into per-book JSON is permitted by that license.
- Strong's dictionaries: Open Scriptures, derived from Strong's Exhaustive Concordance
  (1890) and Hebrew dictionary (1894), CC-BY-SA.
- Book context records: written for this app, neutral descriptive summaries.

Attribution required: "Language data from STEPBible.org (CC BY 4.0) and Open Scriptures
Strong's dictionaries (CC-BY-SA)."
