Note: We do not have permission to create/update/delete in production database (must go through <s>Dewayne D</s>/Mike E)

## Uncategorized
- Implement a routine or something to remove migrated data from staging
- SCAQMD monitors 88 & 103 have metadata in database, but no associated measurement data
- SiteIDs 24 & 25 have the same lat/long and site name but different external siteIDs
- Develop data dictionary (ISP2B) 

## Stored Procedures
- Calculate site start date from minimum monitor start date


## Views
- Update view used to create the download data so that external monitorIDs are published (right now internal monitorIDs are published in downloadable files)


## Database Table Modifications


## New Database Tables
- Adjustment Technique 
  - Internal Code/ID, External Code, Equation, Description, Public Description (Equation could be JSON or could be stored within the Description field)



