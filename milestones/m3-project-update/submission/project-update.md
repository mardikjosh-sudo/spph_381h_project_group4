# M3 Project Update

## Project and audience

**Title:** Opioid Toxicity Death Rates Across Canada's Provinces and Territories, and the Male-to-Female Gap, 2016–2025

**Audience:** Provincial and regional public-health decision makers who need a concise, qualified view of published opioid mortality surveillance.

## Refined question

How did PHAC's reported annual crude rate of apparent opioid toxicity deaths vary across Canada's provinces and territories from 2016 to 2025? Where both sex-specific rates are available, how did the reported male-to-female rate ratio vary?

## Data and analytic sample

We use the September 22, 2026 Public Health Agency of Canada *Opioid- and Stimulant-related Harms in Canada* CSV snapshot committed at `data/SubstanceHarmsData.csv`. We selected annual opioid-death crude rates for 2016–2025: 420 rate records forming 140 region-years across 13 provinces and territories plus the separate Canada reference series. The availability audit retains all 140 region-years. After checking availability across every region and measure, Table 1 uses the common 2016–2024 window; it has 125 eligible region-years after excluding partial-year Nunavut 2023. Each compact table cell shows its own contributing-year count because suppression and unavailability differ by measure. The 2025 values remain in the annual figures and endpoint comparison, with reporting-change cautions for British Columbia, Quebec, and Canada. Suppressed and unavailable values remain missing; published zeroes remain zero.

## Current finding

The published Canada overall crude rate was 7.8 deaths per 100,000 in 2016 and 16.2 in 2024. This endpoint difference is supported by the fixed source CSV and the code-generated report. It does not establish a steady rise, explain the change, or make crude regional rates directly comparable. The jurisdiction panels show important variation and gaps that a single national value obscures.

## Decision needing review

We revised Table 1 in response to M2 feedback: it now groups the four key measures by region, omits individual year lists, and reports `n` in each cell. We need feedback on whether the matched-year rule for Yukon and the Northwest Territories is clear, whether the small-multiple figure communicates regional variation, and whether the 2025 comparability cautions are prominent enough. We also need advice on whether the male-to-female ratio should remain a secondary figure, given suppression and undefined ratios in several smaller jurisdictions.

## Next steps

Review the report and preview with peers; check figure labels, cautions, and interpretation against the PHAC technical notes; simplify the final knowledge-translation view in response to feedback; and have another group member render the report from the committed repository before the final submission.