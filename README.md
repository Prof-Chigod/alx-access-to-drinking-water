# alx-access-to-drinking-water
ALX integrated project: WHO/UNICEF JMP 2020 drinking-water access analysis in spreadsheets.
# Access to drinking water (2020)

Spreadsheet analysis of WHO/UNICEF JMP estimates on drinking-water service levels.

## Data
- Source: WHO/UNICEF Joint Monitoring Programme, Estimates on the use of water (2020)
- Unit notes: `pop_n` is population in thousands; service columns are percentages
- Missing values appear as NAN

## What I did
1. Imported a mixed comma/semicolon CSV and repaired five split rows with COUNTA + filter
2. Compared dataset population to the 7.821 billion world estimate
3. Built urban/rural shares and a population-vs-urbanisation chart
4. Computed max, min, mean, median, mode, quartiles, IQR for 12 service features
5. Built 100% stacked columns for national, urban, and rural access
6. Pivoted access by World Bank income group

## Files
- `Estimates on the use of water (2020).csv` — raw extract
- `access_to_drinking_water_2020.xlsx` — cleaned data, Global 2020 Report, charts

## Main findings
- Dataset national population is within ~0.44% of the 2020 world estimate
- Basic water is near-universal in high-income countries; low-income countries average ~63% basic
- Rural distributions are much wider than urban ones
