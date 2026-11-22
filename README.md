# VehicleLens — Exploring Indian Vehicle Registration Trends

VehicleLens is a personal data analytics project I built to explore how vehicle registrations in an Indian dataset vary over time, across states, and by manufacturer, vehicle category and fuel type. I turned the source CSVs into an interactive dashboard so readers can go from a broad trend, such as a shift in fuel mix, to the states, brands and models behind it.

## What you can explore

- **Registration trends** — View annual and monthly registration counts, year-over-year growth, category shares and the split between new and resale registrations. A three-month moving average helps reveal trends in monthly volume.
- **State comparisons** — Use an interactive map to compare registration volume, vehicle mix, EV share and growth. Select a state to open its report card.
- **Manufacturers and models** — Explore rankings for two-wheelers and four-wheelers, browse an A–Z brand directory, and see each manufacturer's model lineup and registration breakdown.
- **Fuel mix and electrification** — Track how petrol, diesel, gas, hybrids and pure electric vehicles contribute to the sample over time. Compare states by both EV registration count and EV share.
- **Vehicle search and comparison** — Search by brand or model and compare two models from the same category using registration counts, fuel type, vehicle weight and other available attributes.
- **Printable report cards** — Generate a summary for a state or manufacturer and save it as a PDF using the browser's print menu.

## How I prepared and analysed the data

I started with 500,000 source rows and excluded five with invalid registration years. The remaining **499,995 rows** represent **2,806,654 registrations within the sample** across **35 states and union territories**.

- Used `vehicleCount` to calculate registration totals and weighted summaries because one row can represent multiple registrations.
- Consolidated selected Tata and Volkswagen/Škoda manufacturer names, reducing 1,244 raw names to 1,238 groups. Grouped models by manufacturer, normalized model name and vehicle category.
- Calculated annual metrics using calendar years, kept hybrids separate from pure EVs, and excluded zero or missing weights from average gross vehicle weight.
- Built the dashboard with HTML, CSS, JavaScript and Chart.js, combining charts, tables, an interactive map and printable summaries.

## Run locally

Download the dashboard HTML file from this repository and open it in a web browser. Chart.js and the optional online vehicle lookup use an internet connection.

## Data source and limitations

VehicleLens uses [Indian Vehicle Registration Data (2020–25)](https://www.kaggle.com/datasets/aatifahmad123/indian-vehicle-registration-data-202025), published by Aatif Ahmad on Kaggle under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The project applies the filtering, grouping and aggregation described above.

The results describe the registration sample. Its original administrative source and extraction date have not been independently verified. Coverage starts in April 2020, December 2025 coverage is unverified, and the sample contains no Telangana records. Keep these coverage limits in mind when comparing years or states.

## License

The [MIT License](LICENSE) applies to the original VehicleLens code. The source dataset remains under CC BY 4.0.
## Data source and license

VehicleLens uses [Indian Vehicle Registration Data (2020–25)](https://www.kaggle.com/datasets/aatifahmad123/indian-vehicle-registration-data-202025), published by Aatif Ahmad on Kaggle under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

VehicleLens filters and groups the records and uses the `vehicleCount` field to calculate summary statistics. The results describe the dataset sample. Its original administrative source has not been independently verified.

The MIT license applies to the original VehicleLens code. The dataset remains under CC BY 4.0.
