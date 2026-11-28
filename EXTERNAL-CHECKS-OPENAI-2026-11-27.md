# External checks by OpenAI agents — 2026-11-27

This lab's work is a human–AI collaboration, and outside AI systems are
part of how it gets checked. On 2026-11-27, agents from **OpenAI**
independently re-ran parts of this study against the public tables and
reported two findings. Both were then reproduced independently by the
lab from its own local data before being recorded here. We are grateful
for the scrutiny; this file is the standing record of what they found.

## Finding 1 — the Fonozoo/FNJV gap is not a species-mix artefact

Restricting the comparison to the **134 accepted species present in both
archives** and weighting each species equally, **33.6%** of Fonozoo
recordings had changed names versus **0.9%** in FNJV. The headline gap
therefore does not arise from the two archives holding different species.

*Lab verification:* reproduced exactly (134 shared accepted species;
33.6% vs 0.9%), with split-ambiguous recordings excluded from the
denominator, consistent with the paper's rule that split-ambiguous
filings are flagged, never guessed. (Including them gives 33.2% for
Fonozoo; the conclusion is unchanged.)

*Open question, as the OpenAI agents themselves noted:* this control
does not separate how much of the gap is due to recording age versus
curation. Fonozoo's filenames are frozen at guide publication; FNJV's
exported names are the catalogue's current, curated names. That
asymmetry is stated in the paper.

## Finding 2 — `classifications.csv` does not reproduce the paper on its own

Weighting the public `classifications.csv` by its `n_recordings` column
gives 472 unchanged recordings, not the paper's 469. The file counts
**one extra unchanged recording for each of three species**. Using the
per-file inventory instead recovers the paper's headline exactly:
**146/629 changed (23.2%)**. The paper's headline stands; it is the
CSV's weights that need fixing.

*Lab verification and root cause:* confirmed. The three species are
*Boophis marojezensis*, *Boophis microtympanum* and *Spinomantis
bertini*. Each has a second, provisional (cf./aff.) filing under the
same filed name, and the name-resolution step pooled firm and
provisional filings when counting recordings per name, inflating each
firm count by one. The per-file tables were never affected.

## Status

- The manuscript's headline, abstract and control numbers are
  unaffected.
- One derived number in the manuscript (the Madagascar region share,
  computed from the weighted table) shifts trivially when the weights
  are corrected: 10/175 (5.7%) → 10/172 (5.8%).
- The CSV weight fix, the region-number correction, and a short
  manuscript paragraph reporting Finding 1's shared-species control
  are scheduled as one revision pass. The manuscript is not yet
  submitted, so this is a pre-submission fix, not a correction.

*Recorded 2026-11-27 by Atharva Chourey Lab. Credit for both findings:
OpenAI agents (external checkers). Independent reproduction: the lab.*
