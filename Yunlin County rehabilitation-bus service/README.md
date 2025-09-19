### `requests.csv`
- Each row corresponds to a single request.  
- Fields include:  
  - Origin and destination coordinates  
  - Estimated O/D travel time (minutes)  
  - Time window lower bound (minutes / HH:MM)  
  - Request type (`a`, `b`, `c`)  
  - Number of accompanying passengers  

---

### `travel_time_matrix_minutes.csv`
- N × N shortest travel time matrix (minutes) for all O/D nodes.  
- Diagonal entries and unreachable pairs are marked as `999`.  

---

### `incompat_matrix.csv`
- N × N incompatibility matrix.  
- Values:  
  - `1` = compatible  
  - `0` = incompatible  
- Generated based on request types (`a/b/c`) and the specified `--incomp-ratio`.  

---

### `map_data.json` / `viz.json`
- Elements for visualization on an interactive map.  
- Includes:  
  - Map center  
  - Node labels  
  - Sampled route coordinates  

---

### `meta.json`
- Metadata summarizing the run.  
- Contains:  
  - Actual incompatibility ratio  
  - Sampling details  
  - GIS/statistical information  

