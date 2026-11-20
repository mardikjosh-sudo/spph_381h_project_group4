# AI-Use Note

## Audit trail

The seven inherited M2 code-audit entries below are copied verbatim from the group's M2 `ai-use-note.md`. Their verification describes M2. The M3 revision entries afterward describe the changed code and checks for this draft. Inline comments for unchanged code chunks are retained from the M2 QMD.

### Inherited M2 code-audit entries

**prepare-region-year-data (M2)**

### AI prompt

Read the PHAC CSV using repository-relative paths. Select annual opioid-death crude rates for 2016-2025 and reshape overall, male, and female values into unique region-years. Preserve zeroes and suppression labels, calculate ratios only with a positive female denominator, and flag partial-year coverage and the specified 2025 reporting changes.

### Verification

Checked source filters, unique keys, numeric values, zeroes, and raw suppression labels.

**missingness-and-export (M2)**

### AI prompt

Before exclusions, summarize availability of overall, male, female, and ratio values across all selected region-years. Include numeric and missing counts, missing percentages, and separate counts for suppression, unavailable values, and zero denominators. Display and export missingness-summary.csv.

### Verification

Compared all availability categories and percentages with separate base-R counts and the exported CSV.

**summary-eligibility (M2)**

### AI prompt

Create a summary dataset excluding partial-year Nunavut 2023 and the flagged 2025 records for BC, Quebec, and Canada. Retain the original panel for the availability audit and display the number excluded for each reason alongside the number of remaining region-years.

### Verification

Checked Nunavut 2023 and the three flagged 2025 rows against PHAC notes and the group's M1 plan.

**table1-and-export (M2)**

### AI prompt

Summarize each region and measure using eligible-year N, numeric N, missing N, and mean (sample SD) across available annual values. Handle groups with zero or one numeric value explicitly, round summaries to two decimals, and display and export the same table as table1.csv.

### Verification

Checked numeric-year N, means, and sample SDs with independent base-R summaries and CSV read-back.

**table1-and-export / endpoint-comparison (M2)**

### AI prompt

Align Yukon and Northwest Territories' overall means to years with both sex-specific rates reported, list the calendar years used in Table 1, and retain Prince Edward Island's independently reported overall series. Expand the endpoint comparison to 2016, 2024, and 2025, and organize the report under the M2 example's headings.

### Verification

Checked matched year sets and recalculated means against the prepared panel; compared endpoint values with the source CSV, including suppression and unavailable labels; confirmed the six report headings match the example.

**figure-overall-rates (M2)**

### AI prompt

Follow our M1 plan with one panel per province or territory, blue annual crude-rate trends, and a grey PHAC Canada reference. Preserve gaps, omit partial-year Nunavut 2023, and show flagged 2025 values as disconnected triangles. Use common zero-based axes and explain colours and markers.

### Verification

Checked plotted values against source rates and confirmed partial-year omissions and disconnected caution points.

**figure-sex-ratios (M2)**

### AI prompt

Plot annual male-to-female rate ratios by province or territory using common zero-based axes and a dashed reference at 1. Preserve gaps and disconnected flagged 2025 points, label panels with no defined ratios, and explain that missing ratios do not imply equality or describe gender identity.

### Verification

Checked ratios against male and female rates, positive denominators, missing-data gaps, and empty-panel labels.

### M3 revision audit

The M3 prompts below summarize the actual M2 feedback and subsequent requests to revise the report. They are representative prompt summaries, not verbatim historical chat transcripts.

**prepare-region-year-data — output path only**

# AI prompt: Keep the M2 data preparation unchanged, but write its generated CSV outputs under milestones/m3-project-update/submission/outputs.
# Verified: Compared this chunk with M2; only out_dir changed. Confirmed the fixed CSV hash and generated M3 CSV outputs after rendering.

**summary-eligibility — common window**

# AI prompt: Revise the M2 summary-eligibility chunk to use the same 2016–2024 calendar window for every region after checking data availability. Exclude partial-year Nunavut 2023, retain all 2016–2025 rows in the availability audit and figures, and display the Table 1 selection counts.
# Verified: Checked 126 region-years in 2016–2024 before the Nunavut exclusion, 125 afterward, and the 2025 and Nunavut cautions against the source data and PHAC technical notes.

**table1-and-export — compact regional table**

# AI prompt: Revise the M2 Table 1 chunk into one row per region and four columns: overall, female, male, and male-to-female ratio. Use the common 2016–2024 window, show mean (sample SD) and contributing-year n in each cell, remove year lists, and explain remaining n differences in the caption. Retain matched-year overall means for Yukon and the Northwest Territories and PEI's independently reported overall series.
# Verified: Audited availability across all 14 regions and four measures; independently recalculated all 56 exported table cells from the CSV and checked the matched-year counts (Yukon n=4; Northwest Territories n=5).

## What AI helped with

ChatGPT (Codex) adapted the M2 analysis into the M3 report, revised the summary window and Table 1 after the M2 feedback, and helped draft the report and submission notes. The unchanged missingness, endpoint, and plotting chunks retain their M2 code and audit comments.

## What I changed

The M3 preparation chunk writes outputs to the M3 folder. The summary chunk now uses 2016–2024 across regions, and Table 1 now has one row per region, four key measures, and a contributing-year count in each cell. I retained the M2 matched-year rule for Yukon and the Northwest Territories, excluded partial-year Nunavut 2023, and kept 2025 in the annual figures and full availability audit.

## How I verified the result

Compared the M2 and M3 code chunks to identify four unchanged chunks and three revisions. Checked the fixed CSV fingerprint, the region-year selection and availability counts, and PHAC's technical notes for partial-year coverage and 2025 reporting changes. Independently recalculated all 56 Table 1 cells from the CSV and compared them with `outputs/table1.csv`; the report rendered after the code revisions.