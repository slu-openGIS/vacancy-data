# STL_BARRIERS_All

### Metadata
  * **Title -** St. Louis Barrier Locations, April 2017
  * **Date of Original Publication -** 06 Apr 2018
  * **Date of Last Update -** 07 Apr 2018
  * **Edition -** v0.1.1
  * **Abstract -** Point locations for all known current and historic street closures in `.csv`, `.shp`, and `.geoJSON` formats.
  * **Maintenance Frequency -** Frequent
  * **Keywords -** Missouri, St. Louis, Street Closures, Barriers, Urban Planning
  * **Constraints Use -** Open Data Commons Attribution License (ODC-By) v1.0
  * **Constraints Text -** see `LICENSE`
  * **Spatial Representation Type -** Vector - Point
  * **Coordinate System -**
    * `.csv` - NAD 1983
    * `.geoJSON` - WGS 1984
    * `.shp` - NAD 1983
  * **Language -** English
  * **Topic Category -** Street Closures
  * **Source:** Created by the *Streets Not Thru* [project team](https://chris-prener.github.io/barriers/team/)
  * **Modifications:** see `location-data/NEWS.md`
  * **Point of Contact -** Christopher Prener, Ph.D. ([chris.prener@slu.edu](mailto:chris.prener@slu.edu))
  * **Author/Owner -** Christopher Prener, Ph.D. ([chris.prener@slu.edu](mailto:chris.prener@slu.edu))
  * **Link -** [https://github.com/chris-prener/barriers-data](https://github.com/chris-prener/barriers-data)

### Variable Definitions
  * `BarrierID` - identification number assigned to individual barriers
  * `Status` - is an intersection `closed`, `open`, or is that `unknown`?
  * `LastUpdate` - date of last update to record
  * `Type` - is the closure of the intersection `complete` or `partial`?
  * `BarrierCk` - date when was the barrier's location and status was last confirmed
  * `CheckType` - method for the last confirmation of the barrier's location and status
  * `BarrierCk2` - date information for supplemental confirmation
  * `CheckType2` - method for supplemental confirmation
  * `Descrip` - human readable description of the closure
  * `long` - `.csv` *only* - longitude of barrier location
  * `lat` - `.csv` *only* - latitude of barrier location
