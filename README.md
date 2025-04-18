## VATSIM Sweden ACC Sectorization Map Data

### Content of config.json:


1. List of possible ACC logon codes for Sweden:
```
"controllerList": [
  { "name": "ESAA", "color": "#1f77b4" },
  { "name": "ESOS 1", "color": "#e41a1c" },...
],
```

2. VATSIM Sector Ownership Logic in correct order:
```
"sectorsOwnership": {
  "ESOS1": ["ESOS 1", "ESOS 9", "ESOS 3", "ESAA"],
  "ESOS2": ["ESOS 2", "ESOS 7", "ESOS 9", "ESOS 1", "ESOS 3", "ESAA"],...
},
````

3. Presets of the most common sector combinations in Sweden:
```
"presets": [
  { "name": "OS 3 + MM 2", "controllers": ["ESOS 3", "ESMM 2"] },...
],
````

4. Combining sectors with real life sectors defined in another file:
```
"connectGroupWithRealSectors": {
  "ESOS1": ["ESOS 1:1", "ESOS 1:2", "ESOS 1:3"],
  "ESOS2": ["ESOS 2:2", "ESOS 2:3", "ESOS 2:4", "ESOS 2:5", "ESOS 2:1"],...
}
````

- The ``connectGroupWithRealSectors`` data is connected with a geojson file containing sectorization as of 20 MAR 2025.
- In case the real-life sectors have been changed, please contact me to update the geojson file accordingly.
