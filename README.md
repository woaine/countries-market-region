# Countries by Market Region Dataset

This repository provides a dataset derived from the ISO 3166-1 country listings merged with UN Geoscheme regional classifications. It retains only the following attributes—country name, alpha-2 code, region, and sub-region—and introduces a new column, `market-region`, to classify countries into the four most common business regions.

## Data Schema

- `name`: Official country name
- `alpha-2`: ISO 3166-1 alpha-2 country code  
- `region`: UN Geoscheme region
- `sub-region`: UN Geoscheme sub-region  
- `market-region`: Business region grouping (APAC, LATAM, NA, EMEA)

## Market Regions

The `market-region` segments countries into one of four categories:

- **APAC**: Asia–Pacific markets
- **LATAM**: Latin America and the Caribbean  
- **NA**: North America  
- **EMEA**: Europe, Middle East, and Africa  

**Note:** Antarctica isn’t included in APAC, LATAM, NA, or EMEA. Governed by the Antarctic Treaty System and lacking a permanent commercial market, it’s tracked separately under "Other." To preserve data completeness, Antarctica is labeled "Antarctica" in both its UN Geoscheme region and sub-region fields, which would otherwise be empty.

## Sample Data

Below is a snapshot of the dataset, illustrating how Antarctica is handled:

| name         | alpha-2 | region      | sub-region                         | market-region |
|--------------|---------|-------------|------------------------------------|---------------|
| Antarctica   | AQ      | Antarctica  | Antarctica                         | Other         |
| Afghanistan  | AF      | Asia        | Southern Asia                      | APAC          |
| Albania      | AL      | Europe      | Southern Europe                    | EMEA          |
| Argentina    | AR      | Americas    | Latin America and the Caribbean    | LATAM         |
| Canada       | CA      | Americas    | Northern America                   | NA            |

Refer to the `data/processed/market_region.csv` file for the full dataset.

## References

This dataset is a derivative work of [ISO-3166 Country and Dependent Territories Lists with UN Regional Codes (v10.0)](https://github.com/lukes/ISO-3166-Countries-with-Regional-Codes) by [lukes](https://github.com/lukes).
