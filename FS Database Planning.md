## Wishlist

- add DataProviderId, SiteId, MonitorId, StreamId to metadata tables 
  - add data provider id to monitor table
- have batchfilelog indicate how many subhourly/hourly/non-continuous/etc. records are successfully processed instead of how many records are successfully processed (non-specific)
- have batchfilerecordlog indicate which type of data was in the record (if successfully processed)
- have data tables indicate date/time that the record was added to the table ? (logging modifications mentioned above also sufficient)


## New procedures/fixes
- need way of dealing with Adjustments that aren't adjustments (e.g., SJV sending AObs as raw value and AObsAdj as truncated values/negatives to zero)
- need to find a way to manage external quality flags (data provider flags)
- how to deal with AObs in AObsAdj where AObsAdj is just a truncation of AObs or AObsAdj sets negative value to zero
