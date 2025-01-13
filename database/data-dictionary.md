# Data Dictionary
The following is a AI back translation of the data in the sotrage lay compiled by ChatGpt and manual efforts. It needs to be reviewed and updated for accuracy. 

**Table of Contents**  

- [Data Dictionary](#data-dictionary)
  - [**Table name is `quran-data`**](#table-name-is-quran-data)
  - [**Table name is `formula-list`**](#table-name-is-formula-list)
  - [**Table name is `formula-id-codes-linked-global-words`**](#table-name-is-formula-id-codes-linked-global-words)
  - [**Table name is `formula-archetype-list-lower`**](#table-name-is-formula-archetype-list-lower)
  - [**Table name is `quran-translation`**](#table-name-is-quran-translation)
  - [**Table name is `exact-arabic-list`**](#table-name-is-exact-arabic-list)
  - [**Table name is `exact-transliteration-list`**](#table-name-is-exact-transliteration-list)
  - [**Table name is `quran-verse-endings`**](#table-name-is-quran-verse-endings)
  - [**Table name is `formulaic-glosses`**](#table-name-is-formulaic-glosses)
  - [**Table name is `lemma-list`**](#table-name-is-lemma-list)
  - [**Table name is `quran-full-parse`**](#table-name-is-quran-full-parse)
  - [**Table name is `dictionary-entries`**](#table-name-is-dictionary-entries)
  - [**Table name is `root-list`**](#table-name-is-root-list)
  - [**Table name is `sura-data`**](#table-name-is-sura-data)
  - [**Table name is `intertextual links`**](#table-name-is-intertextual-links)
  - [**Table name is `proper-noun-list`**](#table-name-is-proper-noun-list)
  - [**Table name is `stats-suras`**](#table-name-is-stats-suras)
  - [**Table name is `buckwalter-encoding`**](#table-name-is-buckwalter-encoding)
  - [**Table name is `help-page-links`**](#table-name-is-help-page-links)
  - [**Table name is `intertextual sources`**](#table-name-is-intertextual-sources)
  - [**Table name is `tooltip-text`**](#table-name-is-tooltip-text)
  - [**Table name is `quick-tips`**](#table-name-is-quick-tips)
  - [**Table name is `failed-searches`**](#table-name-is-failed-searches)
  - [**Table name is `usage`**](#table-name-is-usage)
  - [**Table name is `render-formulaic-density-summaries`**](#table-name-is-render-formulaic-density-summaries)
  - [**Table name is `translation-list`**](#table-name-is-translation-list)
  - [**Table name is `usage-verses-searches`**](#table-name-is-usage-verses-searches)
  - [**Table name is `login-logs`**](#table-name-is-login-logs)
  - [**Table name is `users`**](#table-name-is-users)
  - [**Table name is `transliteration-exceptions`**](#table-name-is-transliteration-exceptions)
- [Empty Tables that need more information](#empty-tables-that-need-more-information)
  - [**Table name is `tags`**](#table-name-is-tags)
  - [**Table name is `messages`**](#table-name-is-messages)
  - [**Table name is `tagged-verses`**](#table-name-is-tagged-verses)
  - [**Table name is `bookmarks`**](#table-name-is-bookmarks)
  - [**Table name is `history`**](#table-name-is-history)



## **Table name is `quran-data`**
The `quran-data` table represents the foundational dataset for the Qur'an, including information about its verses, chapters (suras), and textual structure. It provides the original Arabic text and metadata such as verse numbering, chapter information, and divisions of the text for both analysis and display purposes. Each entry corresponds to a single verse, forming the backbone of Qur'anic data management.

### Analysis of the `quran-data` Table

The `quran-data` table provides granular information about each word in the Qur'an, broken down into linguistic, grammatical, and semantic categories. Each field serves a specific role in capturing the nuances of the Qur'anic text. Below is the analysis with uniquely described fields.

---

| **Table Name**  | **Field Name**               | **Description**                                                                                                                                             |
|------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `quran-data`     | `RECORD NUMBER`            | A unique identifier for each record in the table, representing a specific word within a verse.                                                              |
| `quran-data`     | `LOCATION`                 | The hierarchical location of the word in the format `(Sura:Verse:Word:Segment)`.                                                                             |
| `quran-data`     | `SURA-VERSE`               | The reference to the Sura and Verse in which the word is located.                                                                                           |
| `quran-data`     | `SURA`                     | The chapter (Sura) number of the Qur'an where the word appears.                                                                                              |
| `quran-data`     | `VERSE`                    | The verse number within the specified Sura.                                                                                                                |
| `quran-data`     | `WORD`                     | The position of the word within the verse.                                                                                                                  |
| `quran-data`     | `SEGMENT`                  | The segment number within the word, useful for compound or multi-part words.                                                                                |
| `quran-data`     | `GLOBAL WORD NUMBER`       | A unique global identifier for each word in the Qur'an, across all Suras and verses.                                                                        |
| `quran-data`     | `CHANGES AFFECTING WORD`   | The number of manuscript changes or corrections affecting the word.                                                                                         |
| `quran-data`     | `FORM`                     | The grammatical form or type of the word, such as prefix, suffix, or stem.                                                                                  |
| `quran-data`     | `TRANSLITERATED`           | A phonetic transliteration of the word into Latin script.                                                                                                   |
| `quran-data`     | `RENDERED ARABIC`          | The word in its rendered Arabic script form.                                                                                                                |
| `quran-data`     | `TAG`                      | A short tag describing the word's role (e.g., CONJ for conjunction).                                                                                        |
| `quran-data`     | `TAG EXPLAINED`            | A detailed explanation of the tag, providing context about the word's grammatical role.                                                                     |
| `quran-data`     | `FEATURES`                 | Additional linguistic features, such as case, mood, or part of speech, concatenated as a string.                                                            |
| `quran-data`     | `PART OF WORD`             | Indicates whether the word is part of a compound or multi-part construction.                                                                                |
| `quran-data`     | `CASES`                    | The grammatical case of the word (e.g., nominative, accusative, genitive).                                                                                  |
| `quran-data`     | `GENDER`                   | The gender of the word (e.g., masculine, feminine, or neuter).                                                                                              |
| `quran-data`     | `PERSON`                   | The grammatical person of the word (e.g., first, second, or third person).                                                                                  |
| `quran-data`     | `NUMBER`                   | Indicates whether the word is singular, dual, or plural.                                                                                                    |
| `quran-data`     | `ROUGH TRANSLATION`        | A rough English translation of the word.                                                                                                                   |
| `quran-data`     | `ROOT`                     | The root letters of the word in Arabic.                                                                                                                     |
| `quran-data`     | `LEMMA`                    | The base form (lemma) of the word in Arabic.                                                                                                                |
| `quran-data`     | `PARSED FLAG`              | Indicates whether the word has been parsed and tagged for grammatical analysis.                                                                              |
| `quran-data`     | `QTL-PART-OF-WORD`         | Specifies if the word is part of a Quranic textual lemma.                                                                                                   |
| `quran-data`     | `QTL-TAG-EXPLAINED`        | Explains the tag in Quranic Text Lemma (QTL) terms.                                                                                                         |
| `quran-data`     | `QTL-LEMMA`                | The Quranic Text Lemma form of the word.                                                                                                                   |
| `quran-data`     | `QTL-LEMMA-BINARY`         | Binary-encoded representation of the Quranic Text Lemma.                                                                                                   |
| `quran-data`     | `QTL-LEMMA-TRANSLITERATED` | Transliterated form of the Quranic Text Lemma.                                                                                                             |
| `quran-data`     | `QTL-ROOT`                 | The Quranic Text Root of the word.                                                                                                                         |
| `quran-data`     | `QTL-ROOT-BINARY`          | Binary-encoded representation of the Quranic Text Root.                                                                                                    |
| `quran-data`     | `QTL-ROOT-TRANSLITERATED`  | Transliterated form of the Quranic Text Root.                                                                                                              |
| `quran-data`     | `QTL-SPECIAL-WORD-GROUP`   | Indicates if the word belongs to a specific Quranic word group.                                                                                            |
| `quran-data`     | `QTL-GENDER`               | The Quranic Text Lemma gender of the word.                                                                                                                 |
| `quran-data`     | `QTL-CASE`                 | The grammatical case for Quranic Text Lemma.                                                                                                               |
| `quran-data`     | `QTL-NUMBER`               | The grammatical number for Quranic Text Lemma.                                                                                                             |
| `quran-data`     | `QTL-PERSON`               | The grammatical person for Quranic Text Lemma.                                                                                                             |
| `quran-data`     | `QTL-VOICE`                | Indicates active or passive voice in Quranic Text Lemma.                                                                                                   |
| `quran-data`     | `QTL-DERIVED-NOUN-TYPE`    | Specifies if the noun is derived and its type in Quranic Text Lemma.                                                                                       |
| `quran-data`     | `QTL-ARABIC-FORM`          | The Arabic form of the Quranic Text Lemma.                                                                                                                 |
| `quran-data`     | `QTL-NOUN-STATE`           | Specifies the state of the noun (e.g., definite or indefinite).                                                                                            |
| `quran-data`     | `QTL-MOOD`                 | The grammatical mood of the word (e.g., indicative, subjunctive).                                                                                           |
| `quran-data`     | `ROOT OR PARTICLE`         | Indicates whether the word is a root or particle.                                                                                                          |
| `quran-data`     | `GLOSS`                    | A detailed gloss or semantic explanation of the word.                                                                                                      |
| `quran-data`     | `FIXED_ARABIC`             | Corrected Arabic text for the word, if applicable.                                                                                                         |
| `quran-data`     | `FIXED_TRANSLITERATION`    | Corrected transliteration for the word, if applicable.                                                                                                     |
| `quran-data`     | `FIXED_GLOSS`              | Corrected gloss for the word, if applicable.                                                                                                               |
| `quran-data`     | `FIXED_DB_APPROVED`        | Indicates if the fixed entries have been approved for database use.                                                                                        |
| `quran-data`     | `PREVIOUS ARABIC`          | The Arabic text before any corrections were applied.                                                                                                       |
| `quran-data`     | `PREVIOUS TRANSLITERATION` | The transliteration before any corrections were applied.                                                                                                   |
| `quran-data`     | `TRANSLITERATION FIX APPLIED` | Indicates whether a transliteration fix was applied.                                                                                                       |
| `quran-data`     | `FIXED_NOTES`              | Notes explaining the corrections made.                                                                                                                     |
| `quran-data`     | `FIX_CREATED_BY`           | The user or system responsible for creating the fix.                                                                                                       |
| `quran-data`     | `FIX_APPROVED_BY`          | The user or system responsible for approving the fix.                                                                                                      |
| `quran-data`     | `FIX_CHANGES_SUGGESTED`    | Indicates if changes were suggested for review.                                                                                                            |
| `quran-data`     | `AJC FOREIGN WORD`         | Indicates foreign or borrowed words within the Quranic text.                                                                                               |

---

### Key Insights

1. **Comprehensive Linguistic Analysis**:
   - The `quran-data` table serves as a foundational resource for linguistic studies, capturing granular details about each word's grammatical, phonetic, and semantic properties.
   - Features like `ROOT`, `LEMMA`, and `PARSED FLAG` enable precise morphological and syntactic parsing.

2. **Advanced Parsing Features**:
   - The inclusion of `QTL-*` fields offers specialized metadata for Quranic Text Lemmas, emphasizing the contextual use of words in the Qur'anic corpus.
   - Fields like `TRANSLITERATION FIX APPLIED` and `FIXED_NOTES` ensure data integrity and traceability of corrections.

3. **Interdisciplinary Utility**:
   - This table supports multiple disciplines, including computational linguistics, textual criticism, and comparative theology.

---

### Example Interpretation of Data

#### Row Example:
| **FIELD**       | **VALUE**                     |
|------------------|-------------------------------|
| RECORD NUMBER    | `127719`                     |
| LOCATION         | `(100:10:1:2)`               |
| SURA-VERSE       | `100:10`                     |
| TRANSLITERATED   | `wa-ḥuṣṣila`                 |
| RENDERED ARABIC  | `وَحُصِّلَ`                  |
| TAG              | `V`                          |
| TAG EXPLAINED    | `Verb`                       |
| ROOT             | `HSl`                        |
| ROUGH TRANSLATION| `And is made apparent`       |

#### Interpretation:
This record represents a verb (`TAG: V`) in Sura 100, Verse 10. The verb, transliterated as `wa-ḥuṣṣila`, is rendered in Arabic as `وَحُصِّلَ` and stems from the root `HSl`. The root indicates the semantic concept of something being "gathered" or "made apparent," contextualized in this verse as an action. The word is part of a passive voice construction (`PERSON: 3`, `VOICE: Passive`) and carries significant theological implications in the context of divine judgment.

---

### Contextual Significance

1. **Textual Criticism**:
   - Fields like `CHANGES AFFECTING WORD` and `PREVIOUS ARABIC` document manuscript variations, crucial for analyzing the textual history of the Qur'an.

2. **Linguistic Semantics**:
   - The table facilitates semantic analysis of Qur'anic language by linking words to their roots, lemmas, and glosses.

3. **Thematic Analysis**:
   - By examining `FORMULA-*` fields, researchers can identify recurring themes and formulaic structures, shedding light on the Qur'an's rhetorical strategies.

4. **Cross-Linguistic Comparisons**:
   - Transliteration and transliteration fixes allow for accurate phonetic representations, enabling comparative studies between Arabic and other languages.

5. **Machine Learning and NLP**:
   - The structured data can train models for natural language processing tasks, such as part-of-speech tagging, lemmatization, or translation.

---

### First 10 Rows Example (2025-01-14)
|   RECORD NUMBER | LOCATION     | SURA-VERSE   |   SURA |   VERSE |   WORD |   SEGMENT |   GLOBAL WORD NUMBER |   CHANGES AFFECTING WORD | FORM     | TRANSLITERATED   | RENDERED ARABIC   | TAG   | TAG EXPLAINED            | FEATURES                                           | PART OF WORD   | CASES      |   GENDER |   PERSON |   NUMBER | Rough Translation   |   ROOT |   LEMMA |   Parsed Flag | QTL-PART-OF-WORD   | QTL-TAG-EXPLAINED             | QTL-LEMMA   | QTL-LEMMA-BINARY                                             | QTL-LEMMA-TRANSLITERATED   | QTL-ROOT   | QTL-ROOT-BINARY      | QTL-ROOT-TRANSLITERATED   | QTL-SPECIAL-WORD-GROUP   | QTL-GENDER   | QTL-CASE   | QTL-NUMBER   |   QTL-PERSON | QTL-VOICE   |   QTL-DERIVED-NOUN-TYPE | QTL-ARABIC-FORM   |   QTL-NOUN-STATE |   QTL-MOOD |   FORMULA-2-ROOT |   FORMULA-3-ROOT |   F3-ROOT-QTL-ROOT-FLAG |   FORMULA-4-ROOT |   FORMULA-5-ROOT |   FORMULA-3-ROOT-ALL |   FORMULA-4-ROOT-ALL |   FORMULA-5-ROOT-ALL |   FORMULA-3-LEMMA |   FORMULA-4-LEMMA |   FORMULA-5-LEMMA |   FORMULA-3-ANY |   FORMULA-4-ANY |   FORMULA-5-ANY | ROOT OR PARTICLE   | GLOSS                     |   FIXED_ARABIC |   FIXED_TRANSLITERATION |   FIXED_GLOSS | FIXED_DB_APPROVED   |   PREVIOUS ARABIC | PREVIOUS TRANSLITERATION   | TRANSLITERATION FIX APPLIED   |   FIXED_NOTES |   FIX_CREATED_BY |   FIX_APPROVED_BY |   FIX_CHANGES_SUGGESTED |   AJC FOREIGN WORD |
|----------------:|:-------------|:-------------|-------:|--------:|-------:|----------:|---------------------:|-------------------------:|:---------|:-----------------|:------------------|:------|:-------------------------|:---------------------------------------------------|:---------------|:-----------|---------:|---------:|---------:|:--------------------|-------:|--------:|--------------:|:-------------------|:------------------------------|:------------|:-------------------------------------------------------------|:---------------------------|:-----------|:---------------------|:--------------------------|:-------------------------|:-------------|:-----------|:-------------|-------------:|:------------|------------------------:|:------------------|-----------------:|-----------:|-----------------:|-----------------:|------------------------:|-----------------:|-----------------:|---------------------:|---------------------:|---------------------:|------------------:|------------------:|------------------:|----------------:|----------------:|----------------:|:-------------------|:--------------------------|---------------:|------------------------:|--------------:|:--------------------|------------------:|:---------------------------|:------------------------------|--------------:|-----------------:|------------------:|------------------------:|-------------------:|
|          127718 | (100:10:1:1) | 100:10       |    100 |      10 |      1 |         1 |                77109 |                        0 | wa       | wa-?u??ila       | ?????????         | CONJ  | Coordinating Conjunction | PREFIX|w:CONJ+                                     | Prefix         | nan        |      nan |      nan |      nan | test                |    nan |     nan |             8 | Prefix             | Coordinating Conjunction (wa) | nan         | \0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0 | nan                        | nan        | \0\0\0\0\0\0\0\0\0\0 | nan                       | nan                      | nan          | nan        | nan          |            0 | nan         |                     nan | nan               |              nan |        nan |                0 |                0 |                       0 |                0 |                0 |                    0 |                    0 |                    0 |                 0 |                 0 |                 0 |               0 |               0 |               0 | nan                | And is made apparent      |            nan |                     nan |           nan | Y                   |               nan | nan                        | N                             |           nan |                0 |                 1 |                     nan |                nan |
|          127719 | (100:10:1:2) | 100:10       |    100 |      10 |      1 |         2 |                77109 |                        0 | HuS~ila  | wa-?u??ila       | ?????????         | V     | Verb                     | STEM|POS:V|PERF|PASS|(II)|LEM:HuS~ila|ROOT:HSl|3MS | Stem           | nan        |      nan |      nan |      nan | nan                 |    nan |     nan |             8 | Stem               | Perfect Verb                  | HuS~ila     | HuS~ila\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0        | ?u?~ila                    | HSl        | HSl\0\0\0\0\0\0\0    | ??l                       | nan                      | Masculine    | nan        | Singular     |            3 | Passive     |                     nan | II                |              nan |        nan |                0 |                0 |                       0 |                0 |                0 |                    0 |                    0 |                    0 |                 0 |                 0 |                 0 |               0 |               0 |               0 | HSl                | And is made apparent      |            nan |                     nan |           nan | Y                   |               nan | nan                        | N                             |           nan |                0 |                 1 |                     nan |                nan |
|          127720 | (100:10:2:1) | 100:10       |    100 |      10 |      2 |         1 |                77110 |                        0 | maA      | m?               | ???               | REL   | Relative Pronoun         | STEM|POS:REL|LEM:maA                               | Stem           | nan        |      nan |      nan |      nan | nan                 |    nan |     nan |             8 | Stem               | Relative Pronoun              | maA         | maA\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0    | ma'                        | nan        | \0\0\0\0\0\0\0\0\0\0 | nan                       | nan                      | nan          | nan        | nan          |            0 | nan         |                     nan | nan               |              nan |        nan |                0 |                0 |                       0 |                0 |                0 |                    0 |                    0 |                    0 |                 1 |                 0 |                 0 |               1 |               0 |               0 | PORP               | (as)                      |            nan |                     nan |           nan | Y                   |               nan | nan                        | N                             |           nan |                0 |                 1 |                     nan |                nan |
|          127721 | (100:10:3:1) | 100:10       |    100 |      10 |      3 |         1 |                77111 |                        0 | fiY      | f?               | ???               | P     | Particle-Preposition     | STEM|POS:P|LEM:fiY                                 | Stem           | nan        |      nan |      nan |      nan | nan                 |    nan |     nan |             8 | Stem               | Particle-Preposition          | fiY         | fiY\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0    | fiY                        | nan        | \0\0\0\0\0\0\0\0\0\0 | nan                       | nan                      | nan          | nan        | nan          |            0 | nan         |                     nan | nan               |              nan |        nan |                0 |                0 |                       0 |                0 |                0 |                    0 |                    0 |                    0 |                 1 |                 0 |                 0 |               1 |               0 |               0 | PORP               | in                        |            nan |                     nan |           nan | Y                   |               nan | nan                        | N                             |           nan |                0 |                 1 |                     nan |                nan |
|          127722 | (100:10:4:1) | 100:10       |    100 |      10 |      4 |         1 |                77112 |                        0 | {l       | l-?ud?ri         | ??????????        | DET   | Definite Article         | PREFIX|Al+                                         | Prefix         | nan        |      nan |      nan |      nan | nan                 |    nan |     nan |             8 | Prefix             | Definite Article              | nan         | \0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0 | nan                        | nan        | \0\0\0\0\0\0\0\0\0\0 | nan                       | nan                      | nan          | nan        | nan          |            0 | nan         |                     nan | nan               |              nan |        nan |                0 |                0 |                       0 |                0 |                0 |                    0 |                    0 |                    0 |                 1 |                 0 |                 0 |               1 |               0 |               0 | nan                | of what is in the breasts |            nan |                     nan |           nan | Y                   |               nan | nan                        | N                             |           nan |                0 |                 1 |                     nan |                nan |
|          127723 | (100:10:4:2) | 100:10       |    100 |      10 |      4 |         2 |                77112 |                        0 | S~uduwri | l-?ud?ri         | ??????????        | N     | Noun                     | STEM|POS:N|LEM:Sador|ROOT:Sdr|MP|GEN               | Stem           | Genitive   |      nan |      nan |      nan | nan                 |    nan |     nan |             8 | Stem               | Noun                          | Sador       | Sador\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0      | ?ador                      | Sdr        | Sdr\0\0\0\0\0\0\0    | ?dr                       | nan                      | Masculine    | Genitive   | Plural       |            0 | nan         |                     nan | nan               |              nan |        nan |                0 |                0 |                       0 |                0 |                0 |                    0 |                    0 |                    0 |                 1 |                 0 |                 0 |               1 |               0 |               0 | Sdr                | of what is in the breasts |            nan |                     nan |           nan | Y                   |               nan | nan                        | N                             |           nan |                0 |                 1 |                     nan |                nan |
|          127724 | (100:11:1:1) | 100:11       |    100 |      11 |      1 |         1 |                77113 |                        0 | <in~a    | inna             | ?????             | ACC   | Accusative Particle      | STEM|POS:ACC|LEM:<in~|SP:<in~                      | Stem           | Accusative |      nan |      nan |      nan | nan                 |    nan |     nan |             8 | Stem               | Accusative Particle           | <in~        | <in~\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0     | <in~                       | nan        | \0\0\0\0\0\0\0\0\0\0 | nan                       | <in~                     | nan          | nan        | nan          |            0 | nan         |                     nan | nan               |              nan |        nan |                0 |                0 |                       0 |                0 |                0 |                    0 |                    0 |                    0 |                 0 |                 0 |                 0 |               0 |               0 |               0 | PORP               | indeed                    |            nan |                     nan |           nan | Y                   |               nan | 'inna                      | N                             |           nan |                0 |                 1 |                     nan |                nan |
|          127725 | (100:11:2:1) | 100:11       |    100 |      11 |      2 |         1 |                77114 |                        0 | rab~a    | rabbahum         | ????????          | N     | Noun                     | STEM|POS:N|LEM:rab~|ROOT:rbb|M|ACC                 | Stem           | Accusative |      nan |      nan |      nan | nan                 |    nan |     nan |             8 | Stem               | Noun                          | rab~        | rab~\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0     | rab~                       | rbb        | rbb\0\0\0\0\0\0\0    | rbb                       | nan                      | Masculine    | Accusative | Singular     |            0 | nan         |                     nan | nan               |              nan |        nan |                0 |                0 |                       0 |                0 |                0 |                    0 |                    0 |                    0 |                 0 |                 0 |                 0 |               0 |               0 |               0 | rbb                | their Lord                |            nan |                     nan |           nan | Y                   |               nan | nan                        | N                             |           nan |                0 |                 1 |                     nan |                  1 |
|          127726 | (100:11:2:2) | 100:11       |    100 |      11 |      2 |         2 |                77114 |                        0 | hum      | rabbahum         | ????????          | PRON  | Personal Pronoun         | SUFFIX|PRON:3MP                                    | Suffix         | nan        |      nan |      nan |      nan | nan                 |    nan |     nan |             8 | Suffix             | Personal Pronoun              | nan         | \0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0 | nan                        | nan        | \0\0\0\0\0\0\0\0\0\0 | nan                       | nan                      | Masculine    | nan        | Plural       |            3 | nan         |                     nan | nan               |              nan |        nan |                0 |                0 |                       0 |                0 |                0 |                    0 |                    0 |                    0 |                 0 |                 0 |                 0 |               0 |               0 |               0 | nan                | their Lord                |            nan |                     nan |           nan | Y                   |               nan | nan                        | N                             |           nan |                0 |                 1 |                     nan |                nan |
|          127727 | (100:11:3:1) | 100:11       |    100 |      11 |      3 |         1 |                77115 |                        0 | bi       | bihim            | ??????            | P     | Particle-Preposition     | PREFIX|bi+                                         | Prefix         | nan        |      nan |      nan |      nan | nan                 |    nan |     nan |             8 | Prefix             | Particle-Preposition          | nan         | \0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0 | nan                        | nan        | \0\0\0\0\0\0\0\0\0\0 | nan                       | nan                      | nan          | nan        | nan          |            0 | nan         |                     nan | nan               |              nan |        nan |                0 |                0 |                       0 |                0 |                0 |                    0 |                    0 |                    0 |                 0 |                 0 |                 0 |               0 |               0 |               0 | PORP               | them                      |            nan |                     nan |           nan | Y                   |               nan | nan                        | N                             |           nan |                0 |                 1 |                     nan |                nan |

---

## **Table name is `formula-list`**
The `formula-list` table contains a comprehensive catalog of repeated phrases or formulae in the Qur'an. It captures patterns of words or phrases that recur throughout the text and provides details on their frequency, position, and context. This table is essential for identifying formulaic structures used in linguistic, thematic, and rhetorical analyses of the Qur'an.

### **Analysis of the `formula-list` Table**

Below is the detailed description of each field in the `formula-list` table, including the table name as a left-hand column in every row.

---

| **Table Name**   | **Field Name**              | **Description**                                                                                                                                                                       |
|-------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `formula-list`    | `FORMID`                   | A unique identifier for each formula entry in the table, used as a primary key for indexing and referencing.                                                                           |
| `formula-list`    | `FORMULA`                  | The original concatenated sequence of roots or elements that constitute the formula, separated by `+`.                                                                                 |
| `formula-list`    | `FORMULA LOWER`            | A lowercase version of the `FORMULA` field, ensuring consistency for case-insensitive analysis and comparisons.                                                                         |
| `formula-list`    | `FORMULA TRANSLITERATED`   | The formula represented in Roman script for transliteration, aiding phonetic analysis and accessibility for non-Arabic readers.                                                        |
| `formula-list`    | `FORMULA ARABIC`           | The Arabic script representation of the formula, providing the original textual form.                                                                                                  |
| `formula-list`    | `START SURA`               | The sura (chapter) number in the Quran where the formula begins.                                                                                                                       |
| `formula-list`    | `START VERSE`              | The verse number in the starting sura where the formula begins.                                                                                                                        |
| `formula-list`    | `START WORD`               | The position of the first word in the formula within the starting verse.                                                                                                               |
| `formula-list`    | `END VERSE`                | The verse number where the formula concludes.                                                                                                                                          |
| `formula-list`    | `START-SURA-VERSE`         | A compound identifier combining the sura and verse numbers (e.g., `2:3`), marking the formula's starting location in the Quran.                                                        |
| `formula-list`    | `END-SURA-VERSE`           | A compound identifier combining the sura and verse numbers (e.g., `2:4`), marking the formula's ending location in the Quran.                                                          |
| `formula-list`    | `FORMULA PROVENANCE`       | Specifies the historical or contextual classification of the formula, such as `Meccan` or `Medinan`, based on the sura's origin.                                                       |
| `formula-list`    | `LENGTH`                  | The number of root elements or words that make up the formula.                                                                                                                         |
| `formula-list`    | `TYPE`                    | The classification of the formula, often denoting the linguistic focus, such as `ROOT` (based on root patterns).                                                                       |
| `formula-list`    | `START RECORD`            | The record number in the database where the formula begins, used for indexing and referencing within the data.                                                                         |
| `formula-list`    | `END RECORD`              | The record number in the database where the formula ends.                                                                                                                              |
| `formula-list`    | `START GLOBAL WORD NUMBER` | A sequential number representing the starting word of the formula across the entire Quran.                                                                                             |
| `formula-list`    | `END GLOBAL WORD NUMBER`   | A sequential number representing the ending word of the formula across the entire Quran.                                                                                               |
| `formula-list`    | `OCCURRENCES`             | The total number of times the formula appears in the Quran.                                                                                                                            |
| `formula-list`    | `OCCURRENCES MECCAN`      | The number of times the formula appears in Meccan suras.                                                                                                                               |
| `formula-list`    | `OCCURRENCES MEDINAN`     | The number of times the formula appears in Medinan suras.                                                                                                                              |
| `formula-list`    | `Element1`                | The first root or element of the formula.                                                                                                                                               |
| `formula-list`    | `Element2`                | The second root or element of the formula.                                                                                                                                              |
| `formula-list`    | `Element3`                | The third root or element of the formula.                                                                                                                                               |
| `formula-list`    | `Element4`                | The fourth root or element of the formula.                                                                                                                                              |
| `formula-list`    | `Element5`                | The fifth root or element of the formula, if applicable.                                                                                                                               |
| `formula-list`    | `VERSE LIST`              | A semicolon-separated list of sura-verse pairs (e.g., `1:1; 2:3`) where the formula occurs.                                                                                             |
| `formula-list`    | `APPEARS IN HOW MANY SURAS`| The number of unique suras in which the formula appears.                                                                                                                               |
| `formula-list`    | `CONCAT OF FORMULA AND TYPE`| A concatenated string combining the formula and its type for quick identification and categorization (e.g., `smw+Alh+rHm+rHm-ROOT`).                                                   |
| `formula-list`    | `FORMULA ARCHETYPE ID`    | Links the formula to a specific archetype or template ID, grouping formulas into broader linguistic or thematic categories.                                                            |
| `formula-list`    | `FORMULA FULL GLOSS`      | A detailed explanation or interpretation of the formula, providing its semantic or contextual meaning.                                                                                  |

---

### **Key Insights**
1. **Formula Structure**:
   - Fields like `FORMULA`, `FORMULA TRANSLITERATED`, and `FORMULA ARABIC` define the formula in its original, phonetic, and Arabic forms.
2. **Occurrences and Context**:
   - `OCCURRENCES`, `OCCURRENCES MECCAN`, and `OCCURRENCES MEDINAN` provide quantitative context for the formula’s usage in different Quranic periods.
3. **Element Decomposition**:
   - `Element1` to `Element5` break down the formula into individual components for detailed linguistic analysis.
4. **Localization**:
   - `START-SURA-VERSE` and `END-SURA-VERSE` localize the formula within the Quran, while `VERSE LIST` maps all its occurrences.
5. **Archetypes and Glosses**:
   - `FORMULA ARCHETYPE ID` and `FORMULA FULL GLOSS` enrich the analysis by linking formulas to archetypes and providing their interpretive meanings.

---

### First 10 Rows Example (2025-01-14)
|   FORMID | FORMULA         | FORMULA LOWER   | FORMULA TRANSLITERATED   | FORMULA ARABIC        |   START SURA |   START VERSE |   START WORD |   END VERSE | START-SURA-VERSE   | END-SURA-VERSE   | FORMULA PROVENANCE   |   LENGTH | TYPE   |   START RECORD |   END RECORD |   START GLOBAL WORD NUMBER |   END GLOBAL WORD NUMBER |   OCCURRENCES |   OCCURRENCES MECCAN |   OCCURRENCES MEDINAN | Element1   | Element2   | Element3   | Element4   |   Element5 | VERSE LIST                             |   APPEARS IN HOW MANY SURAS | CONCAT OF FORMULA AND TYPE   |   FORMULA ARCHETYPE ID |   FORMULA FULL GLOSS |
|---------:|:----------------|:----------------|:-------------------------|:----------------------|-------------:|--------------:|-------------:|------------:|:-------------------|:-----------------|:---------------------|---------:|:-------|---------------:|-------------:|---------------------------:|-------------------------:|--------------:|---------------------:|----------------------:|:-----------|:-----------|:-----------|:-----------|-----------:|:---------------------------------------|----------------------------:|:-----------------------------|-----------------------:|---------------------:|
|        1 | smw+Alh+rHm+rHm | smw+alh+rhm+rhm | smw + 'lh + r?m + r?m    | سمو + اله + رحم + رحم |            1 |             1 |            1 |           1 | 1:1                | 1:1              | Meccan               |        4 | ROOT   |              2 |            7 |                          1 |                        4 |             2 |                    2 |                     0 | smw        | Alh        | rHm        | rHm        |        nan | 1:1; 27:30                             |                           2 | smw+Alh+rHm+rHm-ROOT         |                      1 |                  nan |
|        2 | Hmd+Alh+rbb+Elm | hmd+alh+rbb+elm | ?md + 'lh + rbb + ?lm    | حمد + اله + ربب + علم |            1 |             2 |            1 |           2 | 1:2                | 1:2              | Meccan               |        4 | ROOT   |              9 |           14 |                          5 |                        8 |             6 |                    6 |                     0 | Hmd        | Alh        | rbb        | Elm        |        nan | 1:2; 6:45; 10:10; 37:182; 39:75; 40:65 |                           6 | Hmd+Alh+rbb+Elm-ROOT         |                      2 |                  nan |
|        3 | hdy+SrT+qwm+SrT | hdy+srt+qwm+srt | hdy + ?r? + qwm + ?r?    | هدي + صرط + قوم + صرط |            1 |             6 |            1 |           7 | 1:6                | 1:7              | Meccan               |        4 | ROOT   |             28 |           34 |                         18 |                       21 |             2 |                    2 |                     0 | hdy        | SrT        | qwm        | SrT        |        nan | 1:6; 42:52                             |                           2 | hdy+SrT+qwm+SrT-ROOT         |                      3 |                  nan |
|        4 | qwm+Slw+rzq+nfq | qwm+slw+rzq+nfq | qwm + ?lw + rzq + nfq    | قوم + صلو + رزق + نفق |            2 |             3 |            4 |           3 | 2:3                | 2:3              | Medinan              |        4 | ROOT   |             68 |           78 |                         41 |                       45 |             3 |                    0 |                     3 | qwm        | Slw        | rzq        | nfq        |        nan | 2:3; 8:3; 22:35                        |                           3 | qwm+Slw+rzq+nfq-ROOT         |                      4 |                  nan |
|        5 | Slw+rzq+nfq+Amn | slw+rzq+nfq+amn | ?lw + rzq + nfq + 'mn    | صلو + رزق + نفق + امن |            2 |             3 |            5 |           4 | 2:3                | 2:4              | Medinan              |        4 | ROOT   |             71 |           82 |                         42 |                       47 |             2 |                    0 |                     2 | Slw        | rzq        | nfq        | Amn        |        nan | 2:3; 8:3                               |                           2 | Slw+rzq+nfq+Amn-ROOT         |                      5 |                  nan |
|        6 | Amn+nzl+nzl+qbl | amn+nzl+nzl+qbl | 'mn + nzl + nzl + qbl    | امن + نزل + نزل + قبل |            2 |             4 |            2 |           4 | 2:4                | 2:4              | Medinan              |        4 | ROOT   |             82 |           93 |                         47 |                       54 |             3 |                    0 |                     3 | Amn        | nzl        | nzl        | qbl        |        nan | 2:4; 4:60; 4:162                       |                           2 | Amn+nzl+nzl+qbl-ROOT         |                      6 |                  nan |
|        7 | Axr+yqn+hdy+rbb | axr+yqn+hdy+rbb | 'xr + yqn + hdy + rbb    | اخر + يقن + هدي + ربب |            2 |             4 |           10 |           5 | 2:4                | 2:5              | Medinan              |        4 | ROOT   |             98 |          106 |                         55 |                       62 |             2 |                    1 |                     1 | Axr        | yqn        | hdy        | rbb        |        nan | 2:4; 31:4                              |                           2 | Axr+yqn+hdy+rbb-ROOT         |                      7 |                  nan |
|        8 | yqn+hdy+rbb+flH | yqn+hdy+rbb+flh | yqn + hdy + rbb + fl?    | يقن + هدي + ربب + فلح |            2 |             4 |           12 |           5 | 2:4                | 2:5              | Medinan              |        4 | ROOT   |            100 |          112 |                         57 |                       65 |             2 |                    1 |                     1 | yqn        | hdy        | rbb        | flH        |        nan | 2:4; 31:4                              |                           2 | yqn+hdy+rbb+flH-ROOT         |                      8 |                  nan |
|        9 | swy+n*r+n*r+Amn | swy+n*r+n*r+amn | swy + ndhr + ndhr + 'mn  | سوي + نذر + نذر + امن |            2 |             6 |            4 |           6 | 2:6                | 2:6              | Medinan              |        4 | ROOT   |            117 |          129 |                         69 |                       76 |             2 |                    1 |                     1 | swy        | n*r        | n*r        | Amn        |        nan | 2:6; 36:10                             |                           2 | swy+n*r+n*r+Amn-ROOT         |                      9 |                  nan |
|       10 | Alh+qlb+smE+bSr | alh+qlb+sme+bsr | 'lh + qlb + sm? + b?r    | اله + قلب + سمع + بصر |            2 |             7 |            2 |           7 | 2:7                | 2:7              | Medinan              |        4 | ROOT   |            132 |          142 |                         78 |                       84 |             2 |                    1 |                     1 | Alh        | qlb        | smE        | bSr        |        nan | 2:7; 16:108                            |                           2 | Alh+qlb+smE+bSr-ROOT         |                     10 |                  nan |

---

## **Table name is `formula-id-codes-linked-global-words`**
This table maps formulaic phrases to their unique identifiers, linking them to globally occurring words within the Qur'an. It serves as a bridge between formulaic data and individual lexical items, aiding in understanding the compositional use of words across formulaic expressions.

### **Analysis of the `formula-id-codes-linked-global-words` Table**

Below is the detailed analysis and description of each field in the `formula-id-codes-linked-global-words` table, including the table name as a left-hand column.

---

| **Table Name**                                 | **Field Name**          | **Description**                                                                                                                                       |
|------------------------------------------------|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `formula-id-codes-linked-global-words`         | `GLOBAL WORD NUMBER`     | A unique sequential identifier for a word across the entire Quran. This field links each word to its position globally within the Quranic text.       |
| `formula-id-codes-linked-global-words`         | `FCODES`                 | A list of formula codes (e.g., `FC:8614`) associated with the corresponding global word. These codes represent formulas or patterns in which the word participates. |

---

### **Key Insights**
1. **Field Relationships**:
   - `GLOBAL WORD NUMBER` provides a unique identifier for precise referencing, linking to other tables or datasets that use this identifier for Quranic analysis.
   - `FCODES` lists formula codes, each denoting a unique formula or pattern in the Quranic text where the word occurs.

2. **Data Structure**:
   - The `FCODES` field can contain multiple values separated by commas, indicating that a word may participate in several formulas or linguistic patterns.
   - Empty `FCODES` (e.g., row 9) imply no formulas or patterns are linked to that particular global word.

3. **Applications**:
   - This table helps identify which formulas are associated with specific words, enabling detailed analysis of Quranic patterns, their prevalence, and their linguistic significance.
   - It supports cross-referencing with other tables, such as `formula-list`, to analyze the distribution of formulas in the Quran.

---

### Example Interpretation of Data:
- **Row 1**: The word with `GLOBAL WORD NUMBER` 1 is linked to formulas `FC:1`, `FC:8614`, `FC:8435`, and `FC:6352`.
- **Row 9**: No formulas are linked to the word with `GLOBAL WORD NUMBER` 9, indicating it does not participate in any identified patterns.

---

### First 10 Rows Example (2025-01-14)
| GLOBAL WORD NUMBER | FCODES                            |
|---|---|
| 1 | FC:1,FC:8614,FC:8435,FC:6352                       |
| 2 | FC:1,FC:8614,FC:8615,FC:8435,FC:6352,FC:7067       |
| 3 | FC:1,FC:8614,FC:8615,FC:8435,FC:6352,FC:7067       |
| 4 | FC:1,FC:8615,FC:8435,FC:7067                       |
| 5 | FC:2,FC:8616,FC:27081,FC:6280                      |
| 6 | FC:2,FC:8616,FC:8617,FC:27081,FC:6280,FC:6259      |
| 7 | FC:2,FC:8616,FC:8617,FC:27081,FC:6280,FC:6259      |
| 8 | FC:2,FC:8617,FC:27081,FC:6259                      |
| 9 |                                                    |
| 10 |                                                   |

---

## **Table name is `formula-archetype-list-lower`**
The `formula-archetype-list-lower` table organizes formulaic expressions by their archetypal forms, categorizing repeated patterns into simplified or "lower-case" structures for linguistic generalization. It is instrumental in recognizing underlying archetypes in the Qur'an's repetitive stylistic elements.

### **Analysis of the `formula-archetype-list-lower` Table**

Below is the detailed analysis and description of each field in the `formula-archetype-list-lower` table, including the table name as a left-hand column.

---

| **Table Name**                      | **Field Name**       | **Description**                                                                                                                                          |
|-------------------------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `formula-archetype-list-lower`      | `FORMULA ID`          | A unique identifier for each formula archetype, used as the primary key for indexing and referencing.                                                    |
| `formula-archetype-list-lower`      | `FORMULA LOWER`       | A lowercase representation of the formula archetype, consisting of concatenated root elements separated by `+`.                                          |
| `formula-archetype-list-lower`      | `LENGTH`              | The number of root elements or components in the formula archetype.                                                                                      |
| `formula-archetype-list-lower`      | `TYPE`                | The classification or category of the formula archetype, such as `ROOT`, indicating that the formula is based on root patterns in the Quran.             |

---

### **Key Insights**
1. **Field Relationships**:
   - `FORMULA ID` uniquely identifies each formula archetype, linking it to other data sources or tables that analyze Quranic linguistic patterns.
   - `FORMULA LOWER` standardizes the formula for consistent analysis, ensuring case-insensitive comparisons across different datasets.

2. **Formula Analysis**:
   - The `FORMULA LOWER` field breaks down formulas into their root components, providing insights into Quranic linguistic structures and recurring patterns.
   - The `LENGTH` field specifies the size of the formula, allowing for classification and segmentation of formulas by their complexity.

3. **Applications**:
   - This table supports linguistic analysis by categorizing Quranic formulas and linking them to specific root structures or patterns.
   - The `TYPE` field, with the value `ROOT`, emphasizes the focus on root-based formulas, which are fundamental in Arabic morphology and Quranic exegesis.

---

### Example Interpretation of Data:
- **Row 1**: Formula with ID `1` has the structure `smw+alh+rhm+rhm`, consisting of 4 root elements (`LENGTH = 4`) and is classified as a `ROOT` formula.
- **Row 10**: Formula with ID `10` has the structure `alh+qlb+sme+bsr`, also consisting of 4 root elements, and is similarly categorized as a `ROOT` formula.

---

### Contextual Significance:
- **Focus on Roots**:
  - The table highlights the centrality of root-based formulas in Quranic linguistic analysis, reflecting the importance of roots in Arabic language studies.
- **Archetype Identification**:
  - By standardizing and categorizing formula archetypes, this table serves as a foundational reference for identifying recurring patterns and their theological or linguistic significance.

---

### First 10 Rows Example (2025-01-14)
|   FORMULA ID | FORMULA LOWER   |   LENGTH | TYPE   |
|-------------:|:----------------|---------:|:-------|
|            1 | smw+alh+rhm+rhm |        4 | ROOT   |
|            2 | hmd+alh+rbb+elm |        4 | ROOT   |
|            3 | hdy+srt+qwm+srt |        4 | ROOT   |
|            4 | qwm+slw+rzq+nfq |        4 | ROOT   |
|            5 | slw+rzq+nfq+amn |        4 | ROOT   |
|            6 | amn+nzl+nzl+qbl |        4 | ROOT   |
|            7 | axr+yqn+hdy+rbb |        4 | ROOT   |
|            8 | yqn+hdy+rbb+flh |        4 | ROOT   |
|            9 | swy+n*r+n*r+amn |        4 | ROOT   |
|           10 | alh+qlb+sme+bsr |        4 | ROOT   |

---

## **Table name is `quran-translation`**
The `quran-translation` table contains translations of the Qur'an into various languages, each entry aligning with its corresponding verse. It includes details like the translator’s name and translation metadata, making it a valuable resource for comparative studies and linguistic research.

### **Analysis of the `quran-translation` Table**

Below is a detailed analysis and description of each field in the `quran-translation` table, with the table name included as a left-hand column.

---

| **Table Name**        | **Field Name**     | **Description**                                                                                                                                                   |
|------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `quran-translation`    | `Sura`            | The chapter number in the Quran, indicating the sura to which the verse belongs.                                                                                  |
| `quran-translation`    | `Verse`           | The verse number within the sura, identifying the specific verse being referenced.                                                                                 |
| `quran-translation`    | `Translator`      | The name of the translator (e.g., Yusuf Ali) who provided the English translation of the verse.                                                                    |
| `quran-translation`    | `Text`            | The translated text of the verse, including HTML-like `<eX>` tags to highlight specific segments of the verse for emphasis or annotation purposes.                  |

---

### **Key Insights**

1. **Field Relationships**:
   - `Sura` and `Verse` together uniquely identify a specific verse within the Quran, providing a direct reference to its original location in the text.
   - `Translator` specifies the source of the translation, allowing for comparative studies between different translations.

2. **Text Representation**:
   - The `Text` field includes HTML-like tags (e.g., `<e1>`, `<e2>`) to mark portions of the translation, likely for emphasis, annotation, or segmentation.
   - The structure allows for enhanced readability and enables tools to manipulate or highlight parts of the translation programmatically.

3. **Applications**:
   - Supports Quranic study by providing translations of verses for non-Arabic speakers.
   - The use of tags in the `Text` field makes it easier to integrate translations into digital applications with advanced formatting or interactive capabilities.

---

### Example Interpretation of Data:
- **Row 1**:
  - **Sura**: 1
  - **Verse**: 1
  - **Translator**: Yusuf Ali
  - **Text**: `<e1>In the name</e> <e2>of Allah</e>, <e3>Most Gracious</e>, <e4>Most Merciful</e>.`
  - This provides a structured and tagged English translation of the verse.

- **Row 3**:
  - **Sura**: 1
  - **Verse**: 3
  - **Text**: `<e9>Most Gracious</e>, <e10>Most Merciful</e>;`
  - Tags emphasize key descriptive phrases.

---

### Contextual Significance:
1. **Tagged Structure**:
   - The `<eX>` tags suggest a segmentation strategy that aids in digital applications such as interlinear tools or thematic analysis.
2. **Comparative Translation**:
   - Including the translator allows for future additions of multiple translations, enabling comparative studies of translation styles and interpretations.
3. **Accessibility**:
   - By associating verses with translations, the table makes the Quran accessible to a broader audience, particularly non-Arabic speakers.

---

### First 10 Rows Example (2025-01-14)
| Sura   |   Verse | Translator   | Text                                                                                                                  |
|:-------|--------:|:-------------|:----------------------------------------------------------------------------------------------------------------------|
| 1      |       2 | Yusuf Ali    | <e5>Praise be</e> <e6>to Allah</e>, <e7>the Cherisher and Sustainer</e> <e8>of the worlds</e>;                        |
| 1      |       1 | Yusuf Ali    | <e1>In the name</e> <e2>of Allah</e>, <e3>Most Gracious</e>, <e4>Most Merciful</e>.                                   |
| 1      |       3 | Yusuf Ali    | <e9>Most Gracious</e>, <e10>Most Merciful</e>;                                                                        |
| 1      |       4 | Yusuf Ali    | <e11>Master</e><e12> of the Day</e> <e13>of Judgment</e>.                                                             |
| 1      |       5 | Yusuf Ali    | Thee do we worship, and Thine aid we seek. \n                                                                         |
| 1      |       6 | Yusuf Ali    | Show us the straight way, \n                                                                                          |
| 1      |       7 | Yusuf Ali    | The way of those on whom Thou hast bestowed Thy Grace, those \nwhose (portion) is not wrath, and who go not astray.\n |
| 2      |       1 | Yusuf Ali    | A.L.M. \n                                                                                                             |
| 2      |       2 | Yusuf Ali    | This is the Book; in it is guidance sure, without doubt, to \nthose who fear Allah;\n                                 |
| 2      |       3 | Yusuf Ali    | Who believe in the Unseen, are steadfast in prayer, and spend \nout of what We have provided for them;\n              |

---

## **Table name is `exact-arabic-list`**
The `exact-arabic-list` table provides a precise list of Arabic words in their original script, extracted from the Qur'an. It is used to ensure textual accuracy and facilitate analyses requiring direct access to the Qur'an's language.

### **Analysis of the `exact-arabic-list` Table**

Below is the detailed analysis and description of each field in the `exact-arabic-list` table, with the table name included as a left-hand column.

---

| **Table Name**        | **Field Name**       | **Description**                                                                                                                                   |
|------------------------|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `exact-arabic-list`    | `EXACT ID`          | A unique identifier for each exact Arabic phrase or word in the list. This serves as the primary key for indexing and referencing.                |
| `exact-arabic-list`    | `EXACT ARABIC`      | The precise Arabic text of the word or phrase, maintaining its original diacritical marks for accurate representation and analysis.                |

---

### **Key Insights**

1. **Field Relationships**:
   - `EXACT ID` uniquely identifies each entry in the table, allowing for precise mapping and referencing in related datasets.
   - `EXACT ARABIC` provides the exact Arabic spelling, including diacritics, ensuring textual integrity for linguistic or scriptural studies.

2. **Text Representation**:
   - The `EXACT ARABIC` field captures words or phrases exactly as they appear in the Quran, preserving subtle orthographic differences critical to interpretation and linguistic analysis.

3. **Applications**:
   - Enables Quranic studies requiring exact matches of Arabic words or phrases.
   - Facilitates computational text analysis, such as frequency counts, orthographic studies, and contextual searches.

---

### Example Interpretation of Data:
- **Row 1**:
  - **EXACT ID**: 861
  - **EXACT ARABIC**: `ءَآللَّەُ`
  - Represents the exact Arabic text for a word or phrase, including the hamza, shadda, and other diacritical marks.

- **Row 5**:
  - **EXACT ID**: 12400
  - **EXACT ARABIC**: `ءَأَسْلَمْتُمْ`
  - Represents a specific Quranic phrase in its precise Arabic form, preserving all orthographic details.

---

---
### First 10 Rows Example (2025-01-14)
|   EXACT ID | EXACT ARABIC   |
|-----------:|---------------:|
|        861 | ءَآللَّەُ |
|      11307 | ءَأَتَّخِذُ |
|       2332 | ءَأَرْبَابٌ |
|       4527 | ءَأَسْجُدُ |
|      12400 | ءَأَسْلَمْتُمْ |
|      15254 | ءَأَشْفَقْتُمْ |
|       8227 | ءَأَشْكُرُ |
|      12615 | ءَأَقْرَرْتُمْ |
|       1831 | ءَأَلِدُ |
|      16166 | ءَأَمِنتُم |


### Contextual Significance:
1. **Linguistic Accuracy**:
   - By preserving diacritical marks, the table ensures linguistic and phonetic precision, which is essential for Quranic recitation (tajweed) and textual integrity.
2. **Orthographic Studies**:
   - This table can be used for studying orthographic variants and patterns in Quranic text.
3. **Digital Applications**:
   - Useful for creating searchable Quranic databases or linguistic tools that rely on exact text matches.

---

## **Table name is `exact-transliteration-list`**
The `exact-transliteration-list` table contains transliterated versions of Arabic words from the Qur'an, using standardized Latin scripts. This is especially useful for linguistic studies and for readers unfamiliar with the Arabic script who wish to study the Qur'an's phonetics and structure.

### **Analysis of the `exact-transliteration-list` Table**

Below is the detailed analysis and description of each field in the `exact-transliteration-list` table, with the table name included as a left-hand column.

---

| **Table Name**                  | **Field Name**            | **Description**                                                                                                                                         |
|----------------------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exact-transliteration-list`     | `EXACT ID`                | A unique identifier for each transliterated Arabic word or phrase in the list. This serves as the primary key for indexing and referencing.             |
| `exact-transliteration-list`     | `EXACT TRANSLITERATION`   | The precise transliteration of an Arabic word or phrase into Roman script, preserving phonetic accuracy for non-Arabic speakers.                        |

---

### **Key Insights**

1. **Field Relationships**:
   - `EXACT ID` uniquely identifies each transliteration, allowing it to be linked to other datasets or tables that include related Arabic words or phrases.
   - `EXACT TRANSLITERATION` provides the Romanized equivalent of the exact Arabic text, ensuring phonetic representation and accessibility for analysis.

2. **Text Representation**:
   - The `EXACT TRANSLITERATION` field captures the transliterated version of the Arabic text using diacritical marks and phonetic approximations, preserving the linguistic nuances.

3. **Applications**:
   - Facilitates Quranic studies for non-Arabic speakers by providing accurate transliterations for recitation or analysis.
   - Supports computational linguistic tools requiring both phonetic and textual representations of Quranic words.

---

### Example Interpretation of Data:
- **Row 1**:
  - **EXACT ID**: 1
  - **EXACT TRANSLITERATION**: `bi-aṣḥābi`
  - Represents the transliterated form of an Arabic word or phrase, capturing its phonetic essence.
- **Row 3**:
  - **EXACT ID**: 3
  - **EXACT TRANSLITERATION**: `a-alidu`
  - Provides the transliteration of the Arabic phrase for accurate recitation and analysis.

---

### Contextual Significance:
1. **Phonetic Accessibility**:
   - The table bridges the gap for non-Arabic speakers, enabling them to study and recite Quranic text with correct phonetics.
2. **Linguistic Analysis**:
   - Useful for studying the relationship between Arabic script and its phonetic representation, particularly in Quranic recitation (tajweed).
3. **Digital Tools**:
   - The table can power Quranic apps or linguistic tools that rely on phonetic search or interlinear text alignment.

---

### First 10 Rows Example (2025-01-14)
|   EXACT ID | EXACT TRANSLITERATION   |
|-----------:|:------------------------|
|          1 | bi-aṣḥābi               |
|          2 | miʾatun                 |
|          3 | a-alidu                 |
|          4 | a-ālihatunā             |
|          5 | a-amintum               |
|          6 | a-andhartahum           |
|          7 | a-anta                  |
|          8 | a-aqrartum              |
|          9 | a-arbābun               |
|         10 | a-ashkuru               |


---

## **Table name is `quran-verse-endings`**
The `quran-verse-endings` table focuses on the rhyming and stylistic structures at the end of Qur'anic verses. It documents verse-ending patterns, including linguistic and phonetic features, and is vital for studying Qur'anic rhyme and rhythm.

### **Analysis of the `quran-verse-endings` Table**

Below is the detailed analysis and description of each field in the `quran-verse-endings` table, with the table name included as a left-hand column.

---

| **Table Name**             | **Field Name**                 | **Description**                                                                                                                                                     |
|-----------------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `quran-verse-endings`       | `SURA-VERSE`                   | A combined identifier that specifies the chapter (sura) and verse number in the Quran (e.g., `100:1` for sura 100, verse 1).                                        |
| `quran-verse-endings`       | `SURA`                        | The sura (chapter) number in the Quran.                                                                                                                            |
| `quran-verse-endings`       | `VERSE`                       | The verse number within the sura.                                                                                                                                  |
| `quran-verse-endings`       | `FINAL 2 LETTERS`             | The last two letters of the verse's final word, representing the rhyme or phonetic pattern.                                                                         |
| `quran-verse-endings`       | `MATCHES NEXT VERSE ENDING`   | Indicates whether the final letters of this verse's ending match the next verse's ending (`1` for yes, `0` for no).                                                |
| `quran-verse-endings`       | `FINAL WORD`                  | The last word of the verse in Arabic transliteration, providing the textual context for the ending.                                                                 |
| `quran-verse-endings`       | `FINAL GLOBAL WORD NUMBER`    | The global word number assigned to the final word of the verse, uniquely identifying it in the Quranic corpus.                                                     |

---

### **Key Insights**

1. **Field Relationships**:
   - `SURA-VERSE` uniquely identifies each verse in the Quran, linking it to its corresponding ending and other characteristics.
   - `FINAL GLOBAL WORD NUMBER` provides a precise mapping to the global word dataset, enabling advanced cross-referencing.

2. **Verse Endings Analysis**:
   - `FINAL 2 LETTERS` highlights rhyme patterns and phonetic structures, which are significant in Quranic recitation (tajweed) and stylistic studies.
   - `MATCHES NEXT VERSE ENDING` captures rhyme consistency between consecutive verses, which is a key feature of Quranic eloquence.

3. **Applications**:
   - Supports linguistic studies of Quranic rhyme schemes and phonetics.
   - Enables computational analysis of stylistic patterns, such as rhyme continuity across verses.

---

### Example Interpretation of Data:
- **Row 1**:
  - **SURA-VERSE**: `100:1`
  - **FINAL 2 LETTERS**: `an`
  - **MATCHES NEXT VERSE ENDING**: `1` (matches the next verse ending)
  - **FINAL WORD**: `ḍabḥan`
  - Indicates that the verse ends with a rhyme pattern (`an`) that continues in the next verse.

- **Row 6**:
  - **SURA-VERSE**: `100:6`
  - **FINAL 2 LETTERS**: `un`
  - **MATCHES NEXT VERSE ENDING**: `1` (matches the next verse ending)
  - **FINAL WORD**: `lakanūdun`
  - Demonstrates a consistent rhyme (`un`) with the subsequent verse.

---

### Contextual Significance:
1. **Phonetic Patterns**:
   - `FINAL 2 LETTERS` aids in understanding the Quran’s rhyme schemes, which contribute to its melodic and rhythmic qualities.
2. **Rhyme Consistency**:
   - The `MATCHES NEXT VERSE ENDING` field provides insights into the intentional continuity of verse endings, reflecting Quranic stylistic elegance.
3. **Global Word Tracking**:
   - `FINAL GLOBAL WORD NUMBER` ensures traceability of verse endings within the entire Quranic corpus.

---

### First 10 Rows Example (2025-01-14)
| SURA-VERSE   |   SURA |   VERSE | FINAL 2 LETTERS   |   MATCHES NEXT VERSE ENDING | FINAL WORD   |   FINAL GLOBAL WORD NUMBER |
|:-------------|-------:|--------:|:------------------|----------------------------:|:-------------|---------------------------:|
| 100:1        |    100 |       1 | an                |                           1 | ?ab?an       |                      77079 |
| 100:10       |    100 |      10 | ri                |                           0 | l-?ud?ri     |                      77112 |
| 100:11       |    100 |      11 | un                |                           0 | la-khab?run  |                      77117 |
| 100:2        |    100 |       2 | an                |                           1 | qad?an       |                      77081 |
| 100:3        |    100 |       3 | an                |                           1 | ?ub?an       |                      77083 |
| 100:4        |    100 |       4 | an                |                           1 | naq?an       |                      77086 |
| 100:5        |    100 |       5 | an                |                           0 | jam?an       |                      77089 |
| 100:6        |    100 |       6 | un                |                           1 | lakan?dun    |                      77093 |
| 100:7        |    100 |       7 | un                |                           1 | lashah?dun   |                      77097 |
| 100:8        |    100 |       8 | un                |                           0 | la-shad?dun  |                      77101 |	

---

## **Table name is `formulaic-glosses`**
The `formulaic-glosses` table provides glosses or meanings for recurring formulae in the Qur'an, adding semantic context to repeated phrases. It helps in understanding the significance and meaning behind formulaic elements in the Qur'an's structure.

### **Analysis of the `formulaic-glosses` Table**

Below is the detailed analysis and description of each field in the `formulaic-glosses` table, with the table name included as a left-hand column.

---

| **Table Name**             | **Field Name** | **Description**                                                                                                                                           |
|-----------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `formulaic-glosses`         | `FID`          | A unique identifier for each formulaic gloss entry, serving as the primary key for indexing and referencing.                                               |
| `formulaic-glosses`         | `LEXEME`       | The root or lexeme of the word or phrase in transliterated form, representing the linguistic base from which various derivations can occur.                |
| `formulaic-glosses`         | `GLOSS`        | The English gloss or meaning of the lexeme, providing a concise explanation or translation that aids in understanding its contextual use in formulas.       |

---

### **Key Insights**

1. **Field Relationships**:
   - `FID` uniquely identifies each entry, linking it to other datasets or tables containing Quranic formulas or linguistic elements.
   - `LEXEME` represents the fundamental root or morphological unit, critical for understanding its derivational family in Arabic.

2. **Linguistic Utility**:
   - The `GLOSS` field provides the semantic interpretation of the lexeme, which is useful for linguistic studies, translation efforts, and formulaic analysis.
   - Together, the `LEXEME` and `GLOSS` fields form a lexicon of formulaic components that can be used to explore recurring patterns and meanings in Quranic text.

3. **Applications**:
   - Supports formulaic analysis by linking lexemes to their meanings in a standardized way.
   - Facilitates linguistic studies on root meanings and their various contexts within the Quran.

---

### Example Interpretation of Data:
- **Row 1**:
  - **FID**: `1`
  - **LEXEME**: `$Am`
  - **GLOSS**: `(of) the left?`
  - Represents the formulaic gloss for the root `$Am`, providing insight into its semantic role in formulas.

- **Row 10**:
  - **FID**: `10`
  - **LEXEME**: `$fq`
  - **GLOSS**: `fearful`
  - Represents the semantic interpretation of the lexeme `$fq`, aiding in understanding its use in Quranic formulas.

---

### First 10 Rows Example (2025-01-14)
|   FID | LEXEME   | GLOSS             |
|------:|:---------|:------------------|
|     1 | $Am      | (of) the left?    |
|     3 | $bh      | resembling        |
|     4 | $dd      | severe            |
|     7 | $Er      | perceive          |
|     8 | $fE      | any intercessor   |
|    10 | $fq      | fearful           |
|    16 | $hd      | (as) a Witness    |
|    17 | $HH      | (from) stinginess |
|    19 | $Hn      | laden             |
|    21 | $hr      | months            |

---

### Contextual Significance:
1. **Linguistic Insights**:
   - By providing both the lexeme and its gloss, the table offers insights into how formulaic structures in the Quran are constructed and interpreted.
2. **Formulaic Analysis**:
   - This table can be integrated with others (e.g., `formula-list`) to analyze how glosses and lexemes combine to form complex linguistic patterns.
3. **Cross-Linguistic Applications**:
   - The data can be used for translation studies, showing how Arabic roots map to concise English meanings in Quranic formulas.

---

## **Table name is `lemma-list`**
The `lemma-list` table contains base forms of words (lemmas) found in the Qur'an. It acts as a lexical reference for scholars analyzing word usage, morphology, and semantics in the text.

### Analysis of the `lemma-list` Table

Below is the detailed analysis of the `lemma-list` table, with unique descriptions for each field.

---

| **Table Name**  | **Field Name**               | **Description**                                                                                                                                              |
|------------------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lemma-list`     | `LEMMA ID`                 | A unique identifier for each lemma entry, serving as the primary key for the table.                                                                          |
| `lemma-list`     | `ENGLISH`                  | The English transliteration of the lemma, providing a readable representation for non-Arabic speakers.                                                       |
| `lemma-list`     | `ENGLISH-BINARY`           | A binary-encoded representation of the English transliteration, primarily for computational purposes.                                                        |
| `lemma-list`     | `ARABIC`                   | The lemma in Arabic script, capturing its original orthographic representation.                                                                               |
| `lemma-list`     | `ARABIC ALTERNATE RENDERING` | An alternative rendering of the Arabic lemma, reflecting variations or orthographic differences.                                                             |
| `lemma-list`     | `ROOT`                     | The linguistic root associated with the lemma, linking it to its morphological base.                                                                          |
| `lemma-list`     | `ROOT-BINARY`              | A binary-encoded representation of the root for computational analysis.                                                                                       |
| `lemma-list`     | `COUNT`                    | The total number of occurrences of the lemma in the Qur'an.                                                                                                   |
| `lemma-list`     | `COUNT MECCAN`             | The number of times the lemma appears in Meccan chapters.                                                                                                     |
| `lemma-list`     | `COUNT MEDINAN`            | The number of times the lemma appears in Medinan chapters.                                                                                                    |
| `lemma-list`     | `ENGLISH TRANSLITERATED`   | A phonetic representation of the lemma in Roman script, aiding in pronunciation for non-Arabic speakers.                                                     |
| `lemma-list`     | `100-COUNT-ALL`            | The normalized frequency of the lemma per 100 words across the entire Qur'an.                                                                                 |
| `lemma-list`     | `100-COUNT-MECCAN`         | The normalized frequency of the lemma per 100 words in Meccan chapters.                                                                                       |
| `lemma-list`     | `100-COUNT-MEDINAN`        | The normalized frequency of the lemma per 100 words in Medinan chapters.                                                                                      |
| `lemma-list`     | `GLOSS`                    | A concise English explanation or meaning of the lemma, providing its semantic context.                                                                        |
| `lemma-list`     | `PROPER NOUN`              | A flag indicating whether the lemma is a proper noun (e.g., a name or place).                                                                                 |
| `lemma-list`     | `CORRECTED TRANSLITERATION`| A corrected transliteration of the lemma if adjustments were necessary for accuracy or consistency.                                                           |
| `lemma-list`     | `ALTERNATIVE TRANSLITERATION` | An alternative transliteration of the lemma, reflecting regional or scholarly differences.                                                                    |
| `lemma-list`     | `LEMMA FIX NOT NEEDED`     | A flag indicating whether the lemma required no corrections during data processing.                                                                           |
| `lemma-list`     | `LEMMA FIXED BY USER`      | A flag showing whether the lemma's transliteration or other attributes were corrected manually by a user.                                                     |
| `lemma-list`     | `AJ FOREIGN PAGE`          | A reference to additional external sources or pages where the lemma may be further described, such as in lexicons or concordances.                           |

---

### Key Insights

1. **Linguistic Focus**:
   - The table connects lemmas to their roots (`ROOT`) and provides phonetic, orthographic, and semantic details for in-depth linguistic analysis.
   - Frequency fields (`COUNT`, `100-COUNT-ALL`, etc.) enable statistical studies of lemma distribution in the Qur'an.

2. **Applications**:
   - Supports linguistic studies by linking lemmas to their roots and providing contextual meanings.
   - Facilitates translation work with accurate glosses and transliterations.

3. **Error Tracking**:
   - The `CORRECTED TRANSLITERATION`, `LEMMA FIX NOT NEEDED`, and `LEMMA FIXED BY USER` fields ensure data accuracy and transparency in lemma processing.

---

### First 10 Rows Example (2025-01-14)
|   LEMMA ID | ENGLISH   | ENGLISH-BINARY                                          | ARABIC   |   ARABIC ALTERNATE RENDERING | ROOT   | ROOT-BINARY           |   COUNT |   COUNT MECCAN |   COUNT MEDINAN | ENGLISH TRANSLITERATED   |   100-COUNT-ALL |   100-COUNT-MECCAN |   100-COUNT-MEDINAN | GLOSS                           |   PROPER NOUN | CORRECTED TRANSLITERATION   | ALTERNATIVE TRANSLITERATION   |   LEMMA FIX NOT NEEDED |   LEMMA FIXED BY USER |   AJ FOREIGN PAGE |
|-----------:|:----------|:--------------------------------------------------------|:---------|-----------------------------:|:-------|:----------------------|--------:|---------------:|----------------:|:-------------------------|----------------:|-------------------:|--------------------:|:--------------------------------|--------------:|:----------------------------|:------------------------------|-----------------------:|----------------------:|------------------:|
|          1 | $a>on     | $a>on\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0 | شَأْن |                          nan | $An    | $An\0\0\0\0\0\0\0\0\0 |       4 |              3 |               1 | shan                     |      0.00536164 |         0.00638311 |          0.00362253 | nan                             |             0 | sha'n!                      | test1,test2                   |                      1 |                     1 |               nan |
|          2 | $aAEir    | $aAEir\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0  | شَاعِر |                          nan | $Er    | $Er\0\0\0\0\0\0\0\0\0 |       5 |              5 |               0 | sh??ir                   |      0.00670205 |         0.0106385  |          0          | nan                             |             0 | zZZ                         | nan                           |                    nan |                     1 |               nan |
|          3 | $aA^'a    | $aA^'a\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0  | شَآءَ |                          nan | $yA    | $yA\0\0\0\0\0\0\0\0\0 |     236 |            160 |              76 | sh?a                     |      0.316337   |         0.340433   |          0.275312   | nan                             |             0 | nan                         | nan                           |                    nan |                   nan |               nan |
|          4 | $aA^q~u   | $aA^q~u\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0   | شَآقُّ |                          nan | $qq    | $qq\0\0\0\0\0\0\0\0\0 |       7 |              1 |               6 | sh?qqu                   |      0.00938287 |         0.0021277  |          0.0217352  | nan                             |             0 | nan                         | nan                           |                    nan |                   nan |               nan |
|          5 | $aAhid    | $aAhid\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0  | شَاهِد |                          nan | $hd    | $hd\0\0\0\0\0\0\0\0\0 |      21 |             14 |               7 | sh?hid                   |      0.0281486  |         0.0297879  |          0.0253577  | nan                             |             0 | nan                         | nan                           |                    nan |                   nan |               nan |
|          6 | $aAkilat  | $aAkilat\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0    | شَاكِلَت |                          nan | $kl    | $kl\0\0\0\0\0\0\0\0\0 |       1 |              1 |               0 | sh?kilat                 |      0.00134041 |         0.0021277  |          0          | nan                             |             0 | nan                         | nan                           |                    nan |                     1 |               nan |
|          7 | $aAkir    | $aAkir\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0  | شَاكِر |                          nan | $kr    | $kr\0\0\0\0\0\0\0\0\0 |      14 |             10 |               4 | sh?kir                   |      0.0187657  |         0.021277   |          0.0144901  | nan                             |             0 | nan                         | nan                           |                    nan |                     1 |               nan |
|          8 | $aAni}    | $aAni}\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0  | شَانِئ |                          nan | $nA    | $nA\0\0\0\0\0\0\0\0\0 |       1 |              1 |               0 | sh?ni                    |      0.00134041 |         0.0021277  |          0          | nan                             |             0 | nan                         | nan                           |                    nan |                     1 |               nan |
|          9 | $aAriko   | $aAriko\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0   | شَارِكْ |                          nan | $rk    | $rk\0\0\0\0\0\0\0\0\0 |       1 |              1 |               0 | sh?rik                   |      0.00134041 |         0.0021277  |          0          | To associate something with God |             0 | nan                         | nan                           |                    nan |                     1 |               185 |
|         10 | $aAwiro   | $aAwiro\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0   | شَاوِرْ |                          nan | $wr    | $wr\0\0\0\0\0\0\0\0\0 |       1 |              0 |               1 | sh?wir                   |      0.00134041 |         0          |          0.00362253 | nan                             |             0 | nan                         | nan                           |                    nan |                   nan |               nan |

---
## **Table name is `quran-full-parse`**
This table provides a detailed grammatical breakdown of each verse, including word-by-word parsing and annotations of parts of speech. It is an essential resource for linguistic and syntactic analysis of the Qur'an.

### **Analysis of the `quran-full-parse` Table**

Below is the detailed analysis and description of each field in the `quran-full-parse` table, with the table name included as a left-hand column and a fourth column indicating compressed or expanded data.

---

| **Table Name**          | **Field Name**                              | **Description**                                                                                                                                         | **Compressed/Expanded** |
|--------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| `quran-full-parse`       | `ID`                                        | A unique identifier for each parsed record, used as the primary key for indexing and referencing.                                                       | Expanded                |
| `quran-full-parse`       | `SURA-VERSE`                                | A compound identifier combining the chapter (Sura) and verse numbers, uniquely identifying the verse (e.g., `2:1`).                                     | Expanded                |
| `quran-full-parse`       | `SURA`                                      | The sura (chapter) number in the Quran.                                                                                                                 | Expanded                |
| `quran-full-parse`       | `VERSE`                                     | The verse number within the sura.                                                                                                                       | Expanded                |
| `quran-full-parse`       | `PARSING`                                   | A detailed parsing of the verse's linguistic components, including grammatical, morphological, and formulaic data encoded in compressed syntax.          | Compressed              |
| `quran-full-parse`       | `Provenance`                                | Indicates the historical or contextual origin of the verse (e.g., Meccan or Medinan).                                                                   | Expanded                |
| `quran-full-parse`       | `Intertextual Link Count`                   | The number of intertextual references or connections linked to the verse.                                                                               | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-ROOT`                            | The total count of root occurrences in the verse as determined by Qur’an Tools analysis.                                                                | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-ROOT-FLAGGED-3-ROOT-FORMULAE`    | The count of flagged 3-root formulaic structures involving roots in the verse.                                                                          | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-ROOT-FLAGGED-4-ROOT-FORMULAE`    | The count of flagged 4-root formulaic structures involving roots in the verse.                                                                          | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-ROOT-FLAGGED-5-ROOT-FORMULAE`    | The count of flagged 5-root formulaic structures involving roots in the verse.                                                                          | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-LEMMA`                           | The total count of lemma occurrences in the verse as determined by Qur’an Tools analysis.                                                               | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-LEMMA-FLAGGED-3-LEMMA-FORMULAE`  | The count of flagged 3-lemma formulaic structures involving lemmas in the verse.                                                                        | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-LEMMA-FLAGGED-4-LEMMA-FORMULAE`  | The count of flagged 4-lemma formulaic structures involving lemmas in the verse.                                                                        | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-LEMMA-FLAGGED-5-LEMMA-FORMULAE`  | The count of flagged 5-lemma formulaic structures involving lemmas in the verse.                                                                        | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-ROOT-OR-PARTICLE`                | The total count of root-or-particle occurrences in the verse.                                                                                           | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-ROOT-OR-PARTICLE-FLAGGED-3-ROOT-ALL-FORMULAE` | The count of flagged 3-root formulaic structures including roots or particles.                                                                          | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-ROOT-OR-PARTICLE-FLAGGED-4-ROOT-ALL-FORMULAE` | The count of flagged 4-root formulaic structures including roots or particles.                                                                          | Expanded                |
| `quran-full-parse`       | `COUNT-QTL-ROOT-OR-PARTICLE-FLAGGED-5-ROOT-ALL-FORMULAE` | The count of flagged 5-root formulaic structures including roots or particles.                                                                          | Expanded                |
| `quran-full-parse`       | `Translator Yusuf Ali`                      | The verse translation provided by Yusuf Ali.                                                                                                            | Expanded                |
| `quran-full-parse`       | `Translator Shakir`                         | The verse translation provided by Shakir.                                                                                                               | Expanded                |
| `quran-full-parse`       | `Translator Pickthall`                      | The verse translation provided by Pickthall.                                                                                                            | Expanded                |
| `quran-full-parse`       | `Translator Arberry`                        | The verse translation provided by Arberry.                                                                                                              | Expanded                |
| `quran-full-parse`       | `FORMULAIC-DENSITY-3-ROOT`                  | The formulaic density of 3-root formulaic structures in the verse.                                                                                      | Expanded                |
| `quran-full-parse`       | `FORMULAIC-DENSITY-4-ROOT`                  | The formulaic density of 4-root formulaic structures in the verse.                                                                                      | Expanded                |
| `quran-full-parse`       | `FORMULAIC-DENSITY-5-ROOT`                  | The formulaic density of 5-root formulaic structures in the verse.                                                                                      | Expanded                |
| `quran-full-parse`       | `FORMULAIC-DENSITY-3-LEMMA`                 | The formulaic density of 3-lemma formulaic structures in the verse.                                                                                     | Expanded                |
| `quran-full-parse`       | `FORMULAIC-DENSITY-4-LEMMA`                 | The formulaic density of 4-lemma formulaic structures in the verse.                                                                                     | Expanded                |
| `quran-full-parse`       | `FORMULAIC-DENSITY-5-LEMMA`                 | The formulaic density of 5-lemma formulaic structures in the verse.                                                                                     | Expanded                |
| `quran-full-parse`       | `FORMULAIC-DENSITY-3-ROOT-ALL`              | The formulaic density of all 3-root formulaic structures in the verse.                                                                                  | Expanded                |
| `quran-full-parse`       | `FORMULAIC-DENSITY-4-ROOT-ALL`              | The formulaic density of all 4-root formulaic structures in the verse.                                                                                  | Expanded                |
| `quran-full-parse`       | `FORMULAIC-DENSITY-5-ROOT-ALL`              | The formulaic density of all 5-root formulaic structures in the verse.                                                                                  | Expanded                |
| `quran-full-parse`       | `RENDERED ARABIC`                           | The Arabic rendering of the verse.                                                                                                                      | Expanded                |
| `quran-full-parse`       | `RENDERED TRANSLITERATION`                  | The transliterated representation of the verse in Roman script.                                                                                         | Expanded                |
| `quran-full-parse`       | `VERSE LENGTH (EXCLUDING QURANIC INITIALS)` | The length of the verse in terms of words, excluding Quranic initials (e.g., `Alif Lam Meem`).                                                          | Expanded                |

---

### **Key Observations**
1. **Compressed Data**:
   - The `PARSING` field contains rich linguistic data encoded in a compressed format, which will require specialized parsing for analysis.
2. **Expanded Fields**:
   - Fields such as `RENDERED ARABIC`, `Translator Yusuf Ali`, and `FORMULAIC-DENSITY-*` provide expanded and directly interpretable data.

---

## **Table name is `dictionary-entries`**
The `dictionary-entries` table acts as a lexicon for the Qur'an, cataloging definitions, transliterations, and related forms of words. It is a foundational resource for both linguistic analysis and translation work.

### **Analysis of the `dictionary-entries` Table**

Below is a detailed analysis and description of each field in the `dictionary-entries` table, with the table name included as a left-hand column.

---

| **Table Name**         | **Field Name**             | **Description**                                                                                                                                                                       |
|-------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dictionary-entries`    | `DICTIONARY ID`           | A unique identifier for each dictionary entry, serving as the primary key for indexing and referencing.                                                                               |
| `dictionary-entries`    | `ENGLISH`                 | The transliterated form of the root or entry in English, providing the base representation for non-Arabic speakers.                                                                   |
| `dictionary-entries`    | `ENGLISH TRANSLITERATED`  | A phonetic representation of the `ENGLISH` field in transliterated form for accurate pronunciation.                                                                                    |
| `dictionary-entries`    | `ENGLISH ALT 1`           | An alternative English transliteration of the entry, offering additional variations or contextual representations.                                                                     |
| `dictionary-entries`    | `ENGLISH ALT 2`           | Another alternative English transliteration, expanding on possible interpretations or orthographic differences.                                                                        |
| `dictionary-entries`    | `ARABIC`                  | The Arabic script of the entry, preserving its original orthography for Quranic and linguistic studies.                                                                                |
| `dictionary-entries`    | `ARABIC FOR SORTING`      | A normalized version of the Arabic script, optimized for computational sorting or indexing.                                                                                           |
| `dictionary-entries`    | `COUNT`                   | The frequency of the root or entry in the Quran, aiding in lexical and thematic analysis.                                                                                              |
| `dictionary-entries`    | `MEANING`                 | A detailed explanation of the root or entry, including its various meanings and semantic nuances in English.                                                                           |
| `dictionary-entries`    | `PENRICE PAGE`            | The page number in Penrice's lexicon where the entry is discussed, providing a reference for deeper linguistic or historical analysis.                                                  |
| `dictionary-entries`    | `LANE PAGE`               | The page number in Lane's lexicon where the entry is detailed, offering a classical Arabic perspective and extended analysis.                                                          |
| `dictionary-entries`    | `TYPE`                    | The classification of the entry, such as `ROOT`, identifying its linguistic or morphological role in the Quranic text.                                                                |

---

### **Key Insights**

1. **Field Relationships**:
   - `DICTIONARY ID` uniquely identifies each entry, linking it to other datasets or tools for further linguistic or thematic exploration.
   - `ARABIC` and `ENGLISH` fields establish a bi-directional mapping between Arabic roots and their English transliterations, aiding cross-linguistic analysis.

2. **Linguistic and Semantic Depth**:
   - The `MEANING` field provides rich semantic insights into the usage and interpretation of Quranic roots, reflecting their versatility and depth.
   - `ENGLISH ALT 1` and `ENGLISH ALT 2` expand on possible transliterations, addressing orthographic variations or alternative phonetic interpretations.

3. **Applications**:
   - Supports lexicon development, enabling computational tools to leverage Quranic vocabulary for searches, translations, or linguistic studies.
   - Acts as a reference for Quranic recitation (tajweed) and thematic analysis by correlating word frequencies (`COUNT`) with their semantic roles.

---

### Example Interpretation of Data:
- **Row 1**:
  - **DICTIONARY ID**: 1
  - **ENGLISH**: `Abb`
  - **ARABIC**: `ابب`
  - **COUNT**: `1`
  - **MEANING**: `Fresh or dry herbage/vegetation of earth/pasture, fruits/vegetables.`
  - Indicates that the root `Abb` appears once in the Quran, with meanings tied to vegetation or agricultural contexts.

- **Row 7**:
  - **DICTIONARY ID**: 7
  - **ENGLISH**: `Aty`
  - **ARABIC**: `اتي`
  - **COUNT**: `549`
  - **MEANING**: `To come, come to; To bring; ... One who gives.`
  - Highlights that `Aty` is a frequently occurring root with a broad semantic range tied to motion, giving, and causation.

---

### Contextual Significance:
1. **Lexical Analysis**:
   - By providing frequencies and detailed meanings, the table facilitates lexical studies focusing on root significance and thematic prominence in the Quran.
2. **Cross-Referencing Classical Sources**:
   - The `PENRICE PAGE` and `LANE PAGE` fields link Quranic roots to classical Arabic lexicons, ensuring historical and linguistic integrity.
3. **Digital Applications**:
   - This table can be integrated into Quranic apps or linguistic databases for efficient root searches, thematic studies, or interlinear text alignment.

---

## **Table name is `root-list`**
The `root-list` table organizes words in the Qur'an by their linguistic roots, which form the basis of the Arabic language. It includes metadata such as occurrences and derivations, aiding in morphological and etymological studies.

### **Analysis of the `Root-list` Table**

Below is the detailed analysis and description of each field in the `Root-list` table, with the table name included as a left-hand column.

---

| **Table Name**      | **Field Name**                 | **Description**                                                                                                                                                                   |
|----------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Root-list`          | `ROOT ID`                     | A unique identifier for each Arabic root entry, serving as the primary key for indexing and referencing.                                                                          |
| `Root-list`          | `ENGLISH`                     | The English transliteration of the root, providing a readable representation for non-Arabic speakers.                                                                            |
| `Root-list`          | `ENGLISH ALT 1`               | An alternative English transliteration of the root, reflecting different transliteration standards or regional variations.                                                        |
| `Root-list`          | `ENGLISH ALT 2`               | Another alternative English transliteration of the root, capturing additional transliteration conventions.                                                                        |
| `Root-list`          | `ENGLISH-BINARY`              | A binary-encoded representation of the transliteration for computational purposes.                                                                                               |
| `Root-list`          | `ARABIC`                      | The Arabic script of the root, preserving its original orthography.                                                                                                              |
| `Root-list`          | `COUNT`                       | The total number of occurrences of the root in the Quran.                                                                                                                        |
| `Root-list`          | `COUNT FIRST`                 | The count of times the root occurs as the first word in a verse.                                                                                                                 |
| `Root-list`          | `COUNT MIDDLE`                | The count of times the root occurs in the middle of a verse.                                                                                                                     |
| `Root-list`          | `COUNT LAST`                  | The count of times the root occurs as the last word in a verse.                                                                                                                  |
| `Root-list`          | `COUNT MECCAN`                | The number of occurrences of the root in Meccan chapters.                                                                                                                        |
| `Root-list`          | `COUNT MEDINAN`               | The number of occurrences of the root in Medinan chapters.                                                                                                                       |
| `Root-list`          | `ENGLISH TRANSLITERATED`      | A phonetic representation of the root, providing a guide to its pronunciation in Roman script.                                                                                   |
| `Root-list`          | `100-COUNT-ALL`               | Normalized frequency of the root per 100 words across the entire Quran.                                                                                                          |
| `Root-list`          | `100-COUNT-MECCAN`            | Normalized frequency of the root per 100 words in Meccan chapters.                                                                                                               |
| `Root-list`          | `100-COUNT-MEDINAN`           | Normalized frequency of the root per 100 words in Medinan chapters.                                                                                                              |
| `Root-list`          | `MEANING`                     | The meaning or semantic range of the root in English, describing its linguistic and contextual significance.                                                                      |
| `Root-list`          | `LETTERS`                     | Specifies whether the root is composed of three or more letters.                                                                                                                 |
| `Root-list`          | `Hapax or Unique`             | Indicates if the root is a hapax legomenon (occurring only once in the Quran) or otherwise unique.                                                                                |
| `Root-list`          | `Unique to Sura`              | Indicates if the root is unique to a specific sura.                                                                                                                              |
| `Root-list`          | `Formula-*`                  | Various fields (`Formula-3-ROOT`, `Formula-4-ROOT`, `Formula-5-ROOT`, etc.) that indicate the root’s role in formulaic patterns of 3, 4, or 5 words.                              |
| `Root-list`          | `Appears in Formulae`         | Indicates whether the root appears in any formulaic structures.                                                                                                                  |
| `Root-list`          | `RENDER_*`                  | Various fields (`RENDER_COUNT_NOUN`, `RENDER_COUNT_VERB`, etc.) that track the grammatical and syntactic occurrences of the root as a noun or verb, broken down by gender, case, etc. |
| `Root-list`          | `PENRICE PAGE`                | The page number in Penrice's lexicon where the root is discussed.                                                                                                                |
| `Root-list`          | `LANE VOLUME`                | The volume number in Lane’s lexicon that contains detailed analysis of the root.                                                                                                 |
| `Root-list`          | `LANE PAGE`                  | The page number in Lane’s lexicon corresponding to the root.                                                                                                                     |
| `Root-list`          | `AFFECTED BY CHANGES`         | Indicates whether the root is affected by textual or orthographic changes in the Quran.                                                                                          |

---

### **Key Insights**

1. **Field Relationships**:
   - `ROOT ID` uniquely identifies each root entry, enabling connections to related datasets.
   - Frequency fields (`COUNT`, `COUNT FIRST`, `COUNT MECCAN`, etc.) provide granular data on root distribution.

2. **Linguistic Analysis**:
   - Formulaic fields highlight the root’s role in specific Quranic patterns.
   - `MEANING` and lexicon references (`PENRICE PAGE`, `LANE PAGE`) offer resources for deeper semantic and linguistic exploration.

3. **Applications**:
   - Supports linguistic studies by analyzing root frequencies, distributions, and roles in formulaic patterns.
   - Facilitates thematic exploration of Quranic vocabulary by linking roots to meanings and occurrences.

---

### Example Interpretation of Data:
- **Row 1**:
  - **ROOT ID**: 1
  - **ARABIC**: `ابب`
  - **COUNT**: 1
  - **MEANING**: `Fresh or dry herbage/vegetation of earth/pasture, fruits/vegetables.`
  - Indicates that the root `ابب` occurs once in the Quran and is classified as a hapax legomenon.

- **Row 5**:
  - **ROOT ID**: 5
  - **ARABIC**: `ابو`
  - **COUNT**: 117
  - **MEANING**: `Father/grandfather/ancestor, fathership/paternity, to nourish/feed/rear, bring up.`
  - Highlights a frequently occurring root, commonly associated with familial terms and nurturing.

---

### Contextual Significance:
1. **Lexical Richness**:
   - Provides insights into the Quran’s vocabulary by highlighting roots’ frequencies, contexts, and semantic ranges.
2. **Interdisciplinary Applications**:
   - Combines linguistic analysis with historical and thematic studies using lexicon references.
3. **Computational Linguistics**:
   - The structured data supports digital tools for Quranic text analysis, such as root-based searches or formulaic density visualizations.

---

### First 10 Rows Example (2025-01-14)
| ROOT ID     | ENGLISH   | ENGLISH ALT 1   | ENGLISH ALT 2   | ENGLISH-BINARY    | ARABIC   |   COUNT |   COUNT FIRST |   COUNT MIDDLE |   COUNT LAST |   COUNT MECCAN |   COUNT MEDINAN | ENGLISH TRANSLITERATED   |   100-COUNT-ALL |   100-COUNT-MECCAN |   100-COUNT-MEDINAN | MEANING                                                                                                                                                                                                                                                                     |   Letters | Hapax or Unique   |   Unique to Sura |   Formula-3-ROOT |   Formula-4-ROOT |   Formula-5-ROOT |   Formula-3-ROOT-ALL |   Formula-4-ROOT-ALL |   Formula-5-ROOT-ALL |   Appears in Formulae |   RENDER_COUNT_NOUN |   RENDER_NOUN_CASE_NOM |   RENDER_NOUN_CASE_ACC |   RENDER_NOUN_CASE_GEN |   RENDER_NOUN_GENDER_MASC |   RENDER_NOUN_GENDER_FEM |   RENDER_NOUN_NUMBER_SINGULAR |   RENDER_NOUN_NUMBER_DUAL |   RENDER_NOUN_NUMBER_PLURAL |   RENDER_COUNT_VERB |   RENDER_VERB_PERSON_1ST |   RENDER_VERB_PERSON_2ND |   RENDER_VERB_PERSON_3RD |   RENDER_VERB_NUMBER_SINGULAR |   RENDER_VERB_NUMBER_DUAL |   RENDER_VERB_NUMBER_PLURAL |   RENDER_VERB_GENDER_MASC |   RENDER_VERB_GENDER_FEM |   RENDER_VERB_FORM_1 |   RENDER_VERB_FORM_2 |   RENDER_VERB_FORM_3 |   RENDER_VERB_FORM_4 |   RENDER_VERB_FORM_5 |   RENDER_VERB_FORM_6 |   RENDER_VERB_FORM_7 |   RENDER_VERB_FORM_8 |   RENDER_VERB_FORM_9 |   RENDER_VERB_FORM_10 |   RENDER_VERB_FORM_11 |   RENDER_VERB_FORM_12 |   PENRICE PAGE |   LANE VOLUME |   LANE PAGE |   AFFECTED BY CHANGES |
|:------------|:----------|:----------------|:----------------|:------------------|:---------|--------:|--------------:|---------------:|-------------:|---------------:|----------------:|:-------------------------|----------------:|-------------------:|--------------------:|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------:|:------------------|-----------------:|-----------------:|-----------------:|-----------------:|---------------------:|---------------------:|---------------------:|----------------------:|--------------------:|-----------------------:|-----------------------:|-----------------------:|--------------------------:|-------------------------:|------------------------------:|--------------------------:|----------------------------:|--------------------:|-------------------------:|-------------------------:|-------------------------:|------------------------------:|--------------------------:|----------------------------:|--------------------------:|-------------------------:|---------------------:|---------------------:|---------------------:|---------------------:|---------------------:|---------------------:|---------------------:|---------------------:|---------------------:|----------------------:|----------------------:|----------------------:|---------------:|--------------:|------------:|----------------------:|
| 1           | Abb       | nan             | nan             | Abb\0\0\0\0\0\0\0 | ابب      |       1 |             0 |              0 |            1 |              1 |               0 | 'bb                      |      0.00200136 |         0.00318878 |           0         | Fresh or dry herbage/vegetation of earth/pasture, fruits/vegetables.                                                                                                                                                                                                        |       nan | HAPAX             |               80 |                0 |                0 |                0 |                    0 |                    0 |                    0 |                     0 |                   1 |                      0 |                      1 |                      0 |                         1 |                        0 |                             1 |                         0 |                           0 |                   0 |                        0 |                        0 |                        0 |                             0 |                         0 |                           0 |                         0 |                        0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                     0 |                     0 |                     0 |             10 |             1 |          39 |                     0 |
| 2           | Abd       | nan             | nan             | Abd\0\0\0\0\0\0\0 | ابد      |      28 |             0 |             23 |            5 |              5 |              23 | 'bd                      |      0.0560381  |         0.0159439  |           0.123616  | He remained/stayed, abode, dwelt constantly/permanently, to render perpetual, time (in an absolute sense), long time, endless/eternal/forever, unlimited/indivisible, lasting/everlasting, unsocial/unfamiliar, never (when used in negative construction).                 |       nan | nan               |                0 |                0 |                0 |                0 |                    0 |                    0 |                    0 |                   248 |                   0 |                      0 |                      0 |                      0 |                         0 |                        0 |                             0 |                         0 |                           0 |                   0 |                        0 |                        0 |                        0 |                             0 |                         0 |                           0 |                         0 |                        0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                     0 |                     0 |                     0 |             10 |             1 |          40 |                     0 |
| 3           | Abq       | nan             | nan             | Abq\0\0\0\0\0\0\0 | ابق      |       1 |             0 |              1 |            0 |              1 |               0 | 'bq                      |      0.00200136 |         0.00318878 |           0         | To run away, fled, went away, he confined/concealed/restricted himself, runaway/fugitive.                                                                                                                                                                                   |       nan | HAPAX             |               37 |                0 |                0 |                0 |                    0 |                    0 |                    0 |                     0 |                   0 |                      0 |                      0 |                      0 |                         0 |                        0 |                             0 |                         0 |                           0 |                   1 |                        0 |                        0 |                        1 |                             1 |                         0 |                           0 |                         1 |                        0 |                    1 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                     0 |                     0 |                     0 |             10 |             1 |          43 |                     0 |
| 4           | Abl       | nan             | nan             | Abl\0\0\0\0\0\0\0 | ابل      |       3 |             0 |              2 |            1 |              3 |               0 | 'bl                      |      0.00600408 |         0.00956633 |           0         | Devote oneself to religious exercises, became a devotee, he overcame/resisted/withstood, camels, acquire camels, camels became numerous, skilled in the good management of camels, herd of camels, flocks, a bundle (e.g. of firewood), a company in a state of dispersion. |       nan | nan               |                0 |                0 |                0 |                0 |                    0 |                    0 |                    0 |                     0 |                   2 |                      0 |                      0 |                      2 |                         2 |                        0 |                             2 |                         0 |                           0 |                   0 |                        0 |                        0 |                        0 |                             0 |                         0 |                           0 |                         0 |                        0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                     0 |                     0 |                     0 |             10 |             1 |          43 |                     0 |
| 5           | Abw       | nan             | nan             | Abw\0\0\0\0\0\0\0 | ابو      |     117 |             5 |            111 |            1 |             94 |              23 | 'bw                      |      0.234159   |         0.299745   |           0.123616  | Father/grandfather/ancestor, fathership/paternity, to nourish/feed/rear, bring up.                                                                                                                                                                                          |       nan | nan               |                0 |                0 |                0 |                0 |                    0 |                    0 |                    0 |                   640 |                 117 |                     48 |                     31 |                     38 |                       117 |                        0 |                            46 |                         7 |                          64 |                   0 |                        0 |                        0 |                        0 |                             0 |                         0 |                           0 |                         0 |                        0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                     0 |                     0 |                     0 |             10 |             1 |          46 |                    12 |
| 6           | Aby       | nan             | nan             | Aby\0\0\0\0\0\0\0 | ابي      |      13 |             0 |             11 |            2 |              7 |               6 | 'by                      |      0.0260177  |         0.0223214  |           0.0322477 | Refuse/refrain/abstain voluntarily, held back, disagree/reject/dislike/disapprove/hate, incompliant/unyielding/resistant.                                                                                                                                                   |       nan | nan               |                0 |                0 |                0 |                0 |                    0 |                    0 |                    0 |                    29 |                   0 |                      0 |                      0 |                      0 |                         0 |                        0 |                             0 |                         0 |                           0 |                  13 |                        0 |                        0 |                       13 |                            11 |                         0 |                           2 |                        11 |                        2 |                   13 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                     0 |                     0 |                     0 |             10 |             1 |          48 |                     0 |
| 7           | Aty       | nan             | nan             | Aty\0\0\0\0\0\0\0 | اتي      |     549 |            28 |            518 |            3 |            344 |             205 | 'ty                      |      1.09875    |         1.09694    |           1.1018    | To come, come to; To bring; to pass, come to pass, come upon; To do, commit; Part.Act = one who comes to; Part.Pass = that which is come to pass; To cause to come, bring, produce, give; The bestowing of gifts; One who gives.                                            |       nan | nan               |                0 |                0 |                0 |                0 |                    0 |                    0 |                    0 |                  3787 |                  14 |                     10 |                      2 |                      2 |                         8 |                        4 |                            12 |                         0 |                           1 |                 535 |                      107 |                      115 |                      313 |                           279 |                         5 |                         251 |                       384 |                       44 |                  264 |                    0 |                    0 |                  271 |                    0 |                    0 |                    0 |                    0 |                    0 |                     0 |                     0 |                     0 |             11 |             1 |          51 |                    12 |
| 8           | Avv       | Athth           | 'thth           | Avv\0\0\0\0\0\0\0 | اثث      |       2 |             0 |              2 |            0 |              2 |               0 | 'vv                      |      0.00400272 |         0.00637755 |           0         | To be luxuriated, close, become much in quantity, abundant, numerous, great, thick or large. athaathan - goods, utensils, household furniture, moveable goods, all property consisting of camels/sheep/goats and abandoned property.                                        |       nan | nan               |                0 |                0 |                0 |                0 |                    0 |                    0 |                    0 |                     0 |                   2 |                      0 |                      2 |                      0 |                         2 |                        0 |                             2 |                         0 |                           0 |                   0 |                        0 |                        0 |                        0 |                             0 |                         0 |                           0 |                         0 |                        0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                     0 |                     0 |                     0 |             11 |             1 |          53 |                     0 |
| 9           | Avr       | Athr            | 'thr            | Avr\0\0\0\0\0\0\0 | اثر      |      21 |             1 |             19 |            1 |             17 |               4 | 'vr                      |      0.0420286  |         0.0542092  |           0.0214984 | To relate, narrate, recite, choose, propose, transmit, raise, prefer, effect, excite.  \nTo stir up, to trump up.                                                                           \nDetermined/resolved/decided upon a thing.                                                          \nOrigin, time/period of life.                                                                       \nDearth, scarcity, drought or sterility.                                                            \nAn iron instrument with which the bottom of a camel's foot is marked, or a camel with such a mark. \nA generous quality/action (e.g. passed down from generation to generation).                       |  | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 32 | 15 | 0 | 3 | 12 | 14 | 1 | 5 | 0 | 10 | 6 | 1 | 1 | 4 | 3 | 0 | 3 | 5 | 0 | 1 | 0 | 0 | 5 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 11 | 1 | 54 | 0|
| 10          | Avl       | Athl            | 'thl            | Avl\0\0\0\0\0\0\0 | اثل      |       1 |             0 |              1 |            0 |              1 |               0 | 'vl                      |      0.00200136 |         0.00318878 |           0         | To take root, be firmly rooted, walk at a quick pace.                                                                                                                                                                                                                       |       nan | HAPAX             |               34 |                0 |                0 |                0 |                    0 |                    0 |                    0 |                     0 |                   1 |                      0 |                      0 |                      1 |                         1 |                        0 |                             1 |                         0 |                           0 |                   0 |                        0 |                        0 |                        0 |                             0 |                         0 |                           0 |                         0 |                        0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                    0 |                     0 |                     0 |                     0 |             11 |             1 |          57 |                     0 |

---

## **Table name is `sura-data`**
This table provides metadata about each sura (chapter) in the Qur'an, including the number of verses, thematic classification, and provenance (Meccan or Medinan). It serves as a guide to the structural organization of the Qur'an.

### **Analysis of the `sura-data` Table**

Below is the detailed analysis and description of each field in the `sura-data` table, with the table name included as a left-hand column.

---

| **Table Name**       | **Field Name**              | **Description**                                                                                                                                             |
|-----------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sura-data`           | `Sura Number`              | The chapter number of the Quran, uniquely identifying each sura.                                                                                            |
| `sura-data`           | `Verses`                   | The number of verses in the sura.                                                                                                                           |
| `sura-data`           | `Words`                    | The total number of words in the sura.                                                                                                                      |
| `sura-data`           | `English Name`             | The English name of the sura, commonly used in translations and interpretations.                                                                             |
| `sura-data`           | `Arabic Name`              | The name of the sura in Arabic script, preserving its original orthography.                                                                                  |
| `sura-data`           | `Alternative Name 1`       | An alternative transliterated name of the sura, reflecting a common variant.                                                                                 |
| `sura-data`           | `Alternative Name 2`       | Another alternative transliterated name of the sura, providing additional variants for identification.                                                       |
| `sura-data`           | `Provenance`               | Indicates whether the sura originated in Mecca (`Meccan`) or Medina (`Medinan`), reflecting its historical and contextual background.                        |
| `sura-data`           | `Durie Classification`     | A classification system for suras based on their thematic and linguistic characteristics, such as `PRE-TRANSITIONAL` or `POST-TRANSITIONAL`.                 |
| `sura-data`           | `Parsed Flag`              | Indicates whether the sura has been fully parsed for linguistic analysis (`1` for yes, `0` for no).                                                          |
| `sura-data`           | `Root Count Different`     | The number of different roots found in the sura, highlighting its lexical diversity.                                                                         |
| `sura-data`           | `Root Count Unique`        | The count of roots unique to the sura, reflecting its distinct linguistic features.                                                                          |
| `sura-data`           | `Root Count Hapax`         | The number of hapax legomena (roots that occur only once) in the sura.                                                                                       |
| `sura-data`           | `Hapax per 100 Words`      | The frequency of hapax legomena per 100 words, providing a normalized measure of lexical rarity.                                                             |
| `sura-data`           | `Manuscripts`              | The number of Quranic manuscripts that include this sura, relevant for textual studies and historical analysis.                                              |
| `sura-data`           | `COUNT_NOUN`               | The total count of nouns in the sura, providing insights into its grammatical structure and thematic focus.                                                   |

---

### **Key Insights**

1. **Field Relationships**:
   - `Sura Number` uniquely identifies each sura and serves as the primary reference key.
   - `Provenance` and `Durie Classification` provide historical and thematic context, enriching interpretive and comparative studies.

2. **Linguistic Analysis**:
   - Fields like `Root Count Different`, `Root Count Unique`, and `Root Count Hapax` quantify the lexical diversity and uniqueness of each sura.
   - `Hapax per 100 Words` normalizes the occurrence of rare words, enabling cross-sura comparisons.

3. **Applications**:
   - Facilitates thematic, linguistic, and historical studies of Quranic chapters.
   - Enables computational tools to analyze Quranic vocabulary, grammar, and stylistic patterns.

---

### Example Interpretation of Data:
- **Row 1**:
  - **Sura Number**: 1
  - **English Name**: `The Opening`
  - **Arabic Name**: `الفاتحة`
  - **Provenance**: `Meccan`
  - **Root Count Unique**: `0`
  - **Hapax per 100 Words**: `0`
  - Indicates that the sura `The Opening` has no unique roots and contains no hapax legomena, reflecting its brevity and foundational nature.

- **Row 2**:
  - **Sura Number**: 2
  - **English Name**: `The Cow`
  - **Root Count Different**: `585`
  - **Root Count Hapax**: `22`
  - **Hapax per 100 Words**: `0.245258`
  - Highlights the extensive lexical richness of `The Cow` and its thematic complexity.

---

### Contextual Significance:
1. **Thematic and Historical Insights**:
   - `Provenance` and `Durie Classification` help place suras in their historical and thematic context, reflecting the Quran's development.
2. **Lexical Richness**:
   - Fields like `Root Count Different` and `COUNT_NOUN` provide quantitative measures of linguistic complexity and thematic density.
3. **Digital Applications**:
   - The table supports Quranic tools that analyze vocabulary, track rare words, and visualize thematic trends.

---

### First 10 Rows Example (2025-01-14)
|   Sura Number |   Verses |   Words | English Name        | Arabic Name   | Alternative Name 1   | Alternative Name 2   | Provenance   | Durie Classification   |   Parsed Flag |   Root Count Different |   Root Count Unique |   Root Count Hapax |   Hapax per 100 Words |   Manuscripts |   COUNT_NOUN |
|--------------:|---------:|--------:|:--------------------|:--------------|:---------------------|:---------------------|:-------------|:-----------------------|--------------:|-----------------------:|--------------------:|-------------------:|----------------------:|--------------:|-------------:|
|             1 |        7 |      29 | The Opening         | al-F?ti?ah    | Al Fatihah           | al-F?ti?ah           | Meccan       | PRE-TRANSITIONAL       |            33 |                     18 |                   0 |                  0 |              0        |             6 |           12 |
|             2 |      286 |    6116 | The Cow             | al-Baqara     | Al Baqarah           | al-Baqara            | Medinan      | POST-TRANSITIONAL      |            33 |                    585 |                  22 |                 18 |              0.245258 |            22 |         1860 |
|             3 |      200 |    3481 | The Family of Imran | ?l-?Imr?n     | Al Imran             | ?l-?Imr?n            | Medinan      | POST-TRANSITIONAL      |            33 |                    439 |                   8 |                  6 |              0.143637 |            21 |         1083 |
|             4 |      176 |    3747 | The Women           | al-Nis??      | Al-Nisa'             | al-Nis??             | Medinan      | POST-TRANSITIONAL      |            33 |                    462 |                  17 |                 13 |              0.320256 |            30 |         1140 |
|             5 |      120 |    2804 | The Table Spread    | al-M??idah    | Al Ma'idah           | al-M??idah           | Medinan      | POST-TRANSITIONAL      |            33 |                    422 |                  13 |                 11 |              0.356633 |            36 |          868 |
|             6 |      165 |    3050 | The Cattle          | al-An??m      | al-An??m             | nan                  | Meccan       | PRE-TRANSITIONAL       |            33 |                    421 |                  11 |                  7 |              0.229508 |            37 |          943 |
|             7 |      206 |    3320 | The Heights         | al-A?r?f      | Al-A'raf             | al-A?r?f             | Meccan       | PRE-TRANSITIONAL       |            33 |                    477 |                  14 |                 13 |              0.331325 |            31 |         1010 |
|             8 |       75 |    1233 | The Spoils of War   | al-Anf?l      | al-Anf?l             | nan                  | Medinan      | POST-TRANSITIONAL      |            33 |                    266 |                   5 |                  5 |              0.405515 |            24 |          361 |
|             9 |      129 |    2498 | Repentance          | al-Tawbah     | Al-Bara'a            | al-Tawbah            | Medinan      | POST-TRANSITIONAL      |            33 |                    366 |                  12 |                  9 |              0.280224 |            28 |          753 |
|            10 |      109 |    1833 | Jonah               | Y?nus         | Y?nus                | nan                  | Meccan       | PRE-TRANSITIONAL       |            33 |                    290 |                   0 |                  0 |              0        |            26 |          550 |

---

## **Table name is `intertextual links`**
The `intertextual links` table documents references and connections between Qur'anic verses and external texts or traditions. It includes source details, bibliographic references, and text comparisons, supporting studies on the Qur'an's historical and literary context.

### **Analysis of the `intertextual links` Table**

Below is the detailed analysis and description of each field in the `intertextual links` table, with the table name included as a left-hand column.

---

### Column Descriptions for the Table `intertextual links`

| **Table Name**        | **Column Name**   | **Description**                                                                                                                                                                                                                               |
|------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intertextual links`   | `INTERTEXT ID`   | A unique identifier for each intertextual link, serving as the primary key for the table.                                                                                                                                                |
| `intertextual links`   | `SURA`           | The sura (chapter) number of the Qur'an where the intertextual reference begins.                                                                                                                                                           |
| `intertextual links`   | `START VERSE`    | The specific verse in the sura where the intertextual reference starts.                                                                                                                                                                   |
| `intertextual links`   | `END VERSE`      | The specific verse in the sura where the intertextual reference ends.                                                                                                                                                                     |
| `intertextual links`   | `SOURCE`         | The abbreviated name of the intertextual source text or tradition that is being referenced. Examples include `IGT` (Infancy Gospel of Thomas) or `CAVE` (The Revolt of Satan).                                                             |
| `intertextual links`   | `SOURCE REF`     | A reference to the chapter and verses within the source text or tradition being cited. This provides context for the intertextual connection.                                                                                              |
| `intertextual links`   | `TEXT`           | The detailed text of the intertextual reference, often containing narrative or descriptive content related to the specific connection with the Qur'anic verses.                                                                             |
| `intertextual links`   | `BIBLIOGRAPHY`   | A bibliographic citation or reference for the source text, providing additional details about its origin, publication, or historical context.                                                                                              |

### Example Breakdown of Field Content

1. **INTERTEXT ID**: Unique identifiers like `0`, `1`, `3`, etc.
2. **SURA**: `5`, `2`, `7`, etc., indicating the Qur'anic chapter.
3. **START VERSE**: Specific verse numbers like `110`, `34`.
4. **END VERSE**: Ending verse numbers, same or different as `START VERSE`.
5. **SOURCE**: `IGT`, `CAVE`, `GOSBART`, etc.
6. **SOURCE REF**: References like `Chapter 2:1-7`, `Chapter 36:1-7`.
7. **TEXT**: Full passages with detailed descriptions of events or narratives.
8. **BIBLIOGRAPHY**: Bibliographic details for external sources.

---

### **Key Insights**

1. **Field Relationships**:
   - `ID` uniquely identifies each intertextual link for clear referencing.
   - `SURA`, `VERSE START`, and `VERSE END` collectively identify the specific Quranic verses linked to the intertextual source.
   - `SOURCE ID` ties the link to a source table for further metadata about the source (e.g., language, publication date).

2. **Content Utility**:
   - `EXCERPT` provides users with context by showing the actual text from the intertextual source, allowing for direct comparison with Quranic verses.
   - `SOURCE TITLE` offers a clear label for the source, enhancing user understanding of its origin or significance.

3. **Applications**:
   - Supports intertextual analysis by connecting Quranic verses to relevant external sources.
   - Enables thematic and linguistic studies of shared narratives across religious or historical texts.

---

### Example Interpretation of Data:
- **Row 1**:
  - **ID**: 0
  - **SURA**: 5
  - **VERSE START**: 110
  - **VERSE END**: 110
  - **SOURCE ID**: `IGT`
  - **SOURCE TITLE**: `Chapter 2:1-7`
  - **EXCERPT**: `V1 When the boy Jesus was five years old...`
  - Indicates a link between Quranic verse 5:110 and an excerpt from `IGT`, describing an event from the life of Jesus.

- **Row 7**:
  - **ID**: 7
  - **SURA**: 18
  - **VERSE START**: 50
  - **VERSE END**: 50
  - **SOURCE ID**: `CAVE`
  - **SOURCE TITLE**: `The First Thousand Years: The Revolt of Satan`
  - **EXCERPT**: `And when the prince of the lower order of angels saw what great majesty had been given unto Adam...`
  - Highlights a connection between Quranic verse 18:50 and a narrative from `CAVE` about Satan’s revolt.

---

### Contextual Significance:
1. **Intertextual Studies**:
   - Facilitates the exploration of shared narratives between the Quran and other historical or religious texts.
2. **Narrative Context**:
   - The `EXCERPT` field allows users to view related passages, providing deeper understanding and comparative analysis.
3. **Digital Applications**:
   - Powers features like linking Quranic verses to relevant sources in digital study tools, enabling users to navigate intertextual relationships seamlessly.

---

## **Table name is `proper-noun-list`**
The `proper-noun-list` table catalogs proper nouns found in the Qur'an, along with their transliterations, alternative spellings, and associated Arabic script. This dataset is instrumental in identifying and analyzing references to key individuals, places, and entities within the text.

### **Analysis of the `proper-noun-list` Table**

Below is the detailed analysis and description of each field in the `proper-noun-list` table, with the table name included as a left-hand column.

---

| **Table Name**         | **Field Name**          | **Description**                                                                                                                                          |
|-------------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `proper-noun-list`      | `PROPER NOUN ID`       | A unique identifier for each proper noun in the list, serving as the primary key for indexing and referencing.                                            |
| `proper-noun-list`      | `ENGLISH`              | The English transliteration of the proper noun, providing a readable representation of the noun for non-Arabic speakers.                                  |
| `proper-noun-list`      | `ENGLISH-BINARY`       | A binary-encoded representation of the English transliteration, optimized for computational processing and sorting.                                       |
| `proper-noun-list`      | `ARABIC`               | The Arabic script representation of the proper noun, preserving the original orthography.                                                                |
| `proper-noun-list`      | `ROOT`                 | The root letters associated with the proper noun, reflecting its morphological base in Arabic linguistics.                                                |
| `proper-noun-list`      | `ROOT-BINARY`          | A binary-encoded representation of the root, optimized for computational processing and analysis.                                                         |
| `proper-noun-list`      | `COUNT`                | The frequency of the proper noun in the Quran, indicating how many times it appears.                                                                      |
| `proper-noun-list`      | `ENGLISH TRANSLITERATED`| A phonetic representation of the proper noun in Roman script, aiding in accurate pronunciation and analysis.                                               |
| `proper-noun-list`      | `GLOSS`                | A brief explanation or translation of the proper noun, providing contextual meaning (e.g., Shaytan for Satan, Injil for Gospel).                          |
| `proper-noun-list`      | `LOOK UP VIA`          | Specifies the method of lookup for the proper noun, such as `ROOT` or `LEMMA`, linking it to linguistic and semantic contexts.                            |

---

### **Key Insights**

1. **Field Relationships**:
   - `PROPER NOUN ID` uniquely identifies each noun and links it to related linguistic or semantic information.
   - `ROOT` and `ROOT-BINARY` provide the morphological foundation, essential for Quranic studies and lexicon analysis.

2. **Linguistic Utility**:
   - Fields like `ENGLISH`, `ENGLISH-BINARY`, and `ENGLISH TRANSLITERATED` facilitate accessibility for non-Arabic speakers while preserving phonetic and orthographic accuracy.
   - `GLOSS` provides a semantic explanation, bridging linguistic and thematic studies.

3. **Applications**:
   - Supports Quranic tools for proper noun searches, linguistic analysis, and thematic studies.
   - Enables computational tools to map Arabic roots to proper nouns and their meanings.

---

### Example Interpretation of Data:
- **Row 1**:
  - **PROPER NOUN ID**: 1
  - **ENGLISH**: `$ayoTa'n`
  - **ARABIC**: `????????`
  - **COUNT**: `80`
  - **GLOSS**: `Shaytan (Satan)`
  - Represents "Shaytan," a frequently mentioned entity in the Quran, appearing 80 times and linked to the root `$Tn`.

- **Row 10**:
  - **PROPER NOUN ID**: 10
  - **ENGLISH**: `<isoHaAq`
  - **ARABIC**: `????????`
  - **COUNT**: `17`
  - **GLOSS**: `Isaac`
  - Indicates the proper noun "Isaac," which appears 17 times in the Quran.

---

### Contextual Significance:
1. **Thematic and Linguistic Insights**:
   - Fields like `ROOT` and `COUNT` help identify the significance of proper nouns and their lexical relationships in the Quran.
2. **Cross-Linguistic Applications**:
   - By combining `ENGLISH TRANSLITERATED` and `GLOSS`, the table bridges Arabic proper nouns with their English equivalents for interfaith and linguistic studies.
3. **Computational Use**:
   - Binary fields like `ENGLISH-BINARY` and `ROOT-BINARY` enable efficient storage and processing for large-scale Quranic databases.

---

### First 10 Rows Example (2025-01-14)
|   PROPER NOUN ID | ENGLISH     | ENGLISH-BINARY                                          | ARABIC      | ROOT   | ROOT-BINARY              |   COUNT | ENGLISH TRANSLITERATED   | GLOSS           | LOOK UP VIA   |
|-----------------:|:------------|:--------------------------------------------------------|:------------|:-------|:-------------------------|--------:|:-------------------------|:----------------|:--------------|
|                1 | $ayoTa`n    | $ayoTa`n\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0    | ????????    | sh?n   | $Tn\0\0\0\0\0\0\0\0\0    |      80 | shay??n                  | Shaytan (Satan) | ROOT          |
|                2 | $uEayob     | $uEayob\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0   | ???????     | nan    | \0\0\0\0\0\0\0\0\0\0\0\0 |      11 | shu?ayb                  | Shu?ayb         | LEMMA         |
|                3 | $~iEoraY`   | $~iEoraY`\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0     | ?????????   | $Er    | $Er\0\0\0\0\0\0\0\0\0    |       1 | shi?ra                   | Sirius          | LEMMA         |
|                4 | <iboliys    | <iboliys\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0    | ????????    | nan    | \0\0\0\0\0\0\0\0\0\0\0\0 |      11 | ibl?s                    | Iblis           | LEMMA         |
|                5 | <iboraAhiym | <iboraAhiym\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0       | ??????????? | nan    | \0\0\0\0\0\0\0\0\0\0\0\0 |      69 | ibr?h?m                  | Ibrahim         | LEMMA         |
|                6 | <idoriys    | <idoriys\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0    | ????????    | nan    | \0\0\0\0\0\0\0\0\0\0\0\0 |       2 | idr?s                    | Idris           | LEMMA         |
|                7 | <iloyaAs    | <iloyaAs\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0    | ????????    | nan    | \0\0\0\0\0\0\0\0\0\0\0\0 |       3 | ily?s                    | Elias (Elijah)  | LEMMA         |
|                8 | <injiyl     | <injiyl\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0   | ???????     | nan    | \0\0\0\0\0\0\0\0\0\0\0\0 |      12 | inj?l                    | Injil (Gospel)  | LEMMA         |
|                9 | <iram       | <iram\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0 | ?????       | nan    | \0\0\0\0\0\0\0\0\0\0\0\0 |       1 | iram                     | Iram            | LEMMA         |
|               10 | <isoHaAq    | <isoHaAq\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0\0    | ????????    | nan    | \0\0\0\0\0\0\0\0\0\0\0\0 |      17 | is??q                    | Is??q (Isaac)   | LEMMA         |

---

## **Table name is `stats-suras`**
This table provides statistical data on each sura, including verse and word counts, provenance (Meccan or Medinan), and additional metrics like formulaic density and root frequencies. It is essential for analyzing the structural and linguistic complexity of the Qur'anic chapters.

### **Analysis of the `stats-suras` Table**

Below is the detailed analysis and description of each field in the `stats-suras` table, with the table name included as a left-hand column.

---

| **Table Name**   | **Field Name** | **Description**                                                                                                                                     |
|-------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `stats-suras`     | `ID`           | A unique identifier for each record in the table, serving as the primary key for indexing and referencing.                                          |
| `stats-suras`     | `SURA`         | The chapter number (sura) in the Quran that was accessed by the user.                                                                               |
| `stats-suras`     | `USER ID`      | The unique identifier of the user who accessed the sura, enabling user-specific analytics and tracking.                                              |
| `stats-suras`     | `ACCESS DATE`  | The date when the sura was accessed by the user, providing temporal context for usage tracking and trend analysis.                                    |

---

### **Key Insights**

1. **Field Relationships**:
   - `ID` uniquely identifies each access record, ensuring data integrity for logging and analysis.
   - `USER ID` links access events to specific users, enabling personalized or aggregate usage tracking.

2. **Usage Tracking**:
   - The combination of `SURA`, `USER ID`, and `ACCESS DATE` allows for precise tracking of Quranic sura access patterns over time.
   - Useful for identifying popular suras and peak access periods.

3. **Applications**:
   - Enables user behavior analysis, such as identifying frequently accessed suras or recurring user patterns.
   - Supports engagement metrics for Quranic tools, highlighting chapters of interest across different users or timeframes.

---

### Example Interpretation of Data:
- **Row 1**:
  - **ID**: 1
  - **SURA**: 3
  - **USER ID**: 3
  - **ACCESS DATE**: `2021-12-07`
  - Indicates that user with ID 3 accessed sura 3 (The Family of Imran) on December 7, 2021.

- **Row 6**:
  - **ID**: 6
  - **SURA**: 4
  - **USER ID**: 3
  - **ACCESS DATE**: `2021-12-16`
  - Indicates that the same user accessed sura 4 (The Women) on December 16, 2021.

---

### Contextual Significance:
1. **User Engagement Insights**:
   - Track individual or group engagement with specific Quranic chapters to identify user preferences or study patterns.
2. **Temporal Analysis**:
   - The `ACCESS DATE` field provides insights into when users engage with the Quranic text, helping optimize tools for peak usage periods.
3. **Personalized Recommendations**:
   - By analyzing `USER ID` and `SURA`, the table supports personalized Quranic study recommendations based on historical access patterns.

---

### First 10 Rows Example (2025-01-14)
|   ID |   SURA |   USER ID | ACCESS DATE   |
|-----:|-------:|----------:|:--------------|
|    1 |      3 |         3 | 2021-12-07    |
|    2 |      3 |         3 | 2021-12-07    |
|    3 |      2 |         3 | 2021-12-16    |
|    4 |      2 |         3 | 2021-12-16    |
|    5 |      3 |         3 | 2021-12-16    |
|    6 |      4 |         3 | 2021-12-16    |
|    7 |      5 |         3 | 2021-12-16    |
|    8 |      6 |         3 | 2021-12-16    |
|    9 |      9 |         3 | 2021-12-16    |
|   10 |     10 |         3 | 2021-12-16    |

---

## **Table name is `buckwalter-encoding`**
The `buckwalter-encoding` table serves as a reference for transliterating Arabic text into Latin characters using the Buckwalter system. This standardized mapping is widely used in computational linguistic studies and text processing of Arabic.

### **Analysis of the `buckwalter-encoding` Table**

Below is the detailed analysis and description of each field in the `buckwalter-encoding` table, with the table name included as a left-hand column.

---

| **Table Name**           | **Field Name** | **Description**                                                                                                                                      |
|---------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `buckwalter-encoding`     | `GLYPH`        | The Arabic script character (glyph) represented in its original orthography.                                                                        |
| `buckwalter-encoding`     | `ASCII`        | The corresponding ASCII character used in the Buckwalter Transliteration system to represent the Arabic glyph.                                        |
| `buckwalter-encoding`     | `DESCRIPTION`  | A textual explanation of the glyph, describing its phonetic or linguistic role (e.g., `Hamza`, `Alif + HamzaAbove`).                                 |
| `buckwalter-encoding`     | `UNICODE`      | The Unicode hexadecimal value for the Arabic glyph, ensuring standardization and compatibility in digital applications.                               |

---

### **Key Insights**

1. **Field Relationships**:
   - `GLYPH` and `ASCII` together establish the mapping between Arabic script characters and their transliterated ASCII equivalents, forming the core of the Buckwalter encoding system.
   - `UNICODE` provides the official digital representation of the Arabic character, ensuring cross-platform consistency.

2. **Applications**:
   - Supports transliteration and text normalization in computational linguistics, enabling seamless conversion between Arabic script and ASCII.
   - Facilitates text processing, search, and storage in digital applications by leveraging the `UNICODE` field for standardized character encoding.

3. **Linguistic Utility**:
   - `DESCRIPTION` provides contextual information about each glyph, aiding in understanding its linguistic role, such as distinctions between `Hamza` and `Alif + HamzaAbove`.

---

### Example Interpretation of Data:
- **Row 1**:
  - **GLYPH**: `?`
  - **ASCII**: `'`
  - **DESCRIPTION**: `Hamza`
  - **UNICODE**: `0621`
  - Represents the Arabic `Hamza` character, encoded as `'` in ASCII and `0621` in Unicode.

- **Row 4**:
  - **GLYPH**: `?`
  - **ASCII**: `<`
  - **DESCRIPTION**: `Alif + HamzaBelow`
  - **UNICODE**: `0625`
  - Represents the character `Alif` with `HamzaBelow`, transliterated as `<` in Buckwalter encoding.

---

### Contextual Significance:
1. **Standardization and Compatibility**:
   - The `UNICODE` field ensures that Arabic characters are stored and processed consistently across platforms and applications.
2. **Transliteration and Text Processing**:
   - The `ASCII` field facilitates transliteration into ASCII, making Arabic text more accessible for computational processing and storage.
3. **Linguistic Research**:
   - The table supports linguistic studies by providing a clear mapping between Arabic script and its phonetic or semantic representations.

---

### First 10 Rows Example (2025-01-14)
| GLYPH   | ASCII   | DESCRIPTION       | UNICODE   |
|:--------|:--------|:------------------|:----------|
| ?       | '       | Hamza             | 0621      |
| ?       | >       | Alif + HamzaAbove | 0623      |
| ?       | &       | Waw + HamzaAbove  | 0624      |
| ?       | <       | Alif + HamzaBelow | 0625      |
| ?       | }       | Ya + HamzaAbove   | 0626      |
| ?       | A       | Alif              | 0627      |
| ?       | b       | Ba                | 0628      |
| ?       | p       | Ta Marbuta        | 0629      |
| ?       | t       | Ta                | 062A      |
| ?       | v       | Tha               | 062B      |

---

## **Table name is `help-page-links`**
This table contains metadata about help pages, including titles and URLs, allowing for easy navigation and access to user guides. It serves as a resource for assisting users in understanding system functionalities and features.

### **Analysis of the `help-page-links` Table**

Below is the detailed analysis and description of each field in the `help-page-links` table, with the table name included as a left-hand column.

---

| **Table Name**        | **Field Name**      | **Description**                                                                                                                           |
|------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `help-page-links`      | `QT PAGE TITLE`    | The title of the help page or article, describing its purpose or content in relation to the Qur’an Tools (QT) application.               |
| `help-page-links`      | `ARTICLE URL`      | The URL of the help page, providing a direct link to the corresponding article or guide within the Qur’an Tools application.              |

---

### **Key Insights**

1. **Field Relationships**:
   - The `QT PAGE TITLE` field serves as a descriptive label for the help page, enabling users to understand the content and purpose of the linked resource.
   - The `ARTICLE URL` field provides a direct link to the resource, supporting efficient navigation within the application.

2. **Applications**:
   - This table is central to managing help documentation and improving user accessibility by linking features to detailed explanations or guides.
   - Supports dynamic menu creation or search functionality within the application, allowing users to quickly locate relevant help topics.

3. **Content Management**:
   - The combination of fields ensures seamless integration of help documentation, making it easy to update or expand the resources.

---

### Example Interpretation of Data:
- **Row 1**:
  - **QT PAGE TITLE**: `Analyse Root Position in Verse`
  - **ARTICLE URL**: `/help/analyse-root-position.php`
  - Represents a help page that explains how to analyze root positions within Quranic verses.

- **Row 4**:
  - **QT PAGE TITLE**: `Chart of Average Word Length per Sura`
  - **ARTICLE URL**: `/help/average-word-length-per-sura-chart.php`
  - Links to a page that provides a chart analyzing the average word length across Quranic suras.

---

### First 10 Rows Example (2025-01-14)
| QT PAGE TITLE                                                | ARTICLE URL                                                 |
|:-------------------------------------------------------------|:------------------------------------------------------------|
| Analyse Root Position in Verse                               | /help/analyse-root-position.php                             |
| Bookmarks Manager                                            | /help/bookmarks-manager.php                                 |
| Browse Intertextual Connections                              | /help/browse-intertextual-connections.php                   |
| Chart of Average Word Length per Sura                        | /help/average-word-length-per-sura-chart.php                |
| Chart of Formulae Used per Sura                              | /help/number-of-formulae-used-per-sura-chart.php            |
| Chart of Formulaic Density by Sura                           | /help/formulaic-density-by-sura-chart.php                   |
| Chart of Grammatical Features By Sura                        | /help/grammatical-features-by-sura-chart.php                |
| Chart of Intertextual Links per Source                       | /help/chart-of-intertextual-links-per-source.php            |
| Chart of Number of Different Verse Endings (Rhymes) per Sura | /help/number-of-different-verse-endings-rhymes-per-sura.php |
| Chart of Number of Loanwords per Sura                        | /help/foreign-words-vocabulary-per-sura-chart.php           |

---

### Contextual Significance:
1. **User Guidance**:
   - This table serves as a directory for users to access detailed guides on specific features, such as analyzing grammatical features or intertextual connections.
2. **Ease of Navigation**:
   - By mapping titles to URLs, the table enables intuitive navigation within the Qur’an Tools application, enhancing the user experience.
3. **Documentation Management**:
   - Facilitates the management and updating of help resources, ensuring they remain relevant and accessible.

---

## **Table name is `intertextual sources`**
The `intertextual sources` table documents connections between Qur'anic verses and external texts, providing bibliographic references and source language data. This table supports comparative studies, highlighting the intertextuality of the Qur'an with earlier scriptures and traditions.

### **Analysis of the `intertextual sources` Table**

Below is the detailed analysis and description of each field in the `intertextual sources` table, with the table name included as a left-hand column.

---

| **Table Name**             | **Field Name**            | **Description**                                                                                                                                                                                                                                                                                                         |
|-----------------------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intertextual sources`      | `SOURCE ID`              | A unique identifier for each intertextual source, typically an abbreviation or short form of the source's name.                                                                                                                                                                                                         |
| `intertextual sources`      | `SOURCE NAME`            | The full name of the intertextual source, such as `1 Samuel` or `The Story of Ahikar`, providing a clear reference for users.                                                                                                                                                                                           |
| `intertextual sources`      | `SOURCE ALTERNATIVE NAME`| An alternative or historical name for the source, helping users identify the source under different names or translations.                                                                                                                                                                                              |
| `intertextual sources`      | `SOURCE LANGUAGE`        | The language(s) of the source (e.g., Hebrew, Greek, Syriac), reflecting its original or most significant textual form.                                                                                                                                                                                                  |
| `intertextual sources`      | `SOURCE DATE`            | A textual representation of the approximate date of the source, often including ranges or eras (e.g., `5th Century BC`, `Late 1st Century AD`).                                                                                                                                                                        |
| `intertextual sources`      | `SOURCE DATE NUMERIC`    | A numerical representation of the approximate date of the source, useful for sorting and computational analysis (e.g., `-700` for 700 BC, `500` for 500 AD).                                                                                                                                                           |
| `intertextual sources`      | `SOURCE URL`             | A URL linking to the source's full text or additional information, providing users direct access to further study or context.                                                                                                                                                                                           |
| `intertextual sources`      | `PUBLISHED SOURCE`       | The bibliographic reference or publication details for the source, including editors, titles, and publication dates, often formatted with HTML for emphasis (e.g., `<i>The Story of Ahikar</i>`).                                                                                                                       |
| `intertextual sources`      | `VERSE REFERENCES`       | A list of Quranic verse references (e.g., `2:246-247`) where the source is intertextually linked, highlighting the relationship between the Quran and the source.                                                                                                                                                        |

---

### **Key Insights**

1. **Field Relationships**:
   - `SOURCE ID` and `SOURCE NAME` uniquely identify and describe each source, enabling clear referencing.
   - `VERSE REFERENCES` links the Quranic verses to intertextual sources, supporting comparative studies and thematic analysis.

2. **Temporal and Linguistic Context**:
   - `SOURCE DATE` and `SOURCE DATE NUMERIC` provide historical context, making it easier to analyze sources chronologically.
   - `SOURCE LANGUAGE` highlights the linguistic diversity of intertextual sources, reflecting the Quran's engagement with a variety of textual traditions.

3. **Applications**:
   - Enables intertextual analysis of Quranic verses by linking them to external texts.
   - Facilitates bibliographic and textual studies through the `PUBLISHED SOURCE` and `SOURCE URL` fields.

---

### Example Interpretation of Data:
- **Row 1**:
  - **SOURCE ID**: `1SAMUEL`
  - **SOURCE NAME**: `1 Samuel`
  - **SOURCE LANGUAGE**: `Hebrew`
  - **SOURCE DATE**: `6th-8th Centuries BC`
  - **VERSE REFERENCES**: `2:246-247;2:250-251`
  - Links the Quranic verses 2:246-247 and 2:250-251 to the intertextual source `1 Samuel`, written in Hebrew during the 6th-8th Centuries BC.

- **Row 8**:
  - **SOURCE ID**: `ALEXANDER`
  - **SOURCE NAME**: `The Alexander Legend`
  - **SOURCE DATE**: `629-630AD`
  - **SOURCE LANGUAGE**: `Syriac`
  - **VERSE REFERENCES**: `18:83;18:86;18:93-97;21:96`
  - Relates verses about the Quranic Alexander (Dhul-Qarnayn) to the Syriac `Alexander Legend` from 629-630 AD.

---

### Contextual Significance:
1. **Historical and Thematic Analysis**:
   - This table allows researchers to explore historical contexts and thematic overlaps between the Quran and other texts.
2. **Bibliographic Reference**:
   - Fields like `PUBLISHED SOURCE` and `SOURCE URL` provide access to high-quality references for academic study.
3. **Interfaith and Comparative Studies**:
   - Enables the exploration of shared narratives and concepts between the Quran and other religious or historical texts.

---

## **Table name is `tooltip-text`**
This table contains text for tooltips displayed in the system, providing concise explanations of features or data points. It enhances the user interface by offering quick and context-sensitive help.

### **Analysis of the `tooltip-text` Table**

Below is the detailed analysis and description of each field in the `tooltip-text` table, with the table name included as a left-hand column.

---

| **Table Name**      | **Field Name**        | **Description**                                                                                                                                                                                                                     |
|----------------------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tooltip-text`       | `ID`                 | A unique identifier for each tooltip, serving as the primary key for indexing and referencing.                                                                                                                                      |
| `tooltip-text`       | `NAME`               | A short, descriptive name for the tooltip, often corresponding to a specific feature or functionality within the Qur’an Gateway application.                                                                                        |
| `tooltip-text`       | `TITLE TEXT`         | The title of the tooltip, providing a concise summary of its purpose or the associated feature.                                                                                                                                     |
| `tooltip-text`       | `BODY TEXT`          | The detailed text of the tooltip, explaining the feature or functionality in greater detail, often including HTML elements for formatting or linking to additional resources.                                                         |

---

### **Key Insights**

1. **Field Relationships**:
   - `ID` uniquely identifies each tooltip, ensuring consistency across different parts of the application.
   - `NAME` provides a functional or contextual label for the tooltip, linking it to a specific feature.

2. **Text Content**:
   - `TITLE TEXT` serves as the headline or summary of the tooltip, giving users immediate clarity about its purpose.
   - `BODY TEXT` provides additional information or guidance, often enhanced with HTML for interactivity, such as links to related features or settings.

3. **Applications**:
   - Tooltips enhance user experience by offering contextual help, guiding users through complex features without requiring external documentation.
   - The `BODY TEXT` field supports dynamic updates to include new features or resources.

---

### Example Interpretation of Data:
- **Row 1**:
  - **ID**: 1
  - **NAME**: `BOOKMARK`
  - **TITLE TEXT**: `Bookmark`
  - **BODY TEXT**: `Save this selection of verses as a bookmark, so you can easily access it again.`
  - Represents a tooltip that explains how to use the bookmarking feature within the application.

- **Row 4**:
  - **ID**: 4
  - **NAME**: `FORMULAE`
  - **TITLE TEXT**: `Formulaic Analysis Options`
  - **BODY TEXT**: `Qur&rsquo;an Gateway can highlight any phrase in the currently selected text that are part of a <i>formula</i>...`
  - Guides users on how to analyze formulaic patterns in Quranic text, with links to related features.

---

### Contextual Significance:
1. **User Assistance**:
   - The `tooltip-text` table serves as a dynamic help system embedded directly into the application, reducing the need for external documentation.
2. **Interactivity**:
   - HTML elements in the `BODY TEXT` field allow for enhanced interactivity, such as linking users to specific settings or advanced features.
3. **Ease of Maintenance**:
   - By centralizing tooltip content in a database table, updates and additions to tooltips can be managed efficiently without modifying application code.

---

### First 10 Rows Example (2025-01-14)
|   ID | NAME              | TITLE TEXT                      | BODY TEXT                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----:|:------------------|:--------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    1 | BOOKMARK          | Bookmark                        | Save this selection of verses as a bookmark, so you can easily access it again.                                                                                                                                                                                                                                                                                                                                                                          |
|    2 | COPYREF           | Copy References                 | Copy this selection of verses to the clipboard as a list of references.                                                                                                                                                                                                                                                                                                                                                                                  |
|    3 | ANALYSE           | Analyse Verses                  | You can count (or chart) the different words found, and even the number of each Arabic letter used in this selection of verses.                                                                                                                                                                                                                                                                                                                          |
|    4 | FORMULAE          | Formulaic Analysis Options      | Qur&rsquo;an Gateway can highlight any phrase in the currently selected text that are part of a <i>formula</i> (a portion of text that is repeated multiple times in the Qur&rsquo;an). You can browse a <a href='formulae/list_formulae.php?L=ANY'><font color=blue>list of every formula</font></a> in the Qur&rsquo;an or <a href='charts/chart-formulae-used-per-sura.php'><font color=blue>chart their frequency</font></a> across the entire text. |
|    5 | CHANGES_PERMANENT | Scribal Change Word Underlining | You have turned underlining of words effected by scribal changes permanently on. You can change this in <a href='preferences.php'><font color=blue>Preferences</font></a>.                                                                                                                                                                                                                                                                               |
|    6 | CHANGES_OFF       | Scribal Change Word Underlining | Click to underline any words affected by scribal changes. (Qur&rsquo;an Gateway has a database of thousands of manuscript changes which you can <a href='manuscripts/list_all_changes.php'><font color=blue>browse</font></a>, or <a href='search.php?S=CHANGES>0&UNDERLINE_CHANGES=Y'><font color=blue>search</font></a> for to see them within the text itself).                                                                                       |
|    7 | CHANGES_ON        | Scribal Change Word Underlining | Click to stop underlining any words affected by scribal changes. (Qur&rsquo;an Gateway has a database of thousands of manuscript changes which you can <a href='manuscripts/list_all_changes.php'><font color=blue>browse</font></a>, or <a href='search.php?S=CHANGES>0&UNDERLINE_CHANGES=Y'><font color=blue>search</font></a> for to see them within the text itself).                                                                                |
|    8 | READER MODE       | Switch to Reader Mode           | View your selection of verses as text in three columns (Arabic, transliteration, and translation). Reader Mode is the easiest and most natural way to read the text.                                                                                                                                                                                                                                                                                     |
|    9 | PARSE MODE        | Switch to Parse Mode            | Break down each verse in your selection into its constituent words, with full linguistic data shown beside each word.                                                                                                                                                                                                                                                                                                                                    |
|   10 | EDIT VERSES       | Edit Verses                     | Click to return to the home page and edit the list of verses you have just looked up.                                                                                                                                                                                                                                                                                                                                                                    |

---

## **Table name is `quick-tips`**
The `quick-tips` table provides a collection of short, actionable suggestions for users navigating the system. It offers guidance on common tasks like searching verses, analyzing roots, and using advanced search functions.

### **Analysis of the `quick-tips` Table**

Below is the detailed analysis and description of each field in the `quick-tips` table, with the table name included as a left-hand column.

---

| **Table Name**     | **Field Name**            | **Description**                                                                                                                                                       |
|---------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `quick-tips`        | `ID`                     | A unique identifier for each quick tip, serving as the primary key for indexing and referencing.                                                                      |
| `quick-tips`        | `Quick Tip`              | The main content of the quick tip, providing concise guidance or information about how to use a feature or perform an action within the Qur’an Tools application.     |
| `quick-tips`        | `Example`                | An example related to the quick tip, illustrating the concept or command described in the `Quick Tip` field.                                                          |
| `quick-tips`        | `More Help Link`         | A URL linking to a help page or resource for additional guidance related to the quick tip, often offering detailed explanations or further examples.                  |
| `quick-tips`        | `Next Quick Tip ID`      | The ID of the next quick tip in the sequence, enabling navigation through a series of tips.                                                                           |
| `quick-tips`        | `Previous Quick Tip ID`  | The ID of the previous quick tip in the sequence, allowing users to navigate back to earlier tips.                                                                    |

---

### **Key Insights**

1. **Field Relationships**:
   - `ID` uniquely identifies each tip, ensuring that the tips can be displayed or referenced independently.
   - `Next Quick Tip ID` and `Previous Quick Tip ID` form a linked list, enabling sequential navigation between tips.

2. **Content Utility**:
   - `Quick Tip` provides actionable, user-friendly advice to help users navigate and utilize the Qur’an Tools application.
   - `Example` enhances understanding by offering practical, real-world illustrations of the tips provided.

3. **Applications**:
   - Helps users discover and understand features of the application through quick, actionable tips.
   - Enables dynamic navigation through a series of tips, creating an interactive and engaging user experience.

---

### Example Interpretation of Data:
- **Row 1**:
  - **ID**: 1
  - **Quick Tip**: `Welcome to Qur'an Tools. You can easily look up a verse by simply typing it into the search box above, for example try typing:`
  - **Example**: `2:256`
  - **More Help Link**: `/help/looking-up-a-passage.php`
  - **Next Quick Tip ID**: `2`
  - **Previous Quick Tip ID**: `NULL`
  - Provides a welcome tip on how to look up a verse by typing its reference into the search box.

- **Row 5**:
  - **ID**: 5
  - **Quick Tip**: `Search the Qur'an for an Arabic root by typing ROOT: into the search box above, following by the root you want. For example, try typing:`
  - **Example**: `ROOT:ktb`
  - **More Help Link**: `/help/performing-a-basic-search.php`
  - **Next Quick Tip ID**: `6`
  - **Previous Quick Tip ID**: `20`
  - Explains how to search for an Arabic root, providing the `ROOT:` command and an example.

---

### Contextual Significance:
1. **User Assistance**:
   - This table acts as an embedded tutorial system, providing step-by-step guidance to new users or highlighting advanced features for experienced users.
2. **Ease of Navigation**:
   - The linked list structure (`Next Quick Tip ID`, `Previous Quick Tip ID`) allows users to move seamlessly between related tips.
3. **Scalability**:
   - Centralized management of quick tips ensures that new features or updates can be easily incorporated into the tips system.

---

### First 10 Rows Example (2025-01-14)
|   ID | Quick Tip                                                                                                                                                                                                                                       | Example                                          | More Help Link                      |   Next Quick Tip ID |   Previous Quick Tip ID |
|-----:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------|:------------------------------------|--------------------:|------------------------:|
|    1 | Welcome to Qur`an Tools. You can easily look up a verse by simply typing it into the search box above, for example try typing:                                                                                                                  | 2:256                                            | /help/looking-up-a-passage.php      |                   2 |                     nan |
|    2 | You can look up an entire sura simply by typing any number between 1 and 114 into the search box above. For example, try typing:                                                                                                                | 110                                              | /help/looking-up-a-passage.php      |                   3 |                       1 |
|    3 | It's easy to look up a range of verses; try typing this into the search box above:                                                                                                                                                              | 2:1-20                                           | /help/looking-up-a-passage.php      |                   4 |                       2 |
|    4 | You can look up a series of ranges of verses by separating them with a semi-colon, like this:                                                                                                                                                   | 17:61-64;18:50;20:116-117;38:71-83               | /help/looking-up-a-passage          |                  20 |                       3 |
|    5 | Search the Qur`an for an Arabic root by typing ROOT: into the search box above, following by the root you want. For example, try typing:                                                                                                        | ROOT:ktb                                         | /help/performing-a-basic-search.php |                   6 |                      20 |
|    6 | See all the Arabic roots in the Qur`an, along with their definitions, using the Dictionary Tool. You'll find it under the Browse menu above.                                                                                                    | <a href='dictionary.php'>Open the Dictionary</a> | /help/the-dictionary-tool.php       |                   7 |                       5 |
|    7 | You can also search using Arabic letters rather than transliterated English. The keyboard icon, just below the search box above, will give you an Arabic keyboard. Click on letters to enter them. And then you can try a search like this one: | ROOT:???                                         | /help/performing-a-basic-search.php |                   8 |                       6 |
|    8 | Search the English translations of the Qur`an by using the ENGLISH command. For example, try typing the example below into the search box above:                                                                                                | ENGLISH:throne                                   | /help/performing-a-basic-search.php |                   9 |                       7 |
|    9 | You can search the English translations for a phrase, rather than a word, by surrounding it with quote marks. For example, try this:                                                                                                            | ENGLISH:"the world"                              | /help/performing-a-basic-search.php |                  10 |                       8 |
|   10 | Search for more than one root by using the AND command. For example, try typing this into the search box above:                                                                                                                                 | ROOT:ktb AND ROOT:ryb                            | /help/performing-a-basic-search.php |                  11 |                       9 |

---

## **Table name is `failed-searches`**
The `failed-searches` table logs unsuccessful user search queries, capturing details like the timestamp and user ID. This data helps in improving the search functionality by identifying gaps or user challenges in retrieving relevant results.

### **Analysis of the `failed-searches` Table**

Below is the detailed analysis and description of each field in the `failed-searches` table, with the table name included as a left-hand column.

---

| **Table Name**       | **Field Name** | **Description**                                                                                                                                          |
|-----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `failed-searches`     | `ID`           | A unique identifier for each failed search entry, serving as the primary key for indexing and referencing.                                                |
| `failed-searches`     | `USER ID`      | The unique identifier of the user who performed the failed search, allowing for tracking and analysis of user-specific issues or patterns.                 |
| `failed-searches`     | `TIMESTAMP`    | The date and time when the failed search occurred, providing a temporal context for analyzing search trends and identifying recurring issues.              |
| `failed-searches`     | `SEARCH`       | The search query entered by the user that resulted in no results, capturing the exact input for debugging or improving the search functionality.           |

---

### **Key Insights**

1. **Field Relationships**:
   - `ID` uniquely identifies each failed search record, ensuring traceability and data integrity.
   - `USER ID` links failed searches to individual users, enabling personalized troubleshooting or improvements.

2. **Search Debugging**:
   - The `SEARCH` field stores the exact query entered by the user, making it easier to identify common issues, such as typos or unsupported commands.
   - `TIMESTAMP` provides temporal context, helping pinpoint periods of increased failed searches for targeted improvements.

3. **Applications**:
   - Helps optimize the search functionality by identifying common patterns in failed searches.
   - Facilitates debugging and troubleshooting by preserving user queries and their context.

---

### Example Interpretation of Data:
- **Row 1**:
  - **ID**: 1
  - **USER ID**: 211
  - **TIMESTAMP**: `2021-12-07 20:31:22`
  - **SEARCH**: `test search`
  - Indicates that user `211` performed a search query (`test search`) that failed at the specified timestamp.

- **Row 7**:
  - **ID**: 7
  - **USER ID**: 1027
  - **TIMESTAMP**: `2021-12-11 03:26:08`
  - **SEARCH**: `test search`
  - Indicates another failed query by user `1027`, occurring on December 11, 2021.

---

### Contextual Significance:
1. **Search Optimization**:
   - Patterns in the `SEARCH` field can reveal frequent user mistakes or unsupported queries, guiding improvements in search algorithms or documentation.
2. **User Experience Analysis**:
   - Tracking failed searches by `USER ID` and `TIMESTAMP` helps identify user groups or time periods where assistance or additional features are needed.
3. **Error Mitigation**:
   - Analysis of failed searches can inform autocomplete suggestions, error corrections, or enhanced help prompts in the search interface.

---

### First 10 Rows Example (2025-01-14)
|   ID |   USER ID | TIMESTAMP           | SEARCH      |
|-----:|----------:|:--------------------|:------------|
|    1 |       211 | 2021-12-07 20:31:22 | test search |
|    2 |       213 | 2021-12-07 20:31:22 | test search |
|    3 |       413 | 2021-12-07 20:36:36 | test search |
|    4 |       415 | 2021-12-07 20:36:36 | test search |
|    5 |       665 | 2021-12-07 20:41:20 | test search |
|    6 |       667 | 2021-12-07 20:41:20 | test search |
|    7 |      1027 | 2021-12-11 03:26:08 | test search |
|    8 |      1029 | 2021-12-11 03:26:09 | test search |
|    9 |      1133 | 2021-12-11 07:55:00 | test search |
|   10 |      1135 | 2021-12-11 07:55:01 | test search |

---

## **Table name is `usage`**
The `usage` table tracks user activity, including the pages they load, timestamps, and associated metadata. It provides insights into user behavior and system utilization, aiding in feature optimization and user experience improvements.

### **Analysis of the `usage` Table**

Below is the detailed analysis and description of each field in the `usage` table, with the table name included as a left-hand column.

---

| **Table Name** | **Field Name**    | **Description**                                                                                                                                                     |
|-----------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `usage`         | `ID`             | A unique identifier for each usage entry, serving as the primary key for indexing and referencing.                                                                 |
| `usage`         | `PAGE LOADED`    | The title or URL of the page that was accessed by the user, representing the action taken or the page viewed within the application.                                |
| `usage`         | `ACTUAL PAGE`    | (Currently empty in the provided data) Intended to store the exact URL or a more detailed path for the page accessed, allowing for precise tracking.                |
| `usage`         | `CATEGORY`       | (Currently empty in the provided data) Intended to categorize the type of page or action (e.g., `Browse`, `Search`, `Help`), supporting more detailed analytics.    |
| `usage`         | `USER ID`        | The unique identifier of the user who accessed the page, enabling tracking and analysis of user behavior.                                                           |
| `usage`         | `DATE AND TIME`  | The timestamp when the page was accessed, providing temporal context for analyzing user activity and engagement trends.                                              |

---

### **Key Insights**

1. **Field Relationships**:
   - `ID` uniquely identifies each usage record, ensuring traceability.
   - `USER ID` links the action to a specific user, allowing for personalized usage analytics.

2. **Usage Tracking**:
   - `PAGE LOADED` captures the action or page accessed, providing insight into user interactions with the application.
   - `DATE AND TIME` allows for temporal analysis, such as peak usage times or trends over specific periods.

3. **Potential Enhancements**:
   - Populating `ACTUAL PAGE` and `CATEGORY` would enable more granular tracking and categorization of user activity, improving analytics.

---

### Example Interpretation of Data:
- **Row 1**:
  - **ID**: 2265
  - **PAGE LOADED**: `/home.php`
  - **USER ID**: 1525
  - **DATE AND TIME**: `2025-01-01 18:41:33`
  - Indicates that user `1525` accessed the home page (`/home.php`) on January 1, 2025, at 6:41 PM.

- **Row 4**:
  - **ID**: 2268
  - **PAGE LOADED**: `/verse_browser.php?V=1`
  - **USER ID**: 1525
  - **DATE AND TIME**: `2025-01-04 11:49:47`
  - Shows the same user accessed a verse browser for verse 1 on January 4, 2025, at 11:49 AM.

---

### Contextual Significance:
1. **User Behavior Analysis**:
   - The `PAGE LOADED` and `DATE AND TIME` fields can help identify popular pages or features and analyze user engagement trends over time.
2. **Feature Optimization**:
   - Tracking user interactions allows for identifying underused or problematic features that may need enhancement.
3. **Personalized Analytics**:
   - By linking actions to `USER ID`, the table supports creating personalized reports or recommendations for users.

---

### First 10 Rows Example (2025-01-14)
|   ID | PAGE LOADED                      |   ACTUAL PAGE |   CATEGORY |   USER ID | DATE AND TIME       |
|-----:|:---------------------------------|--------------:|-----------:|----------:|:--------------------|
| 2265 | /home.php                        |           nan |        nan |      1525 | 2025-01-01 18:41:33 |
| 2266 | /help/welcome-to-quran-tools.php |           nan |        nan |      1525 | 2025-01-01 18:41:44 |
| 2267 | /browse_sura.php                 |           nan |        nan |      1525 | 2025-01-04 11:49:44 |
| 2268 | /verse_browser.php?V=1           |           nan |        nan |      1525 | 2025-01-04 11:49:47 |
| 2269 | /verse_browser.php?V=1           |           nan |        nan |      1525 | 2025-01-04 11:52:45 |

---

## **Table name is `render-formulaic-density-summaries`**
This table summarizes data on formulaic density within the Qur'an, categorizing it by root structures and lemmas. It supports linguistic studies on the prevalence and distribution of formulaic language across chapters and contexts.

### **Analysis of the `render-formulaic-density-summaries` Table**

Below is the detailed analysis and description of each field in the `render-formulaic-density-summaries` table, with the table name included as a left-hand column.

---

| **Table Name**                         | **Field Name**      | **Description**                                                                                                                                               |
|-----------------------------------------|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `render-formulaic-density-summaries`    | `ID`                | A unique identifier for each summary entry, such as `AVERAGE-ALL`, `TOTAL-ALL`, `TOTAL-MECCAN`, or `TOTAL-MEDINAN`, representing the type of summary provided. |
| `render-formulaic-density-summaries`    | `ROOT_3`            | The density of 3-root formulas in the specified context (e.g., average, total, Meccan, Medinan), calculated as a percentage.                                   |
| `render-formulaic-density-summaries`    | `ROOT_4`            | The density of 4-root formulas in the specified context, calculated as a percentage.                                                                           |
| `render-formulaic-density-summaries`    | `ROOT_5`            | The density of 5-root formulas in the specified context, calculated as a percentage.                                                                           |
| `render-formulaic-density-summaries`    | `ROOTPLUS_3`        | The density of 3-root-plus formulas (including roots and particles) in the specified context, calculated as a percentage.                                      |
| `render-formulaic-density-summaries`    | `ROOTPLUS_4`        | The density of 4-root-plus formulas in the specified context, calculated as a percentage.                                                                      |
| `render-formulaic-density-summaries`    | `ROOTPLUS_5`        | The density of 5-root-plus formulas in the specified context, calculated as a percentage.                                                                      |
| `render-formulaic-density-summaries`    | `LEMMA_3`           | The density of 3-lemma formulas in the specified context, calculated as a percentage.                                                                          |
| `render-formulaic-density-summaries`    | `LEMMA_4`           | The density of 4-lemma formulas in the specified context, calculated as a percentage.                                                                          |
| `render-formulaic-density-summaries`    | `LEMMA_5`           | The density of 5-lemma formulas in the specified context, calculated as a percentage.                                                                          |

---

### **Key Insights**

1. **Field Relationships**:
   - `ID` specifies the context of the summary, such as whether the calculations are for all verses (`TOTAL-ALL`), average densities (`AVERAGE-ALL`), or subsets like Meccan or Medinan verses.
   - The fields grouped by `ROOT`, `ROOTPLUS`, and `LEMMA` represent density calculations for 3-word, 4-word, and 5-word formulas.

2. **Contextual Meaning**:
   - `ROOT` fields focus solely on root-based formulas.
   - `ROOTPLUS` fields include formulas combining roots and particles, broadening the analysis scope.
   - `LEMMA` fields analyze formulas based on lemmatized words, capturing semantic groupings.

3. **Applications**:
   - Helps analyze the density of formulaic structures in Quranic text, providing insights into linguistic patterns.
   - Facilitates comparisons between Meccan and Medinan chapters or between different formulaic densities.

---

### Example Interpretation of Data:
- **Row 1**: `AVERAGE-ALL`
  - **ROOT_3**: `39.51`
  - **ROOTPLUS_3**: `62.34`
  - **LEMMA_3**: `58.11`
  - Indicates that on average, 3-root formulas make up 39.51% of the text, while 3-root-plus formulas account for 62.34%, and 3-lemma formulas cover 58.11%.

- **Row 4**: `TOTAL-MEDINAN`
  - **ROOT_3**: `46.47`
  - **ROOTPLUS_3**: `64.74`
  - **LEMMA_3**: `60.70`
  - Shows that Medinan chapters have a higher density of 3-root formulas (46.47%) and 3-root-plus formulas (64.74%) compared to Meccan chapters.

---

### Contextual Significance:
1. **Linguistic Insights**:
   - Highlights variations in formulaic density between Meccan and Medinan chapters, reflecting differences in style, audience, and context.
2. **Comparative Analysis**:
   - Facilitates comparisons across formulaic types (root-based, lemma-based, and root-plus) and word counts (3, 4, 5), offering a comprehensive linguistic perspective.
3. **Digital Applications**:
   - This table can power visualization tools, such as density charts or heatmaps, to explore formulaic patterns in Quranic text.

---

### First 10 Rows Example (2025-01-14)
| ID            |   ROOT_3 |   ROOT_4 |   ROOT_5 |   ROOTPLUS_3 |   ROOTPLUS_4 |   ROOTPLUS_5 |   LEMMA_3 |   LEMMA_4 |   LEMMA_5 |
|:--------------|---------:|---------:|---------:|-------------:|-------------:|-------------:|----------:|----------:|----------:|
| AVERAGE-ALL   |    39.51 |    24.96 |    14.17 |        62.34 |        49.11 |        25.14 |     58.11 |     38.05 |     25.71 |
| TOTAL-ALL     |    39.51 |    24.96 |    14.17 |        62.34 |        49.11 |        25.14 |     58.11 |     38.05 |     25.71 |
| TOTAL-MECCAN  |    35.38 |    23.5  |    13.56 |        60.93 |        47.59 |        23.84 |     56.59 |     36.67 |     25.12 |
| TOTAL-MEDINAN |    46.47 |    27.43 |    15.22 |        64.74 |        51.71 |        27.38 |     60.7  |     40.39 |     26.73 |

---

## **Table name is `translation-list`**
The `translation-list` table catalogs translations of the Qur'an, detailing the translator, publication date, and descriptive notes. It allows users to explore and compare different interpretive perspectives on the text.

### **Analysis of the `translation-list` Table**

Below is the detailed analysis and description of each field in the `translation-list` table, with the table name included as a left-hand column.

---

| **Table Name**        | **Field Name**           | **Description**                                                                                                                                                                |
|------------------------|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `translation-list`     | `TRANSLATION ID`         | A unique identifier for each translation, serving as the primary key for indexing and referencing.                                                                            |
| `translation-list`     | `TRANSLATION NAME`       | The name of the translator or translation, providing a user-friendly label for identifying the translation (e.g., `Yusuf Ali`, `Pickthall`).                                  |
| `translation-list`     | `TRANSLATION ALL CAPS NAME` | The all-uppercase version of the translator or translation name, often used for display consistency or as a reference for case-insensitive operations.                       |
| `translation-list`     | `DESCRIPTION`            | A detailed description of the translation, including the translator’s full name, the year of publication, and notable details about the translation or its significance.      |

---

### **Key Insights**

1. **Field Relationships**:
   - `TRANSLATION ID` uniquely identifies each translation entry, ensuring clear referencing in other datasets or tools.
   - `TRANSLATION NAME` and `TRANSLATION ALL CAPS NAME` provide two formats for the translator’s name, supporting various use cases such as display or case-insensitive searches.

2. **Content Utility**:
   - The `DESCRIPTION` field provides context about each translation, including the translator’s background, publication details, and any distinguishing features.

3. **Applications**:
   - Facilitates user selection of translations in Quranic tools.
   - Supports translation comparisons by providing metadata about each version.

---

### Example Interpretation of Data:
- **Row 1**:
  - **TRANSLATION ID**: 4
  - **TRANSLATION NAME**: `Arberry`
  - **TRANSLATION ALL CAPS NAME**: `ARBERRY`
  - **DESCRIPTION**: `Arthur John Arberry’s 1955 English translation of the Qur’an (<i>The Koran Interpreted</i>)`
  - Represents Arthur Arberry’s translation, notable for its attempt to preserve the Quran’s literary and poetic style.

- **Row 4**:
  - **TRANSLATION ID**: 1
  - **TRANSLATION NAME**: `Yusuf Ali`
  - **TRANSLATION ALL CAPS NAME**: `YUSUFALI`
  - **DESCRIPTION**: `Abdullah Yusuf Ali’s English translation of the Qur’an (1934-1940, published as <i>The Holy Qur’an: Text, Translation and Commentary</i>)`
  - Highlights Yusuf Ali’s widely known translation, notable for its commentary and comprehensive footnotes.

---

### Contextual Significance:
1. **Translation Metadata**:
   - The table provides essential details for identifying and contextualizing Quranic translations, useful for both academic and general audiences.
2. **User Personalization**:
   - By offering multiple translation options, users can choose a version that aligns with their preferences or study needs.
3. **Comparison and Analysis**:
   - The metadata allows for structured comparison between translations, such as their publication date, translator background, and stylistic differences.



# Data Dictionary
|   TRANSLATION ID | TRANSLATION NAME   | TRANSLATION ALL CAPS NAME   | DESCRIPTION                                                                                                                               |
|-----------------:|:-------------------|:----------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
|                4 | Arberry            | ARBERRY                     | Arthur John Arberry?s 1955 English translation of the Qur?an (<i>The Koran Interpreted</i>)                                               |
|                2 | Pickthall          | PICKTHALL                   | Marmaduke William Pickthall?s 1930 English translation of the Qur?an (<i>The Meaning of the Glorious Koran</i>)                           |
|                3 | Shakir             | SHAKIR                      | M. H. Shakir?s English translation of the Qur?an                                                                                          |
|                1 | Yusuf Ali          | YUSUFALI                    | Abdullah Yusuf Ali?s English translation of the Qur?an (1934-1940, published as <i>The Holy Qur?an: Text, Translation and Commentary</i>) |
**End of Table**

---

## **Table name is `usage-verses-searches`**
This table logs searches performed by users for specific verses or queries, capturing metadata like referring pages and timestamps. It provides an audit trail of search behavior, useful for understanding user needs and refining search algorithms.

### **Analysis of the `usage-verses-searches` Table**

Below is the detailed analysis and description of each field in the `usage-verses-searches` table, with the table name included as a left-hand column.

---

| **Table Name**               | **Field Name**        | **Description**                                                                                                                                         |
|-------------------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `usage-verses-searches`       | `ID`                 | A unique identifier for each entry in the table, serving as the primary key for indexing and referencing.                                               |
| `usage-verses-searches`       | `VERSES OR SEARCH`   | Specifies whether the action involved a verse lookup (`V`) or a search query, indicating the type of user interaction.                                   |
| `usage-verses-searches`       | `LOOKED UP`          | The specific verse or search term that was looked up by the user, providing the content of the query or action.                                          |
| `usage-verses-searches`       | `REFERRING PAGE`     | The page from which the action was initiated, offering context for the user's navigation path within the application.                                     |
| `usage-verses-searches`       | `USER ID`            | The unique identifier of the user who performed the action, enabling personalized or aggregate usage analysis.                                           |
| `usage-verses-searches`       | `Institution ID`     | Identifies the institution associated with the user, if applicable. A `NULL` value indicates no institutional affiliation is recorded for the action.    |
| `usage-verses-searches`       | `DATE AND TIME`      | The timestamp when the action occurred, providing temporal context for analyzing trends and user activity patterns.                                       |

---

### **Key Insights**

1. **Field Relationships**:
   - `ID` uniquely identifies each user action, ensuring data traceability.
   - `USER ID` and `Institution ID` link the action to individual users or institutions, allowing for user-specific or group-specific analytics.

2. **Action Context**:
   - `VERSES OR SEARCH` and `LOOKED UP` specify the type of action and the exact content of the lookup, helping analyze user intent and preferences.
   - `REFERRING PAGE` indicates the navigation flow, providing insight into how users interact with the application.

3. **Applications**:
   - Tracks user interactions with verse lookups or searches, enabling insights into popular verses or search trends.
   - Supports optimization of navigation paths and search functionality based on usage patterns.

---

### Example Interpretation of Data:
- **Row 1**:
  - **ID**: 37
  - **VERSES OR SEARCH**: `V`
  - **LOOKED UP**: `1`
  - **REFERRING PAGE**: `/browse_sura.php`
  - **USER ID**: `1525`
  - **Institution ID**: `NULL`
  - **DATE AND TIME**: `2025-01-04 11:49:47`
  - Indicates that user `1525` looked up verse `1` from the page `/browse_sura.php` on January 4, 2025, at 11:49 AM.

- **Row 2**:
  - **ID**: 38
  - **VERSES OR SEARCH**: `V`
  - **LOOKED UP**: `1`
  - **REFERRING PAGE**: `/browse_sura.php`
  - **USER ID**: `1525`
  - **Institution ID**: `NULL`
  - **DATE AND TIME**: `2025-01-04 11:52:45`
  - Shows another verse lookup action for verse `1` by the same user shortly after the previous action.

---

### Contextual Significance:
1. **Usage Tracking**:
   - Helps identify frequently looked-up verses or common search queries, guiding content prioritization or application enhancements.
2. **Navigation Flow Analysis**:
   - By analyzing `REFERRING PAGE`, developers can optimize navigation paths to improve user experience.
3. **Temporal Insights**:
   - The `DATE AND TIME` field allows for identifying peak usage times or monitoring patterns of user engagement over time.

---

### First 10 Rows Example (2025-01-14)
|   ID | VERSES OR SEARCH   |   LOOKED UP | REFERRING PAGE   |   USER ID |   Institution ID | DATE AND TIME       |
|-----:|:-------------------|------------:|:-----------------|----------:|-----------------:|:--------------------|
|   37 | V                  |           1 | /browse_sura.php |      1525 |              nan | 2025-01-04 11:49:47 |
|   38 | V                  |           1 | /browse_sura.php |      1525 |              nan | 2025-01-04 11:52:45 |

---

## **Table name is `login-logs`**
The `login-logs` table records user login activity, including timestamps, IP addresses, and user information. This data is vital for security audits and tracking user access patterns.

### **Analysis of the `login-logs` Table**

Below is the detailed analysis and description of each field in the `login-logs` table, with the table name included as a left-hand column.

---

| **Table Name**   | **Field Name**     | **Description**                                                                                                                                   |
|-------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `login-logs`      | `Record ID`       | A unique identifier for each login record, serving as the primary key for indexing and referencing.                                               |
| `login-logs`      | `User ID`         | The unique identifier of the user who logged in, enabling tracking and analysis of user-specific login activity.                                   |
| `login-logs`      | `Institution ID`  | Identifies the institution associated with the user, if applicable. A `NULL` value indicates no institutional affiliation is recorded for the user.|
| `login-logs`      | `Email Address`   | The email address of the user who logged in, providing an additional reference for identifying the user.                                           |
| `login-logs`      | `Login Date`      | The date when the login occurred, allowing for temporal analysis of login activity.                                                               |
| `login-logs`      | `Login Time`      | The time when the login occurred, complementing `Login Date` for precise tracking of login events.                                                 |
| `login-logs`      | `Login IP`        | The IP address from which the user logged in, providing contextual information for monitoring and security purposes.                               |
| `login-logs`      | `DATE AND TIME`   | A combined timestamp of the login event, consolidating `Login Date` and `Login Time` for convenience in chronological analysis.                    |

---

### **Key Insights**

1. **Field Relationships**:
   - `Record ID` uniquely identifies each login event, ensuring traceability and data integrity.
   - `User ID` and `Email Address` link the login to a specific user, allowing for user-specific analysis.

2. **Login Context**:
   - `Login IP` provides insights into the location or network from which the login occurred, which is useful for security monitoring.
   - `DATE AND TIME` simplifies chronological sorting and analysis of login events.

3. **Applications**:
   - Tracks user login activity to monitor engagement and detect potential security issues.
   - Identifies peak login times or trends for optimizing application availability and performance.

---

### Example Interpretation of Data:
- **Row 1**:
  - **Record ID**: 972
  - **User ID**: 1525
  - **Institution ID**: `NULL`
  - **Email Address**: `<EMAIL TEXT>`
  - **Login Date**: `2025-01-01`
  - **Login Time**: `07:41:33`
  - **Login IP**: `127.0.0.1`
  - **DATE AND TIME**: `2025-01-01 18:41:33`
  - Indicates that user `1525` logged in on January 1, 2025, at 7:41 AM from IP address `127.0.0.1`.

---

### Contextual Significance:
1. **User Engagement Analysis**:
   - Tracks user activity by analyzing login frequency and patterns.
2. **Security Monitoring**:
   - IP tracking allows detection of suspicious activity, such as logins from unusual locations or multiple failed attempts.
3. **Temporal Trends**:
   - Combining `Login Date` and `Login Time` enables identification of peak login times for resource allocation or system optimization.

---

### First 10 Rows Example (2025-01-14)
|   Record ID |   User ID |   Institution ID | Email Address      | Login Date   | Login Time   | Login IP   | DATE AND TIME       |
|------------:|----------:|-----------------:|:-------------------|:-------------|:-------------|:-----------|:--------------------|
|         972 |      1525 |              nan | <EMAIL TEXT> | 2025-01-01   | 07:41:33     | 127.0.0.1  | 2025-01-01 18:41:33 |

---

## **Table name is `users`**
The `users` table stores user account details, including login credentials, preferences, and activity data. It is a core component of user management, supporting authentication and personalization features.

### **Analysis of the `users` Table**

Below is the detailed analysis and description of each field in the `users` table, with the table name included as a left-hand column.

---

| **Table Name**  | **Field Name**                                | **Description**                                                                                                                                                     |
|------------------|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `users`          | `User ID`                                    | A unique identifier for each user, serving as the primary key for indexing and referencing user records.                                                            |
| `users`          | `User Type`                                  | Specifies the type of user (e.g., `CONSUMER`, `ADMIN`), defining their access level and role within the application.                                                 |
| `users`          | `Email Address`                              | The email address associated with the user, used for communication and as a unique identifier for login and account recovery.                                        |
| `users`          | `Password Hash`                              | The hashed version of the user’s password for secure storage and authentication.                                                                                     |
| `users`          | `First Name`                                 | The user’s first name, used for personalization and communication.                                                                                                   |
| `users`          | `Last Name`                                  | The user’s last name, used for personalization and communication.                                                                                                    |
| `users`          | `Administrator`                              | Indicates whether the user has administrative privileges (e.g., `SUPERUSER`, `NULL` if not an admin).                                                                |
| `users`          | `Reset Code`                                 | A code used for resetting the user’s password, generated during a password recovery request.                                                                         |
| `users`          | `Reset Timecode`                             | The timestamp when the password reset code was generated, used to verify the reset request’s validity.                                                               |
| `users`          | `Last Login Date`                            | The date of the user’s most recent login, providing insights into user activity.                                                                                     |
| `users`          | `Last Login Time`                            | The time of the user’s most recent login, complementing `Last Login Date` for precise activity tracking.                                                             |
| `users`          | `Last Login Timestamp`                       | A combined timestamp of the user’s last login event, consolidating date and time for easier chronological analysis.                                                  |
| `users`          | `Is Blocked`                                 | Indicates whether the user’s account is blocked (`NULL` if not blocked).                                                                                             |
| `users`          | `Login Count`                                | The total number of successful logins performed by the user, useful for engagement metrics.                                                                          |
| `users`          | `Fails Count`                                | The number of consecutive failed login attempts by the user, used for security measures such as account locking.                                                     |
| `users`          | `Fail Time`                                  | The timestamp of the user’s most recent failed login attempt.                                                                                                        |
| `users`          | `Creation Date`                              | The date when the user’s account was created, useful for lifecycle tracking and retention analysis.                                                                  |
| `users`          | `Preferred Highlight Colour`                 | The user’s preferred color for highlighting verses or text in the application, stored as a hexadecimal color code (e.g., `FFFF00`).                                  |
| `users`          | `Preferred Highlight Colour Lightness Value` | The lightness value of the preferred highlight color, used for rendering light or dark variations.                                                                   |
| `users`          | `Preferred Cursor Colour`                    | The user’s preferred cursor color, stored as a hexadecimal color code (e.g., `DDDDDD`).                                                                              |
| `users`          | `Preferred Translation`                      | The ID of the user’s preferred Quranic translation, linking to a translation table.                                                                                  |
| `users`          | `Preferred Verse Count`                      | The number of verses the user prefers to view per page, used for pagination settings.                                                                                 |
| `users`          | `Preferred Default Mode`                     | The user’s default mode of operation, such as `0` for basic mode or `1` for advanced features.                                                                        |
| `users`          | `Preferred Keyboard Direction`               | The user’s preferred keyboard direction, such as `LTR` (left-to-right) or `RTL` (right-to-left).                                                                     |
| `users`          | `Preference Italics Transliteration`         | Indicates whether the user prefers transliteration in italics (`1` for enabled, `0` for disabled).                                                                    |
| `users`          | `Preference Show Quick Tips`                 | Indicates whether the user prefers to see quick tips (`1` for enabled, `0` for disabled).                                                                             |
| `users`          | `Preference Floating Page Navigator`         | Indicates whether the user prefers a floating page navigator (`1` for enabled, `0` for disabled).                                                                    |
| `users`          | `Current Quick Tip ID`                       | The ID of the last quick tip viewed by the user, linking to a quick tips table for context.                                                                           |
| `users`          | `AJAX Token`                                 | A token used for secure AJAX requests, preventing cross-site scripting (XSS) attacks.                                                                                |
| `users`          | `Preference Formulaic Glosses`               | Indicates whether the user prefers to see formulaic glosses (`1` for enabled, `0` for disabled).                                                                      |
| `users`          | `Preference Hide Transliteration`            | Indicates whether the user prefers to hide transliteration (`1` for enabled, `0` for disabled).                                                                       |
| `users`          | `LOCKED WITH MESSAGE`                        | Indicates if the user’s account is locked and provides a message or reason for the lock (`NULL` if not locked).                                                       |
| `users`          | `User Name`                                  | The user’s display name, used for personalized interactions within the application.                                                                                   |

---

### **Key Insights**

1. **Field Relationships**:
   - `User ID` links the user’s account to other data, such as login logs, preferences, and usage analytics.
   - `Preferred Translation` connects to the `translation-list` table, personalizing the user’s experience.

2. **User Preferences**:
   - Preferences such as highlight colors, verse count, and transliteration display allow for tailored user experiences.

3. **Security Features**:
   - Fields like `Password Hash`, `Reset Code`, `Reset Timecode`, and `AJAX Token` ensure secure user authentication and session management.

4. **Applications**:
   - Facilitates user account management, engagement tracking, and security monitoring.
   - Personalizes user interactions through configurable preferences.

---

### Example Interpretation of Data:
- **Row 1**:
  - **User ID**: 1525
  - **User Type**: `CONSUMER`
  - **Email Address**: `warwick@foster.net`
  - **Last Login Timestamp**: `2025-01-01 07:41:33`
  - **Preferred Highlight Colour**: `FFFF00`
  - Represents a consumer user with custom preferences for highlights and display. The user has logged in once, with no failed attempts.

---

### Contextual Significance:
1. **Personalized Experience**:
   - User preferences enhance engagement by allowing customizable views and features.
2. **Security and Monitoring**:
   - Tracks login attempts and account status (`Is Blocked`, `Fails Count`) to ensure account integrity.
3. **Lifecycle Analysis**:
   - Tracks user creation and activity to monitor retention and behavior patterns.

---

## **Table name is `transliteration-exceptions`**
The `transliteration-exceptions` table defines exceptions in standard transliteration rules, capturing unique cases where a word is rendered differently for linguistic or contextual reasons. It ensures consistency and accuracy in transliteration output.

### **Analysis of the `transliteration-exceptions` Table**

Below is the detailed analysis and description of each field in the `transliteration-exceptions` table, with the table name included as a left-hand column.

---

| **Table Name**               | **Field Name**  | **Description**                                                                                                                                       |
|-------------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transliteration-exceptions`  | `ID`            | A unique identifier for each transliteration exception, serving as the primary key for indexing and referencing.                                       |
| `transliteration-exceptions`  | `RENDERED`      | The default transliteration of a word or phrase as it appears in the system.                                                                           |
| `transliteration-exceptions`  | `SUBSTITUTE`    | The custom or preferred transliteration to replace the default rendering, ensuring alignment with specific linguistic, cultural, or stylistic preferences. |

---

### **Key Insights**

1. **Field Relationships**:
   - `ID` uniquely identifies each transliteration exception, enabling clear referencing and consistency.
   - `RENDERED` and `SUBSTITUTE` define a mapping between the default transliteration and the custom substitute.

2. **Purpose and Applications**:
   - Corrects or standardizes transliteration discrepancies in Quranic text or related resources.
   - Accommodates user preferences or scholarly conventions for specific terms, such as replacing `al-lah` with `Allah`.

3. **Scalability**:
   - The table allows for the addition of more exceptions as new transliteration cases arise, maintaining flexibility for evolving user needs or scholarly updates.

---

### Example Interpretation of Data:
- **Row 1**:
  - **ID**: 1
  - **RENDERED**: `al-lah`
  - **SUBSTITUTE**: `Allah`
  - Indicates that the transliteration `al-lah` should be replaced with the preferred form `Allah` to align with common usage or theological conventions.

---

### Contextual Significance:
1. **Consistency**:
   - Ensures uniform transliteration across the application, particularly for terms with specific cultural or religious significance.
2. **User Experience**:
   - Improves readability and relevance by substituting less familiar or unconventional transliterations with widely accepted alternatives.
3. **Linguistic Accuracy**:
   - Allows the application to respect established transliteration standards while remaining adaptable to user or scholarly preferences.

---

### First 10 Rows Example (2025-01-14)
|   ID | RENDERED   | SUBSTITUTE   |
|-----:|:-----------|:-------------|
|    1 | al-lah     | Allah        |
**End of table**

---

# Empty Tables that need more information

## **Table name is `tags`**
The `tags` table enables users to categorize and label verses or content, storing tag names, colors, and related metadata. This functionality facilitates personalized organization and retrieval of content.

### Column Descriptions 

| **Table Name**  | **Column Name**      | **Description**                                                                                                                                              |
|------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tags`          | `ID`                 | A unique identifier for each tag, serving as the primary key for the table.                                                                                 |
| `tags`          | `Tag Name`           | The name or label of the tag, providing a descriptive identifier for organizing or categorizing verses.                                                     |
| `tags`          | `User ID`            | A unique identifier linking the tag to the user who created it.                                                                                             |
| `tags`          | `Tag Colour`         | The color associated with the tag, used for visual distinction in interfaces.                                                                               |
| `tags`          | `Tag Lightness Value`| A numerical value indicating the lightness or brightness of the tag’s color, allowing for customizable or accessible color schemes.                          |

---

## **Table name is `messages`**
This table records system-generated messages sent to users, including their content, expiration dates, and status (e.g., retired). It serves as a communication channel between the system and its users.

### Column Descriptions 

| **Table Name**  | **Column Name**      | **Description**                                                                                                                                              |
|------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `messages`      | `ID`                 | A unique identifier for each message, serving as the primary key for the table.                                                                             |
| `messages`      | `MESSAGE`            | The textual content of the message, containing information, notifications, or updates for the user.                                                         |
| `messages`      | `RETIRED`            | A status indicator showing whether the message is no longer active or relevant.                                                                             |
| `messages`      | `DATE AND TIME`      | The date and time when the message was created or sent.                                                                                                     |
| `messages`      | `EXPIRY DATE`        | The date when the message is set to expire or be automatically retired.                                                                                      |

---

## **Table name is `tagged-verses`**
The `tagged-verses` table tracks associations between user-defined tags and specific Qur'anic verses. It supports custom annotations and thematic exploration of the text.

### Column Descriptions 

| **Table Name**  | **Column Name**      | **Description**                                                                                                                                              |
|------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tagged-verses` | `ID`                 | A unique identifier for each tagged verse entry, serving as the primary key.                                                                                |
| `tagged-verses` | `SURA-VERSE`         | The specific sura and verse being tagged, represented in a structured format.                                                                               |
| `tagged-verses` | `User ID`            | A unique identifier linking the tagged verse to a specific user.                                                                                            |
| `tagged-verses` | `TAG ID`             | A reference to the corresponding tag applied to the verse, linking to the `tags` table.                                                                     |

---

## **Table name is `bookmarks`**
This table allows users to save and manage bookmarks for specific verses or sections of the Qur'an, including timestamped metadata. It is a useful feature for revisiting and studying key passages.

### Column Descriptions 

| **Table Name**  | **Column Name**      | **Description**                                                                                                                                              |
|------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bookmarks`     | `Name`               | The name or title of the bookmark, providing a label for easy identification.                                                                                |
| `bookmarks`     | `Timestamp`          | The date and time when the bookmark was created, allowing for chronological tracking.                                                                        |
| `bookmarks`     | `User ID`            | A unique identifier linking the bookmark to a specific user.                                                                                                |
| `bookmarks`     | `Contents`           | The actual content or data associated with the bookmark, such as text or a verse selection.                                                                 |
| `bookmarks`     | `Search Dump`        | A record of the search or query parameters that led to the creation of the bookmark, potentially useful for audit or recreation of the search.              |

---

## **Table name is `history`**
The `history` table records user activity history, such as recently viewed verses or pages. It provides a convenient way for users to revisit previously accessed content.

### Column Descriptions 

| **Table Name**  | **Column Name**      | **Description**                                                                                                                                              |
|------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `history`       | `History Item`       | An individual entry in the user’s search or navigation history, such as visited pages or searched verses.                                                   |
| `history`       | `Timestamp`          | The date and time when the specific history item was recorded.                                                                                              |
| `history`       | `User ID`            | A unique identifier linking the history item to a specific user.                                                                                            |

