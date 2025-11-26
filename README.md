# Norwegian Wordlists

All data in this repository is sourced from the Norwegian word bank datasets provided by [Språkbanken](https://www.nb.no/sprakbanken/).
The lists include lemma forms from both **Norwegian Bokmål (no-nb)** and **Norwegian Nynorsk (no-nn)**.

These files are intended for use in NLP, linguistics, password/passphrase generation, and other text-processing applications.

## combined-lemma-wordlist.txt (146106 words)
This file contains the **merged unique lemma forms** from the [2019 and 2022 word banks](https://www.nb.no/sprakbanken/ressurskatalog/oai-nb-no-sbr-5/) released by Språkbanken.

The list is **unfiltered** and **unprocessed**, representing the raw lemma vocabulary as published in the source datasets.
Its purpose is to provide a clean, deduplicated baseline before any filtering is applied.


## cleaned-source-wordlist.txt (9 409 words)

This file contains the **filtered and cleaned lemma list** derived from `combined-lemma-wordlist.txt`.

The following categories were removed to create a safe, general-purpose wordlist suitable for passphrase generation:

* profanity
* sexual terms
* slurs or hate terms
* drug and alcohol terminology
* violence-related terms
* medical and anatomy terms
* religious terms
* political terms
* place names
* personal names
* brand and product names
* dialect and archaic terms
* loanwords
* abstract weak and compound words

Only valid, neutral Norwegian lemmas remain.
This file serves as the **source for generating the diceware lists**.

**⚠ IMPORTANT**: Despite extensive filtering, some non-neutral or undesirable words may still remain.
Please review the data before using it in sensitive or production environments.

---

## **sorted-diceware-7776-no.txt** (7 776 words)

A deterministic, lexicographically **sorted Norwegian Diceware list** produced from `cleaned-source-wordlist.txt`.

It contains exactly **7 776 entries** (6⁵ combinations), suitable for reproducible password/passphrase generation.

---

## **random-diceware-7776-no.txt** (7 776 words)

A **randomized permutation** of the same 7 776-word diceware list.
This version can be used where ordering should be non-deterministic or uniformly shuffled.

---

## License

All wordlists in this repository are released under **CC0 1.0 Universal (Public Domain Dedication)**.
You may use, modify, redistribute, or incorporate them into any project—commercial or non-commercial—without attribution.

---

If you'd like, I can also generate:

* the `LICENSE` file
* a shields.io “Public Domain / CC0” badge
* a section explaining how the diceware lists are generated
* a pipeline diagram (optional)

Just tell me what to add.
