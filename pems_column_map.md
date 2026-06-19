# PeMS Station 5-Minute File — Column Map

Columns used from the PeMS d07_text_station_5min files (0-indexed):

| Column | Field | Notes |
|--------|-------|-------|
| 0  | Timestamp | MM/DD/YYYY HH:MM:SS |
| 1  | Station (VDS) | unique detector station ID |
| 3  | Freeway | e.g. 60 |
| 4  | Direction | N/S/E/W |
| 5  | Lane type | ML = mainline |
| 6  | Segment length | miles |
| 7  | Samples received | data-quality signal (max ~60) |
| 8  | % observed | NOT populated in this version — use col 7 instead |
| 9  | Total flow | vehicles per interval |
| 11 | Average speed | mph |

PeMS version 20.0.1.
