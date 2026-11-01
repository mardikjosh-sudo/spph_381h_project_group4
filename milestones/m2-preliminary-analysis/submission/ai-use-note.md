# AI-Use Note

## Audit trail

```text
# AI prompt: Read the PHAC CSV as text using repository-relative paths.
# Select annual opioid-death crude rates for 2016-2025 and reshape overall,
# male, and female values into unique region-years. Preserve zeroes and
# suppression labels, calculate ratios only with a positive female denominator,
# and flag partial-year coverage and the specified 2025 reporting changes.
# Verified: Checked source filters, unique keys, numeric values, zeroes, and raw suppression labels.

# AI prompt: Before exclusions, summarize availability of overall, male, female,
# and ratio values across all selected region-years. Include numeric and missing
# counts, missing percentages, and separate counts for suppression, unavailable
# values, and zero denominators. Display and export missingness-summary.csv.
# Verified: Compared all availability categories and percentages with separate base-R counts and the exported CSV.

# AI prompt: Create a summary dataset excluding partial-year Nunavut 2023 and
# the flagged 2025 records for BC, Quebec, and Canada. Retain the original panel
# for the availability audit and display the number excluded for each reason
# alongside the number of remaining region-years.
# Verified: Checked Nunavut 2023 and the three flagged 2025 rows against PHAC notes and the group's M1 plan.

# AI prompt: Summarize each region and measure using eligible-year N, numeric N,
# missing N, and mean (sample SD) across available annual values. Handle groups
# with zero or one numeric value explicitly, round summaries to two decimals,
# and display and export the same table as table1.csv.
# Verified: Checked numeric-year N, means, and sample SDs with independent base-R summaries and CSV read-back.

# AI prompt: Create a side-by-side table of each region's published overall
# crude rate in 2016 and 2024. Preserve the original suppression and unavailable
# labels, and explain that these endpoints do not describe the full trajectory.
# Verified: Compared the displayed cells directly with the source CSV, including suppressed and unavailable labels.

# AI prompt: Follow our M1 plan with one panel per province or territory,
# blue annual crude-rate trends, and a grey PHAC Canada reference. Preserve gaps,
# omit partial-year Nunavut 2023, and show flagged 2025 values as disconnected
# triangles. Use common zero-based axes and explain colours and markers.
# Verified: Checked plotted values against source rates and confirmed partial-year omissions and disconnected caution points.

# AI prompt: Plot annual male-to-female rate ratios by province or territory
# using common zero-based axes and a dashed reference at 1. Preserve gaps and
# disconnected flagged 2025 points, label panels with no defined ratios, and
# explain that missing ratios do not imply equality or describe gender identity.
# Verified: Checked ratios against male and female rates, positive denominators, missing-data gaps, and empty-panel labels.
```

## What AI helped with

ChatGPT (Codex) helped prepare the annual PHAC region-year dataset, preserve suppression labels, calculate valid male-to-female ratios, and document missingness and exclusions.

## What I changed

The analysis was adapted to our PHAC dataset and M1 plan, with explicit handling of suppression, zero denominators, partial-year coverage, and reporting changes. The report includes code-generated CSV exports, a Canada reference series, and wording that avoids causal claims.

## How I verified the result

Preparation checks with Codex compared source filters, region-year counts, missingness categories, and ratio denominators against the repository CSV. Summary counts, means, and sample SDs were checked with separate base-R calculations, while endpoint values and figures were compared with the prepared data and PHAC technical notes. The report rendered successfully using relative paths.