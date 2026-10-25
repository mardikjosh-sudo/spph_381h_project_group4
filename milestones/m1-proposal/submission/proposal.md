
# Project Proposal:

## Project Title: 
Opioid Death Rates Across Canada's Provinces and Territories, and the Male-to-Female Gap, 2016-2025

## Group Members: 
Sky, Tyler, Josh, Nicolas


## Audience and KT Purpose:
Our audience is provincial and regional health policy makers and public-health authorities. The project gives them a descriptive picture of the opioid toxicity death burden in Canada. It shows which provinces and territories have had the highest and lowest death rates, how each compares with the Canada-wide rate, and whether the burden falls equally on men and women. The aim is to inform discussion about where closer analysis and attention may be needed, not to recommend a specific policy or funding decision.

The caution we will keep visible is that these are crude, descriptive surveillance rates. The analysis does not explain why rates changed, and comparisons between provinces should be read with differences in age structure and population size in mind.

## Question:
### Primary: 
How have opioid-related death rates (crude rate, expected to be per 100,000 population) changed across Canadian provinces and territories from 2016 to 2025?
### Secondary:
Does the male-to-female gap in opioid death rates differ across provinces, and has it changed over time?

## Expected Data Source
We will use the public dataset Opioid and Stimulant related Harms in Canada (2016-2026), published by the Public Health Agency of Canada (PHAC) under the Open Government Licence - Canada, available through the Government of Canada Open Government portal and Health Infobase.
## Planned Output

### Cleaned Data Table
- One row per region and year
- Columns:
  - Crude death rate
  - Male rate
  - Female rate
  - Male-to-female ratio
  - Possibly a column describing why data is missing (e.g., suppressed or not reported)

### Two Figures
- **Figure One (Primary Question):** Multiple line chart of the crude death rate by year, one panel per region. The Canadian average is also shown in each chart.
- **Figure Two (Secondary Question):** Line chart of the male-to-female rate ratio by year, one panel per region.

### Quarto Report and Dashboard-Style Page
- **Report:** A Quarto report presenting the cleaned table, both figures, and a discussion of limitations.
- **Dashboard:** Interactive in style, allowing viewers to pick a region and see that region's opioid death rate trend and its male-to-female ratio.

## Known Limitations
From reading the technical notes posted by the Government of Canada:
- Use of crude rate implies a lack of adjustment for differences in age structures, so differences could result from differences in age structure.
- The data for some small regions is suppressed and has small counts, which may lead to misleading results.
- 2026 data is not fully available, so our analysis will be between 2016 and 2025.
- Data is descriptive, so it cannot be used to support causal claims.
- Data for recent years may be undercounted, as provinces only count deaths with completed investigations, which can take 3-24 months.