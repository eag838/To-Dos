Note: We do not have permission to create/update/delete in production database (must go through <s>Dewayne D</s>/Mike E/Michael G/Peter U/Satia A)


## Uncategorized (<> this section needs to be reviewed/updated)
- SCAQMD monitors 88 & 103 have metadata in database, but no associated measurement data
- SiteIDs 24 & 25 have the same lat/long and site name but different external siteIDs
  - Delete Site 25 (mistake by SDAPCD)
- Update metadata (UDL, LDL, UOM, etc.) in StreamSegment for SDAPCD StreamSegmentId=77
- Develop data dictionary (ISP2B?) 

## Data Processing Needs
- Improved logging
- UOM Conversions
- Include all data provider flags (as of 20210409 they are 


## Stored Procedures
- Calculate site start date from minimum monitor start date


## Views
- Add dynamic QA/QC definitions (hard coded right now)


## Database Table Modifications
- Add AQS and ADAM site code fields to site table(s)
- Add Parameter type to parameter table 


## New Database Tables
- Parameter Type table (to support Parameter table updates)


## Logging
- Conversion of 999-like AObs values to NULL


## Completed
- Implement a routine or something to remove migrated data from staging
- Adjustment Technique 
  - Internal Code/ID, External Code, Equation, Description, Public Description (Equation could be JSON or could be stored within the Description field)
- Update view used to create the download data so that external monitorIDs are published (right now internal monitorIDs are published in downloadable files)
