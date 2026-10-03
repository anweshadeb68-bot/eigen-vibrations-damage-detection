# Eigen-vibrations: structural damage detection with linear algebra

Mini project for UE25MA242A. Learns what healthy vibration looks like on a steel
structure (30 sensors) and flags vibration that healthy patterns cannot explain.

## Files
- `damage_detection.ipynb` – the full project, step by step (run this for the demo)
- `damage_detection.html` – the same notebook with all results, opens in any browser (backup)
- `figures/` – charts for the slides
- `zzzAU.TXT`, `zzzBU.TXT`, `zzzBD3.TXT`, `zzzBD13.TXT`, `zzzBD26.TXT` – data

## How to run (Mac)
1. Open Terminal and go to this folder:
   `cd ~/Documents/"Math mini project"`
2. Install once:
   `python3 -m pip install -r requirements.txt`
3. Start the notebook:
   `python3 -m notebook damage_detection.ipynb`
4. In the browser: **Kernel → Restart & Run All**. Takes about 20 seconds.

## Results
| Recording | % of seconds flagged (avg over 30 sensors) | Verdict |
|---|---|---|
| Healthy, unseen run (BU) | 0.4% | HEALTHY |
| Damage at joint 3 | 99.9% | DAMAGED |
| Damage at joint 13 | 99.9% | DAMAGED |
| Damage at joint 26 | 99.1% | DAMAGED |

Locating the damaged joint is indicative only (highest-scoring joint matched for joints 3 and 26, not 13).

## Data source
Avci, O., Abdeljaber, O., Kiranyaz, S., Hussein, M., Gabbouj, M., Inman, D. (2022).
A New Benchmark Problem for Structural Damage Detection: Bolt Loosening Tests on a
Large-Scale Laboratory Structure. Dynamics of Civil Structures, Vol. 2, Springer.
https://onur-avci.com/benchmark/
