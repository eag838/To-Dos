# Conventions for AQview Data Handling etc.
Add your notes on any specific/special ways we handle things. </br>
This version applies to the Interim Solution.</br>
Last Updated 3/12/2021
</br>

## Uncategorized
- 


## Pushing Patches
- Troubleshoot getting metadata and measurement data into database in DEV
- Create script to push changes to UAT
- Troubleshoot script to push changes in UAT
- Contact OIS (PU, SL) to push changes to Production

## Adding Measurement Data 
- Do weekly at a minimum
- Only necessary on Production; don't need to do DEV/UAT (the databases aren't all the same size or same specs)
- Run Clarity data pull script
- Run usp_processMeasurementData procedure in database (if not automated), must be run after Clarity script to capture Clarity data

## Adding Metadata
- Only necessary on Production; don't need to do DEV/UAT (the databases aren't all the same size or same specs)
- When adding metadata, add to existing workbook, not a new one. This keeps our record current in case we need to readd all metadata from the workbook.
- Migration Fail Diagnosis View:
  - AdjCodeIdFound? = 99999 if not needed
  - AdjCodeIdFound? = NULL if found in measurement data but no metadata in database

## Rounding & Truncation
- For now, truncate at 4 decimal places (<= 4 decimal places)
- In future, work with data providers to determine appropriate number decimal places and implement precision by monitor & model (maybe in man-model table)


## Data Provider Quality Flags vs AQview QC flags
- If data provider sends quality flags, do not show AQview flags in download files and instead indicate "quality supplied by provider" 
- For now, only showing data provider flags when they are "invalid"
- For now, indicating "record invalidated by data provider"


## Duration/Frequency in database vs reality
  <table class="tg">
  <thead>
    <tr>
      <th class="tg-0pky">Instrument</th>
      <th class="tg-0pky">DB</th>
      <th class="tg-0pky">Actual</th>
      <th class="tg-0pky">Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="tg-0pky">Clarity</td>
      <td class="tg-0pky"></td>
      <td class="tg-0pky">D: 2 min<br>F: 15 min</td>
      <td class="tg-0pky">Powers off for 15 mins then samples for 2 mins<br>Does this apply to TVOC?</td>
    </tr>
    <tr>
      <td class="tg-0pky">Dylos (CCV)</td>
      <td class="tg-0pky"></td>
      <td class="tg-0pky">D: 2 sec (?)<br>F: 5 min</td>
      <td class="tg-0pky"></td>
    </tr>
    <tr>
      <td class="tg-0pky"></td>
      <td class="tg-0pky"></td>
      <td class="tg-0pky"></td>
      <td class="tg-0pky"></td>
    </tr>
  </tbody>
  </table>
