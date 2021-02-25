Note: We do not have permission to create/update/delete in production database (must go through <s>Dewayne D</s>/Mike E/Michael G/Peter U/Satia A)


## Uncategorized (needs updated)
- SCAQMD monitors 88 & 103 have metadata in database, but no associated measurement data
- SiteIDs 24 & 25 have the same lat/long and site name but different external siteIDs
  - Delete Site 25 (mistake by SDAPCD)
- Update metadata (UDL, LDL, UOM, etc.) in StreamSegment for SDAPCD StreamSegmentId=77
- Develop data dictionary (ISP2B?) 


## Stored Procedures
- Calculate site start date from minimum monitor start date


## Views
- Add dynamic QA/QC definitions (hard coded right now)


## Database Table Modifications
- Add AQS and ADAM site code fields to site table(s)


## New Database Tables
- Add Parameter type to parameter table 


## Completed
- Implement a routine or something to remove migrated data from staging
- Adjustment Technique 
  - Internal Code/ID, External Code, Equation, Description, Public Description (Equation could be JSON or could be stored within the Description field)
- Update view used to create the download data so that external monitorIDs are published (right now internal monitorIDs are published in downloadable files)
