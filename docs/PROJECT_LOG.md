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