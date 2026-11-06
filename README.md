# Mastery 500 Calculator

Calculate the XP, cycles, and time required to reach Mastery 500.

## XP Milestones

XP requirements are cumulative and follow cubic scaling:

    XP(LV) = round(10.4 * LV^3)

The result is rounded to an integer. Level 500 requires exactly 1.3 billion XP.

| Mastery | XP Bonus | Cumulative XP Required |
|---------|----------|------------------------|
| 50 | +5% | 1,300,000 |
| 100 | +10% | 10,400,000 |
| 150 | +15% | 35,100,000 |
| 200 | +20% | 83,200,000 |
| 250 | +25% | 162,500,000 |
| 300 | +30% | 280,800,000 |
| 350 | +35% | 445,900,000 |
| 400 | +40% | 665,600,000 |
| 450 | +45% | 947,700,000 |
| 500 | +50% | 1,300,000,000 |

## Usage

- **Current Mastery Level** — starting level (1–500). Cumulative XP for that
  level is the starting point; milestones already reached are skipped.
- **Mastery XP per cycle** — base XP earned per cycle before milestone bonuses.
- **Cycle duration** — seconds per cycle.
- Each milestone unlocks its bonus XP only after the milestone is reached; the
  bonus applies while earning toward the next milestone.
- Total cycles = sum of cycles needed per segment; total time = cycles ×
  duration.

## Config

The calculator's defaults are:
- Current Mastery Level: `1`
- Mastery XP per cycle: `1200`
- Cycle duration: `1s`

Open `mastery-calculator.html` in a browser and adjust the inputs to recompute
totals. XP thresholds are computed with the cubic formula above.
