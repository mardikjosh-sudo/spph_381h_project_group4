# Data Intake Card

## Data source and steward

Our source is the Public Health Agency of Canada’s (PHAC) Opioid- and Stimulant-related Harms in Canada dataset. PHAC publishes the national surveillance data using information supplied by provincial and territorial partners, including offices of Chief Coroners and Chief Medical Examiners for deaths. Our project examines apparent opioid toxicity deaths, not hospitalizations, emergency department visits, or stimulant-related harms.

Source: Government of Canada dataset record. The release in our repository was last updated September 22, 2026; we accessed it October 26, 2026.

## Access method

The report is publicly accessible. The [main surveillance page](https://health-infobase.canada.ca/substance-related-harms/opioids-stimulants/) provides a ZIP data download. We downloaded the September 2026 release and placed SubstanceHarmsData.csv at data/SubstanceHarmsData.csv in our group repository. Accessed October 26, 2026. The dataset uses the Open Government Licence – Canada.

## File format

The download is a ZIP archive containing a CSV file and a README. The CSV contains public, aggregate surveillance values rather than individual records.

## Unit of analysis

Our planned analysis will use an aggregate demographic group for a particular substance, harm type, and reporting period, rather than individual patient records. The exact row structure has been confirmed.

## Key variables

- Age group
- Reported sex
- Substance category: opioids or stimulants
- Harm type: deaths, hospitalizations, emergency department visits, or available EMS responses
- Reporting year
- Reported count or percentage, where available

## Privacy and stewardship

We will use public aggregate results, preserve suppression and missing-value labels, and avoid attempts to identify individuals. We will document the download date and retain source definitions.

## Equity and interpretation

Coverage differs across harm types and jurisdictions. Percentages describe the distribution of recorded harms; they do not directly measure population risk. We will avoid stigmatizing language and will not interpret reported sex as gender identity.

## Indigenous data governance

The data set does not present an Indigenous-identity breakdown. The downloaded data and documentation have been reviewed. If our analysis involves Indigenous identifiers, communities, territories, or services, we will consult the course’s Week 1 guidance before proceeding.
