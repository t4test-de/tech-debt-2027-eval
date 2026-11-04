# Owed, Not Missing: Traceability Debt as Unsatisfied Path Obligations

Supplementary material for a doubly-anonymous submission to TechDebt 2027.
Author and affiliation details are omitted until notification.

This repository holds the obligation declarations evaluated in Section VII of
the paper and the four trace graphs they were evaluated over, so that the
reported figures can be recomputed and a disagreement about a number can be
located in a declaration rather than in a result.

## Contents

| File | What it is |
|---|---|
| `supplementary-declarations.txt` | Every obligation evaluated in Section VII, in the declarative notation of Figure 1, one clause per line, each naming the clause or internal process item it derives from |
| `automotive-power-window.xlsx` | Driver door power window: 136 requirements, 119 tests, 18 architectural elements |
| `airborne-landing-gear.xlsx` | Landing gear position indication: 121 requirements, 102 tests |
| `medical-pulse-oximeter.xlsx` | Pulse oximeter: 122 requirements, 105 tests, 12 risk controls, 10 hazards |
| `dronology-trace-graph.xlsx` | Public Dronology dataset: 398 artifacts, 596 parent-child links, 892 artifact-to-file links, 225 files |

## Clause vocabulary

`FROM` population · `TO` admissible terminals · `VIA` admissible routes ·
`TARGET` individual or aggregate · `DEPTH` classification-dependent depth ·
`QUANTIFY` coverage or justification · `BASELINE` scope per hop ·
`AGREE` attributes that must hold along the path · `EXCEPT` typed exception and
its discharge duty · `DISCHARGE` existential or joint · `SOURCE` provenance.

The declarations file groups the obligations by subject and states, for each,
the clause it derives from. Where no normative source governs a subject, as
with Dronology, the declaration states the project convention it encodes
instead.

## Reproducing the reported figures

Each workbook carries an Index sheet naming its scope, artifact and link
sheets, and a gap sheet. The numbers in Section VII are recomputable from those
sheets together with the matching declaration.

The comparison point, link-pair evaluation, tests only whether the `FROM` item
carries a link of the terminal type directly; it ignores `VIA`, `TARGET`,
`DEPTH`, `QUANTIFY`, `AGREE`, `EXCEPT` and `DISCHARGE`. The difference between
the two columns of Table IV is the whole of the empirical claim.

Counts are of artifacts, not of links: an item whose descendants carry the
evidence is counted once. Where an ancestor and its descendant both fail the
same obligation, repaying the descendant discharges the ancestor, so the paper
reports both the raw count and the count of independent repayment items.

## Provenance

The automotive, airborne and medical subjects are purpose-built and
anonymised: no product, customer, project or author name appears in any sheet,
in any index title, or in the file metadata. They are constructed to exhibit
the failure classes the paper names, not sampled from a population, which is
stated as a threat to external validity. No frequency claim is drawn from them.

The Dronology graph is derived from the public dataset of Cleland-Huang,
Vierhauser and Bayley, *Dronology: An Incubator for Cyber-Physical System
Research*, ICSE-NIER 2018, pp. 109-112, doi:10.1145/3183399.3183408.

Normative sources are cited in the declarations file by clause. Standard text
is licensed and is not reproduced.
