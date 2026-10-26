# Reproducibility plan

We will use `data/`, `scripts/`, `figures/`, `report/`, `dashboard/`, and `milestones/` folders. Scripts and Quarto files will use paths relative to the group repository root. Tables, figures, and rendered pages will be generated from code.

Our source is PHAC’s public *Opioid- and Stimulant-related Harms in Canada* CSV. The supplied September 22, 2026 release was used for a feasibility check. We will document its [download location](https://health-infobase.canada.ca/substance-related-harms/opioids-stimulants/), release date, file checksum, and the filters used. **We do not need to commit the dataset for M1.** Before M2, we will decide how to preserve the exact version used for results, because PHAC updates the online download.

The preparation code will select `Opioids`, `Deaths`, `By year`, 2016–2025, and `Crude rate`. It will reshape the overall, male, and female values into one row per region and year while retaining `Suppr.`, `n/a`, reported zero, and partial-year coverage as distinct conditions. A male-to-female ratio will be calculated only when both rates are reported and the female rate is greater than zero. We will check region-year uniqueness, row counts, missingness, and the resulting figures against the source.

R and Quarto are the planned tools. The visual code uses `readr`, `dplyr`, `tidyr`, and `ggplot2`; package versions and any later dependencies will be recorded. Another student should be able to obtain the documented PHAC data version, run the scripts from the repository root, and render the named Quarto report. Generated outputs will not be edited by hand.

**Feasibility check:** The supplied CSV loaded successfully. The selected data contain 140 Canada-or-jurisdiction/year rows for 2016–2025: 134 reported overall rates and 111 defined male-to-female ratios. These totals include Canada.