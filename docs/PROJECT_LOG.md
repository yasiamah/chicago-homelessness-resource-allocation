# Project Log

## September 20, 2026

### Objective

Verify the Git repository, Python environment, Jupyter kernel, and GitHub connection.

### Completed

- [ ] Verified the Git repository root
- [ ] Confirmed that the README conflict was resolved
- [ ] Confirmed that `.venv-2` is ignored
- [ ] Activated `.venv-2`
- [ ] Installed the required packages
- [ ] Connected the notebook to the correct kernel
- [ ] Ran the package verification cell
- [ ] Published the completed setup to GitHub

### Files Changed

- `.gitignore`
- `requirements.txt`
- `notebooks/00_project_setup.ipynb`
- `docs/PROJECT_LOG.md`
- `README.md` if conflict resolution was needed

### What I Learned

I learned the difference between a Python virtual environment and a Jupyter kernel. The environment stores the project’s packages. The kernel is the Python process that runs notebook cells.

### Blockers

List any unresolved errors here. Write `None` if everything works.

### Git Commit

`Complete repository and notebook setup`

### Next Step

Create a verified data-source inventory for the Chicago homelessness analysis.





## September 21, 2026

### Objective

Create and validate a structured inventory of the project’s official and supplementary data sources.

### Completed

- [ ] Created the data-source notebook
- [ ] Documented seven verified sources
- [ ] Checked for missing values
- [ ] Checked for duplicate source names
- [ ] Validated the source URLs
- [ ] Exported the inventory to CSV
- [ ] Created the data-source documentation

### Files Changed

- `notebooks/01_data_source_inventory.ipynb`
- `data/processed/data_source_inventory.csv`
- `docs/DATA_SOURCES.md`
- `docs/PROJECT_LOG.md`

### What I Learned

I learned that a data-source inventory records what each dataset measures, its time period, its geographic level, its planned use, and its limitations. This prevents incompatible datasets from being treated as if they measure the same thing.

### Blockers

Write `None` if all validation checks passed.

### Git Commit

`Document verified homelessness data sources`

### Next Step

Download and inspect the Chicago affordable housing and community-area boundary datasets.





## September 22, 2026

### Final Verification

- [x] Selected the `.venv-2` Jupyter kernel
- [x] Ran all notebook cells
- [x] Verified seven data sources
- [x] Confirmed zero missing values
- [x] Confirmed zero duplicate source names
- [x] Exported and reopened the CSV
- [x] Created the data-source documentation

### Result

All data-source inventory validation checks passed. The exported CSV contains seven rows and nine columns.

### Blockers

None.

### Next Step

Download and inspect Chicago’s Affordable Rental Housing Developments dataset.




## September 23, 2026

### Objective

Verify the data-source inventory and begin reproducible collection of Chicago's Affordable Rental Housing Developments dataset.

### Completed

- [ ] Verified all four Day 2 deliverables
- [ ] Ran every inventory notebook cell successfully
- [ ] Confirmed the inventory contains seven rows and nine columns
- [ ] Closed GitHub Issue #2
- [ ] Created the affordable-housing download notebook
- [ ] Downloaded the official dataset through the API
- [ ] Inspected columns, data types, missing values, and duplicates
- [ ] Saved the raw local data
- [ ] Exported the column profile

### Files Changed

- `notebooks/02_affordable_housing_download.ipynb`
- `data/processed/affordable_housing_profile.csv`
- `docs/PROJECT_LOG.md`

### What I Learned

I learned how an API makes data collection reproducible. I also learned that an affordable-housing development inventory measures documented supply, not real-time vacancies or access.

### Blockers

Write `None` if all checks passed. Otherwise record the exact error and the step where it occurred.

### Git Commit

`Download and profile affordable housing data`

### Next Step

Clean the affordable-housing fields and determine whether community-area and unit-count columns are suitable for geographic analysis.





## September 24, 2026

### Objective

Verify that the data-source inventory and affordable-housing ingestion pipeline run successfully and produce the required outputs.

### Completed

- [ ] Ran the data-source inventory notebook successfully
- [ ] Confirmed the inventory CSV contains seven rows and nine columns
- [ ] Ran the affordable-housing notebook successfully
- [ ] Confirmed the API returned HTTP status 200
- [ ] Verified that the raw data and profile files exist
- [ ] Confirmed that the raw dataset is ignored by Git
- [ ] Reopened and validated the saved profile CSV
- [ ] Closed GitHub Issue #2
- [ ] Published the verified checkpoint to GitHub

### Files Changed

- `notebooks/01_data_source_inventory.ipynb`
- `notebooks/02_affordable_housing_download.ipynb`
- `data/processed/data_source_inventory.csv`
- `data/processed/affordable_housing_profile.csv`
- `docs/DATA_SOURCES.md`
- `docs/PROJECT_LOG.md`

