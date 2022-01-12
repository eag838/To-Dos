# Toxics Notes


## Calculations
### Annual Average (MOMM)
The means shown in ARB's toxics pages are actually means of monthly means. Using the mean of monthly means compensates for the uneven distribution of samples over the 12 months of the year.  
Means of monthly means are calculated by first determining the average of all measurements taken within a month at each site. Site means are then calculated by finding the average of the 12 monthly means for each site. Statewide means are calculated by first taking the average of all the monthly site means for each month within the state, and then calculating the average of those 12 monthly means.  
  
1. Change measurements that are 0 or between 0.48 and 0.52 * MDL to -1 * MDL
2. For each month, if obs is negative, use -0.5 * obs, else use obs (this effectively turns -MDL from step 1 above into 1/2 MDL)
3. The annual avg is straight avg of monthly means (mean of monthly means, MOMM)
  
  
Comments based on experience with the original MS Access toxics database:  
The way values below the MDL get handled depend on the lab's specific protocols/policies. At least this was probably true back in older datasets. There are several common ways these <MDL values are handled:
- Set the value to -MDL
- Set the value to 1/2MDL
- Set the value to 0
  
The 0.48-0.52 range in step 1 of calculating MOMM was included in the original toxics database to give some leeway for data type conversion errors if any data values submitted as 0.5 * MDL (because MS Access tends to tack on trailing 9s). We might be able to ignore that part when we calculate the monthly means.
  
  
  
  
  
## Health Messaging

### OEHHA health values:
- REL (Reference Exposure Level)
  - Roughly like the "yellow" AQI category (REAMAR notes from RB 20120508)
  - It is not likely to see health effects at or below the REL with normal individuals (OEHHA reps meeting 20200508)
  - 8-hour REL is a misnomer; not based on time exposure but average breathing rate of workers, 8-hour REL will almost always be 2x chronic; convenience for HARP (OEHHA reps meeting recording 20200508)
- Hazard index
  - Note: some communities could always have HI > 1 because background may stay above level of concern over sustained period of time (REAMAR notes from RB 20120508)
- AEGL
  - Designed for very brief exposure; evacuation level (REAMAR notes from RB 20120508)
- TEEL 
  - Dev by toxicologist at DOE thorough toxicology review – not all are based on AEGLs but some are; slightly more rigorous and updated more often than AEGL (REAMAR notes from RB 20120508)
  - Designed for very brief exposure; evacuation level (REAMAR notes from RB 20120508)
- CSF (Cancer Slope Factor)



### Snippets from meeting notes:
- Application of OEHHA Health Values: (REAMAR notes from RB 20120508)
  - Avoid putting in cancer risk values for meas values unless they’re similar year round 
  - Display RT data and hourly averages rolling compared to acute RELs
  - On monthly basis, update the mean concentrations since monitoring started for comparison to chronic RELs
  - Calculate rolling monthly mean as new data come in for comparison with chronic REL 

- Black Carbon:
  - Consider treating like PM2.5 since BC is a fraction of PM2.5; weight to toxicity levels (OEHHA health metrics and AQview meeting 20201210)


- VOCs:
  - Use a risk assessment approach? Think about some sort of trigger or threshold(?) (OEHHA health metrics and AQview meeting 20201210)













