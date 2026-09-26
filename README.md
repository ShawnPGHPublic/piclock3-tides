# PiClock3 tides

Widget plugin: a smooth 24-hour NOAA tide curve with high/low times in the footer.

Data: `https://api.tidesandcurrents.noaa.gov/api/prod/datagetter`  
No API key.

<img width="433" height="321" alt="image" src="https://github.com/user-attachments/assets/c250f7fb-7ebe-4b42-a632-fe15e8de335d" />


## Install

cd ~/PiClock3
git clone https://github.com/ShawnPGHPublic/piclock3-tides plugins/Tides    

## What you see

Most of the box: today’s predicted water level (6-minute NOAA series,cubic-smoothed), filled under the curve.
Dashed gold line: now.
Dots: published high and low tides.
Footer: station name and the next highs/lows with clock time and height.

units: feet or meters.  Heights use datum MLLW unless you change datum.

---

### Use it

If station is empty, the plugin picks the nearest tide predictions station
to location.latitude / location.longitude.

1. Point a widget at `plugin: plugins.tides` and a `region` (the example uses `bottom`).
2. Set `location` to the coast you care about, or set `station` to a [NOAA station id](https://tidesandcurrents.noaa.gov/stations.html?type=Tide+Predictions).

The example location is Daytona Beach; NOAA should resolve a nearby prediction station automatically. For a known gauge, set station (for example Daytona-area ids around 8720218 / 8720211 — confirm on the NOAA station map for the exact gauge you want).




