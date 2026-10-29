# OpenPointStitcher regression scans

Two full-resolution iPhone scans of neighbouring rooms, and the reference pair for
OpenPointStitcher's `tests/test_regression_real.py`. The fixture holding their hand-confirmed
alignment lives in the main repository (`tests/fixtures/ampbar_confirmed.json`).

| file | points | sha256 |
|---|---|---|
| `Point Cloud AMP Room.pts` | 766,744 | `d7954df9b2e2271333a50d5723d23a74cbe55153c6ba53f9a654ea47b39a6141` |
| `UPSTAIRS SMALL BAR.pts` | 194,562 | `1e7b7838c277326e863fa172c321a8399ad573050f3f58b8b84e2495ab0886bd` |

## Use

Clone this repository as `scans-regression` inside your OpenPointStitcher checkout. The folder is
already in the main repository's `.gitignore`, and the launchers mount it for QA:

```
cd OpenPointStitcher
git clone https://github.com/TeganLovesUnicorns/OpenPointStitcher-regression-scans.git scans-regression
.\stitch.ps1 qa-slow
```

Or point `SCANS_REGRESSION` at a clone somewhere else.

The files must stay exactly as they are. Never thin, re-export or re-save them: the test checks the
point counts and the alignment depends on every point.
