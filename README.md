# Mastery 500 Calculator

Calculate the XP, cycles, and time required to reach Mastery 500.

## XP Milestones

XP requirements are cumulative. Known game observations are preserved exactly.
Intermediate thresholds are estimated using monotonic PCHIP cubic interpolation.
Level 500 is anchored at exactly 1.3 billion XP.

| Mastery | XP Bonus | Cumulative XP Required |
|---------|----------|------------------------|
| 50 | +5% | 1,379,662 |
| 100 | +10% | 10,714,990 |
| 150 | +15% | 35,803,973 |
| 200 | +20% | 84,449,239 |
| 250 | +25% | 164,448,778 |
| 300 | +30% | 283,607,536 |
| 350 | +35% | 449,723,502 |
| 400 | +40% | 670,585,392 |
| 450 | +45% | 954,053,802 |
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
- Mastery XP per cycle: `3796.2`
- Cycle duration: `3.48s`

Open `mastery-calculator.html` in a browser and adjust the inputs to recompute
totals. Intermediate values use PCHIP interpolation between the verified
observations above.
