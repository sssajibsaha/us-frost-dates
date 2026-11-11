# US Frost Dates by NOAA Station (1991-2020 Normals)

Median and cautious last spring and first fall freeze dates for 2357 US weather stations, compiled by [Garden Clock](https://gardenclock.com/frost-date-dataset/).

## Files

- `gardenclock-us-frost-dates-1991-2020.csv`: one row per station
- `datapackage.json`: machine-readable schema (Frictionless Data)

## Columns

| Column | Type | Description |
|---|---|---|
| `station_id` | string | NOAA GHCN station identifier |
| `station_name` | string | NOAA station name |
| `city` | string | Place name used by Garden Clock |
| `state` | string | Two-letter US state or territory code |
| `latitude` | number | Decimal degrees |
| `longitude` | number | Decimal degrees |
| `median_last_spring_freeze` | string | MM-DD, median (50 percent) last spring date at or below the threshold |
| `cautious_last_spring_freeze` | string | MM-DD, later and safer spring date from the same NOAA probability tables |
| `median_first_fall_freeze` | string | MM-DD, median (50 percent) first fall date at or below the threshold |
| `cautious_first_fall_freeze` | string | MM-DD, earlier and safer fall date from the same NOAA probability tables |
| `threshold_f` | integer | Temperature threshold in degrees Fahrenheit (32 for all rows) |

## Method

Source: NOAA NCEI 1991-2020 U.S. Climate Normals (standard-quality station records), retrieved 2026-10-21. Archive: https://www.ncei.noaa.gov/data/normals-annualseasonal/1991-2020/archive/us-climate-normals_1991-2020_v1.0.1_annualseasonal_multivariate_by-station_c20230404.tar.gz
Archive SHA-256: `0fdb814203150780d4ee0c5d53c7844a237a21881101fb7d922b0aa3a1fd190f`. Records scanned: 15616.
Only named stations with four standard-quality 32 F freeze dates and a spring-to-fall season are included. Frost-free and year-round-freeze locations are excluded, so coverage is not every town or ZIP code.
The median is the 50 percent probability date. The cautious dates are the safer-side dates from the same NOAA probability tables, as explained at https://gardenclock.com/frost-date-probabilities-explained/ . Dates are MM-DD with no year. These are historical statistics, not forecasts, and a station may not match conditions at a specific garden.

## License

Creative Commons Attribution 4.0 (CC BY 4.0). The underlying NOAA data is a US government work. Please credit Garden Clock and link to https://gardenclock.com/frost-date-dataset/

## Cite

`Saha, S. (2026). US Frost Dates by NOAA Station (1991-2020 Normals), version 2026-10-21. Garden Clock. https://gardenclock.com/frost-date-dataset/`

## Corrections

Report a questionable value through https://gardenclock.com/contact/