### Result

The source inventory contains 7 rows and 9 columns.

The affordable-housing dataset contains ___ rows and ___ columns. The duplicate-row check found ___ exact duplicates.

### What I Learned

I learned how to verify a reproducible data pipeline by checking the API response, confirming output files exist, reopening saved data, and validating the expected columns.

### Blockers

Write `None` if every verification check passed. Otherwise record the exact error and the notebook cell where it occurred.

### Git Commit

`Verify housing data ingestion pipeline`

### Next Step

Clean and standardize the affordable-housing dataset after the current checkpoint is published.






## September 25, 2026

### Objective

Resolve the notebook execution-order error and verify the affordable-housing ingestion pipeline from beginning to end.

### Completed

- [ ] Restarted the Jupyter kernel
- [ ] Ran every notebook cell in order
- [ ] Confirmed HTTP status 200
- [ ] Confirmed the dataset contained 598 rows and 19 columns
- [ ] Confirmed zero exact duplicate rows
- [ ] Saved the raw dataset locally
- [ ] Saved the processed data profile
- [ ] Verified that both output files are nonempty
- [ ] Confirmed that the raw dataset is ignored by Git
- [ ] Closed GitHub Issue #2
- [ ] Published the completed checkpoint

### Files Changed

- `notebooks/02_affordable_housing_download.ipynb`
- `data/processed/affordable_housing_profile.csv`
- `docs/PROJECT_LOG.md`

### Results

The City API returned 598 affordable-housing development records with 19 columns. The duplicate check found zero exact duplicate rows. The `units` column contained one missing value and the `location` column contained nine missing values.

These results describe the dataset as downloaded on September 25, 2026. They may change when the City updates the source.

### What I Learned

I learned that Jupyter variables exist only in the active kernel session. Restarting the kernel removes those variables, so a reproducible notebook must run successfully from the first cell to the last cell.

### Blockers

Write `None` only after the full notebook and final verification cell pass.

### Git Commit

`Verify affordable housing ingestion pipeline`

### Next Step

Clean the affordable-housing data types, handle the missing units value, and remove unneeded system-generated columns.







## September 26, 2026

### Objective

Verify that the affordable-housing ingestion notebook runs successfully from a fresh kernel and produces reproducible outputs.

### Completed

- [ ] Selected the `.venv-2` notebook kernel
- [ ] Restarted the kernel
- [ ] Ran every notebook cell in order
- [ ] Received HTTP status 200
- [ ] Confirmed the dataset was not empty
- [ ] Verified the raw and profile files
- [ ] Confirmed that Git ignores the raw dataset
- [ ] Published the reproducible files to GitHub

### Results

- Dataset rows: `[ACTUAL ROW COUNT]`
- Dataset columns: `[ACTUAL COLUMN COUNT]`
- Exact duplicate rows: `[ACTUAL DUPLICATE COUNT]`
- Final verification message: `[ACTUAL MESSAGE]`

### Files Changed

- `notebooks/02_affordable_housing_download.ipynb`
- `data/processed/affordable_housing_profile.csv`
- `docs/PROJECT_LOG.md`

### What I Learned

I learned that Jupyter variables exist only in the current kernel session. Restarting the kernel and running all cells in order tests whether a notebook is genuinely reproducible rather than dependent on hidden execution history.

### Blockers

Write `None` only if Run All completed without an error. Otherwise record the exact error and the cell where it occurred.

### Git Commit

`Verify affordable housing ingestion pipeline`

### Next Step

Create `notebooks/03_affordable_housing_cleaning.ipynb` and clean the unit-count, community-area, property-type, and coordinate fields.






## September 28, 2026

### Objective

Clean and validate the Chicago Affordable Rental Housing Developments dataset for later geographic analysis.

### Completed

- [x] Verified the ingestion notebook from a fresh kernel
- [x] Created the cleaning notebook
- [x] Selected the analytical columns
- [x] Standardized text fields
- [x] Converted numeric fields
- [x] Preserved and flagged the missing units value
- [x] Validated community-area numbers
- [x] Screened latitude and longitude values
- [x] Checked missing values and duplicates
- [x] Saved and reopened the cleaned dataset
- [x] Published the completed work to GitHub

### Files Changed

- `notebooks/03_affordable_housing_cleaning.ipynb`
- `data/processed/affordable_housing_cleaned.csv`
- `docs/PROJECT_LOG.md`
- `notebooks/02_affordable_housing_download.ipynb` if its outputs changed

### What I Learned

I learned how to select relevant columns, standardize text, convert data types and validate geographic values. I also learned that a missing unit count should not automatically be changed to zero because missing and zero have different meanings.

