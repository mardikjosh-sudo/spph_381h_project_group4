# M3 Project Update

## Project and audience

**Title:** Public Health Agency of Canada Surveillance Data: Trends in Apparent Opioid Toxicity Death Rates and Male-to-Female Rate Ratios Across Canada's Provinces and Territories, 2016–2025

**Audience:** Provincial and regional public-health decision makers who need a concise, qualified view of published opioid mortality surveillance.

## Refined question

How did PHAC's reported annual crude rate of apparent opioid toxicity deaths vary across Canada's provinces and territories from 2016 to 2025? Where both sex-specific rates are available, how did the reported male-to-female rate ratio vary?

## Data and analytic sample

We use the September 22, 2026 Public Health Agency of Canada *Opioid- and Stimulant-related Harms in Canada* CSV snapshot committed at `data/SubstanceHarmsData.csv`. We selected annual opioid-death crude rates for 2016–2025: 420 rate records forming 140 region-years across 13 provinces and territories plus the separate Canada reference series. The availability audit retains all 140 region-years. After checking availability across every region and measure, Table 1 uses the common 2016–2024 window; it has 125 eligible region-years after excluding partial-year Nunavut 2023. Each table cell shows its contributing-year count. Counts vary because of suppression and unavailability; additionally, the Yukon overall mean uses only the four years when both sex-specific rates are reported, and the Northwest Territories overall mean uses only five such years. The 2025 values remain in the annual figures and endpoint comparison, with reporting-change cautions for British Columbia, Quebec, and Canada. Suppressed and unavailable values remain missing; published zeroes remain zero.

## Current finding

PHAC reported a Canada crude rate of 7.8 deaths per 100,000 in 2016 and 16.2 in 2024. These two years do not show what happened in between or explain why the rate changed. Because crude rates are not adjusted for age, they should not be used to rank jurisdictions. The jurisdiction panels show important variation and gaps that a single national number can hide.

## Decision needing review

We revised Table 1 in response to M2 feedback: it now groups the four key measures by region, omits individual year lists, and reports `n` in each cell. We need feedback on whether the matched-year rule for Yukon and the Northwest Territories—and the reason for restricting their overall means to those years—is clear. We also need feedback on whether the small-multiple figure communicates regional variation, whether the 2025 comparability cautions are prominent enough, and whether the male-to-female ratio should remain a secondary figure given suppression and undefined ratios in several smaller jurisdictions.

## Next steps

Review the report and preview with peers; check figure labels, cautions, and interpretation against the PHAC technical notes; simplify the final knowledge-translation view in response to feedback; and have another group member render the report from the committed repository before the final submission.