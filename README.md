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

# Undertanding the datasets
<img width="904" height="386" alt="image" src="https://github.com/user-attachments/assets/963930f1-1d3a-4b14-b577-d9c2970528c8" />
Identity
Name: Representing country or area.
Income_group: High / Upper middle / Lower middle / Low, or NAN if unpublished.
Population
Pop_n:  national population in thousands (not millions, not people).
pop_u : A percentage of  urban population, not a count of people.
National water (_n)
Wat_bas_n: % with at least basic water (safely managed + basic).
Wat_lim_n: % limited (improved source, >30 min away).
Wat_unimp_n:  % unimproved (unprotected well/spring).
Wat_sur_n:  % surface water (river, lake, pond, canal).
Rural water (_r):  has four levels, rural residents only: wat_bas_r, wat_lim_r, wat_unimp_r, wat_sur_r.
Urban water (_u): same four levels, urban residents only: wat_bas_u, wat_lim_u, wat_unimp_u, wat_sur_u.
Columns you added
Pop_u_val: urban people in thousands: pop_n * pop_u / 100.
Pop_r: rural %: 100 - pop_u.
pop_n (m): population in millions, rounded up (charts).
wat_bas_n (rounded): basic % forced not to stay above 100.
pop_u (rounded) / pop_r (rounded): whole-number shares for axes.
NAN means “no estimate,” not zero. A place that is 100% urban often has NAN on every rural water column.


