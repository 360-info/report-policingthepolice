# `/data`

Files here represent data extracted from the Global Trustworthiness Index, published annually by Ipsos. They rank professions by the percentage of survey respondents who rate people of that profession as generally trustworthy or untrustorthy.

The survey covers people across a couple dozen countries and are available both as an average for the surveyed countries and broken down by country.

## Rights

[Ipsos: Permission to use Documents](https://www.ipsos.com/en/legal-mentions):

> Polls appearing on this website are deemed to be in the public domain and therefore may be used in whole or in part as long as attribution is made to the appropriate Ipsos entity that conducted the work.

## Files

### `ipsos-trust-professions-global.csv`
Results as an average for all surveyed countries each year ([source](https://www.ipsos.com/en/trust/trust-professions-return-status-quo-ante)). Columns include:

- `profession`: The profession asked about
- `year`: The year of the survey
- `pct_trust`: The percentage (1–100) of respondents rating the profession as either trustworthy or very trustworthy

### `ipsos-trust-professions-bycountry.csv`
Results broken down by each country, each year (sources: [2022](https://www.ipsos.com/sites/default/files/ct/news/documents/2022-07/Global%20trustworthiness%202022%20Report.pdf), 
  [2021](https://www.ipsos.com/sites/default/files/ct/news/documents/2021-10/Global-trustworthiness-index-2021.pdf), 
  [2019](https://www.ipsos.com/sites/default/files/ct/news/documents/2019-09/global-trust-in-professions-trust-worthiness-index-2019.pdf)). Columns include:

- `country_code`: A 3 letter code for the country. This is _not_ necessarily an ISO 3166-1 alpha-3 code and is not consistent between years—rely on the `country_name` for country disambiguation.
- `country_name`: The name of the country
- `year`: The year of the survey
- `occupation`: The profession asked about
- `trust`: The percentage (1–100) of respondents rating the profession as either trustworthy or very trustworthy
- `neither`: The percentage (1–100) of respondents rating the profession as neither trustworthy nor untrustworthy
- `distrust`: The percentage (1–100) of respondents rating the profession as either untrustworthy or very untrustworthy

### `ipsos-trust-police-vs-others-bycountry.csv`

Results as `ipsos-trust-professions-bycountry.csv`, but all occupations other than "The police" have been aggregated into a mean figure called "Other occupations" for each country/year combination.

### `ipsos-trust-professions-bycountry-20??-[dis]trust.csv`
Source files transcribed from the annual Ipsos reports. For results in a tidier form, see `ipsos-trust-professions-bycountry.csv` above.
