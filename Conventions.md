# Conventions for AQview Data Handling etc.
Add your notes on any specific/special ways we handle things. 

## Uncategorized


## Rounding & Truncation
- For now, truncate at 4 decimal places (<= 4 decimal places) - 20210310
- In future, work with data providers to determine appropriate number decimal places and implement precision by monitor & model (maybe in man-model table)


## Data Provider Quality Flags vs AQview QC flags
- If data provider sends quality flags, do not show AQview flags in download files and instead indicate "quality supplied by provider" 
- For now, only showing data provider flags when they are "invalid" - 20210310
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
