# comparison

### Metadata
  * **Title -** Crosswalk of Urban Prairie data with STL Vacancy data
  * **Date of Original Publication -** 15 September 2018
  * **Date of Last Update -** 15 September 2018
  * **Edition -** v0.1.0
  * **Abstract -** Data containing the `HANDLE` identification numbers for parcels we determined to contain either vacant lots or vacant buildings as well as an indicator identifying City-owned properties. These data are for the less conservative "high" estimate.
  * **Maintenance Frequency -** Infrequent
  * **Keywords -** Missouri, St. Louis, Street Closures, Barriers, Urban Planning
  * **Constraints Use -** Open Data Commons Attribution License (ODC-By) v1.0
  * **Constraints Text -** see `LICENSE`
  * **Spatial Representation Type -** Vector - Polygon
  * **Coordinate System -** NA
  * **Language -** English
  * **Topic Category -** Vacancy
  * **Source:** Created by the *Urban Prairies* [project team](https://chris-prener.github.io/vacancy/team/)
  * **Modifications:** see `data-2017/comparison/NEWS.md`
  * **Point of Contact -** Christopher Prener, Ph.D. ([chris.prener@slu.edu](mailto:chris.prener@slu.edu))
  * **Author/Owner -** Christopher Prener, Ph.D. ([chris.prener@slu.edu](mailto:chris.prener@slu.edu))
  * **Link -** [https://github.com/chris-prener/vacancy-data](https://github.com/chris-prener/vacancy-data)

### Notes
These data are based on a join of the original data from Prener et al. (*forthcoming*) - the "prairie data" - and the `finalvacantall_20180707.csv` data - the "stl vacancy data". The join was based on the `HANDLE`. Addresses were not compared to validate the join and the join resulted in some duplicate rows.

Four spreadsheets have been created:

1. `vacancy_compared.csv` - the entire joined data set (`n = 49,377` parcels)
2. `vacancy_overlap.csv` - all overlapping parcels (`n = 25,598` parcels)
3. `vacancy_prairieOnly.csv` - parcels that only appear in the prairie data (`n = 23,095` parcels)
4. `vacancy_stlvacOnly.csv` - parcels that only appear in the stl vacancy data (`n = 684` parcels)

All four spreadsheets share the same variables, though not all appear in all sheets.

## Variable Definitions
Bracketed references indicate which of the four spreadsheets listed above contain each variable.

* `HANDLE` - parcel identification number [1-4]
* `p_address` - address from prairie data [1-3]
* `c_address` - address from city data [1-2, 4]
* `p_lcra` - prairie indicator that is `TRUE` if property is owned by LCRA; `FALSE` otherwise [1-3]
* `p_lra` - prairie indicator that is `TRUE` if property is owned by LRA; `FALSE` otherwise [1-3]
* `p_landBank` - prairie indicator that is `TRUE` if property is owned by LCRA or LRA; `FALSE` otherwise [1-3]
* `c_lra` - stl vacancy indicator that is `TRUE` if property is owned by LRA; `FALSE` otherwise [1-2,4]
* `p_typeSimple` - best estimate of property type based on prairie data [1-3]
* `c_typeDetail` - city indicator of representing property type [1-2,4]
* `c_typeSimple` - simplified version of `c_typeDetail` [1-2,4]
* `compare_data` - what data set is the parcel included in? [1]
    - `"city only"` - parcel is included in only the city data
    - `"overlapping"` - parcel is included in both the city and the prairie data
    - `"prairie only"` - parcel is included in only the prairie data
* `compare_type` - does the simplified property type (`"lot"` or `"building"`) in the city data match the prairie data? [1,2]
    - `"matched"` - the property type is the same in the city and prairie data
    - `"unmatched"` - the property type is not the same in the city and the prairie data
* `p_low` - were data included the low estimate from the prairie paper? [1-3]