### Blockers

Write `None` if every validation check passed. Otherwise record the exact failed check.

### Git Commit

`Clean and validate affordable housing data`

### Next Step

Summarize affordable developments and documented units by community area and property type.



## September 30, 2026

### Objective

Summarize documented affordable housing developments and known unit counts by community area and property type.

### Completed

- [x] Loaded the cleaned affordable housing data
- [x] Created the community area summary
- [x] Created the property type summary
- [x] Calculated unit reporting rates
- [x] Validated that no development records were lost
- [x] Created the top 15 community area chart
- [x] Saved and reopened both summary files
- [x] Documented an initial finding
- [x] Published the work to GitHub

### Results

- Community area groups: `[RUN len(community_summary)]`
- Property type groups: `30`
- Highest known documented unit total: `Grand Boulevard with 2,406 known units across 30 development records`
- Records with missing unit counts: `1`

### Files Changed

- `notebooks/04_affordable_housing_summary.ipynb`
- `data/processed/affordable_housing_by_community_area.csv`
- `data/processed/affordable_housing_by_property_type.csv`
- `reports/figures/top_community_areas_affordable_units.png`
- `docs/PROJECT_LOG.md`

### What I Learned

I learned how to use Pandas groupby and aggregation to create community level indicators. I also learned that known documented unit totals are different from vacancies or the actual availability of affordable housing.

### Blockers

None

### Git Commit

`Summarize affordable housing distribution`

### Next Step

Download Chicago community area boundaries and prepare the affordable housing summary for geographic mapping.








## October 1, 2026

### Objective

Finish the affordable housing summary and check its totals. This checkpoint was completed during the October 21 review.

### Completed

- [x] Ran every cleaning and summary code cell in order in fresh Python sessions
- [x] Fixed category spelling errors and documented 10 reviewed area label corrections
- [x] Calculated the total known units and each area's percentage
- [x] Ranked the listed community areas
- [x] Confirmed that percentages total 100%
- [x] Confirmed that no records or known units were lost
- [x] Saved both summary files and checked their contents after reopening
- [x] Updated the top 15 chart
- [x] Finished the initial finding
- [x] Published this completed checkpoint with its supporting files

### Results

- Development records: 598
- Records with missing unit counts: 1
- Total known documented units: 29,550
- Listed community area groups: 66
- Property type groups: 28
- Highest listed unit total: Grand Boulevard
- Grand Boulevard known units: 2,406 across 30 records
- Grand Boulevard share: 8.14%
- Humboldt Park known units after merging the spelling error: 1,139
- Near South Side known units after merging the spacing error: 1,473

### Validation and Category Review

The cleaning changes were checked using the original selected fields from the committed 598-row snapshot. A new City housing download was not substituted for that snapshot. Both notebooks passed ordered execution in fresh Python processes. The reopened CSV contents matched the calculated summaries. Record counts, known unit counts, missing unit counts and total units reconciled in both summaries.

Notebook 03 now normalizes whitespace and merges the clear property type misspellings `Mutifamily` and `Multfamily` into `Multifamily`. Distinct housing programs remain separate.

Ten conflicting or misspelled area labels were reviewed against the listed coordinates and the City's official community area boundary dataset, https://data.cityofchicago.org/d/igwz-8jzy, accessed October 21, 2026. The changes are recorded in `docs/HOUSING_CATEGORY_CORRECTIONS.csv`. These corrections use the recorded location and do not independently verify the street address or every location in a scattered-site development.

Seven other records have a coordinate disagreement even though their listed area names and numbers agree. Their listed areas were kept. They are recorded in `docs/GEOGRAPHY_REVIEW_FLAGS.csv` for the later geography review. The area totals are preliminary until that review is complete.

### Files Changed

- `notebooks/03_affordable_housing_cleaning.ipynb`
- `notebooks/04_affordable_housing_summary.ipynb`
- `data/processed/affordable_housing_cleaned.csv`
- `data/processed/affordable_housing_by_community_area.csv`
- `data/processed/affordable_housing_by_property_type.csv`
- `reports/figures/top_community_areas_affordable_units.png`
- `docs/HOUSING_CATEGORY_CORRECTIONS.csv`
- `docs/GEOGRAPHY_REVIEW_FLAGS.csv`
- `docs/PROJECT_LOG.md`

### What I Learned

I learned that the totals can add up even when area names have spelling errors. Those errors can split one area into separate groups and change the rankings. I also learned why a missing unit count should stay missing.

### Remaining Limitation

The seven geography flags still need review. These counts do not show vacancies or whether the housing meets local need.

### Git Commit

`Finish Notebook 04 summary and category cleanup`

### Next Step

Download and validate Chicago's official community-area boundary data for geographic mapping.