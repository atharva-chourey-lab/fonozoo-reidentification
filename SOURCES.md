# Sources Map — Dead Names in a Frozen Archive (Fonozoo re-identification)

Author: Atharva Chourey
Affiliation: Atharva Chourey Lab (independent research lab)

*Manuscript — not yet peer-reviewed.*

This file maps every key number, verdict and reference in `paper.md` to the source file it was taken from. Nothing in the paper was taken from a source outside this list.

## Primary sources

- `~/workspace/fonozoo-reidentification/MANUSCRIPT.md` — the full manuscript draft (not submitted to any venue). `paper.md` in this repository is that manuscript with only the header/status block converted to the lab's publication format; no result, number or claim was altered.
- `~/workspace/fonozoo-reidentification/PREREGISTRATION.md` — the registered design, fixed before the resolution run.
- `~/workspace/fonozoo-reidentification/NOVELTY.md` — the novelty scrub: no published study re-identifies a pre-DNA sound archive name-by-name against a current backbone and reports the rate.
- `~/workspace/fonozoo-reidentification/RESULTS-EXHAUSTED.md` and `RESULTS.md` — the run records.
- `~/workspace/fonozoo-reidentification/results/summary.json` — GBIF classification summary. Recomputed during the publication build: recordings MOVED 129 + SYNONYM 15 + SPLIT-ELEVATED 2 = 146 changed of 629 countable = 23.2% — matches the manuscript.
- `~/workspace/fonozoo-reidentification/results/fnjv_summary.json` — the FNJV control summary: 61 of 5,793 firm-named recordings changed = 1.1%; 11 of 694 names = 1.6% — matches the manuscript.
- `~/workspace/fonozoo-reidentification/results/region_summary.json`, `catalogue_join_summary.json`, `split_resolutions.json`, `asw_crosscheck_summary.json` — region structure, catalogue join, split verdicts, and the Catalogue of Life second-ruler run.
- `~/workspace/fonozoo-reidentification/data/` — inventory.csv (1,013 recovered files with URLs, sizes, checksums), classifications.csv, resolutions.csv, catalogue_join.csv, region_assignments.csv, and the FNJV tables. The per-recording tables are also released in the lab's goldmine-hunter repository (spin-off record).
- `~/workspace/fonozoo-reidentification/scripts/` — the recovery and resolution code.

## Key numbers and their sources

| Claim in paper | Value | Source file |
|---|---|---|
| Recovered pile | 1,013 audio files, each verified HTTP 200 with checksum at capture | MANUSCRIPT.md §2; data/inventory.csv |
| Countable recordings | 629 firm species-named (of 636 firm, after registered exclusions) | results/summary.json (recomputed) |
| Changed recordings | 146 (23.2%): 129 MOVED, 15 SYNONYM, 2 SPLIT-ELEVATED | results/summary.json (recomputed) |
| Split-ambiguous | 6 recordings (5 names); 4 resolved by the catalogue join | results/summary.json; split_resolutions.json |
| Name-level rate | 128 of 561 firm names changed (22.8%) | MANUSCRIPT.md §3.1 |
| Region structure | Neotropical 30.7% (119/388); Palearctic 16.0% + 16.0% split-ambiguous; Madagascar 5.7% (10/175) | results/region_summary.json |
| Second ruler | COL agrees on 501/573 names (87.4%); 18 genuine disagreements; 47 matcher artefacts; COL rate 24.2% | results/asw_crosscheck_summary.json |
| FNJV control | 61/5,793 recordings changed (1.1%); 11/694 names (1.6%) | results/fnjv_summary.json (recomputed) |
| Catalogue join | FZ_AMPHIBIA 3,618 Darwin Core records; name-level envelope covers 163/636 firm recordings | catalogue_join_summary.json |

## Novelty and framing notes

- The claim is a measurement — the dead-name burden of one frozen archive against a maintained control — stated with its declared limitations (names only, no re-listening; the split screen is a lower bound; region is a genus-level proxy). All six limitations in the paper's §5 are carried over unedited.
- Backbone results are versioned snapshots (GBIF Backbone and Catalogue of Life release 26.11, accessed 2026-11-18); the paper says so and names its backbones, as it recommends.
- The recovered audio remains the Fonoteca Zoológica's (MNCN-CSIC) and is not redistributed anywhere in this publication; the inventory records URLs, sizes and checksums only.
