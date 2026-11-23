# Example input files

Example files to import in DSS4NAFA.

- `sampling_grid_example.csv`: sample locations (`lat`, `lng`), sample type and category (such as Food, Wheat), and the person in charge with a contact number.
- `input-examples/crop_calendar_without_aez.csv`: the month of planting (`P`) or harvest (`H`) for each crop. The calendar is the same for every agro-ecological zone (AEZ).
- `input-examples/land_use_for_admin_unit_or_AEZ.csv`: for each administrative unit or AEZ and each crop, the `land_use` and the `farming_land` percentage.
- `input-examples/sample_food_categories.csv`: food groups and the food types in each group.
- `input-examples/sample_test_distribution.csv`: a template for laboratory results, with one row that describes each column (unit or AEZ, food type, land use, soil type, coordinates, analysis date, radionuclide and contamination in Bq/kg).
- `input-examples/exclusion_zone_1_or_more.geojson`: one or more exclusion zones as polygons.
