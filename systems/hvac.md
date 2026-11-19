# HVAC
## Saturation Pressure (Ps) Table (0°C to 40°C)

| Dry-Bulb Temp (T) | Saturation Pressure (Ps) in Pa | Saturation Pressure (Ps) in kPa |
|-------------------|--------------------------------|---------------------------------|
| 0°C               | 611                            | 0.611                           |
| 1°C               | 657                            | 0.657                           |
| 2°C               | 706                            | 0.706                           |
| 3°C               | 758                            | 0.758                           |
| 4°C               | 813                            | 0.813                           |
| 5°C               | 872                            | 0.872                           |
| 6°C               | 934                            | 0.934                           |
| 7°C               | 1,001                          | 1.001                           |
| 8°C               | 1,071                          | 1.071                           |
| 9°C               | 1,146                          | 1.146                           |
| 10°C              | 1,226                          | 1.226                           |
| 11°C              | 1,310                          | 1.310                           |
| 12°C              | 1,400                          | 1.400                           |
| 13°C              | 1,495                          | 1.495                           |
| 14°C              | 1,595                          | 1.595                           |
| 15°C              | 1,702                          | 1.702                           |
| 16°C              | 1,814                          | 1.814                           |
| 17°C              | 1,933                          | 1.933                           |
| 18°C              | 2,059                          | 2.059                           |
| 19°C              | 2,192                          | 2.192                           |
| 20°C              | 2,333                          | 2.333                           |
| 21°C              | 2,481                          | 2.481                           |
| 22°C              | 2,637                          | 2.637                           |
| 23°C              | 2,803                          | 2.803                           |
| 24°C              | 2,977                          | 2.977                           |
| 25°C              | 3,160                          | 3.160                           |
| 26°C              | 3,353                          | 3.353                           |
| 27°C              | 3,557                          | 3.557                           |
| 28°C              | 3,771                          | 3.771                           |
| 29°C              | 3,997                          | 3.997                           |
| 30°C              | 4,234                          | 4.234                           |
| 31°C              | 4,483                          | 4.483                           |
| 32°C              | 4,745                          | 4.745                           |
| 33°C              | 5,020                          | 5.020                           |
| 34°C              | 5,309                          | 5.309                           |
| 35°C              | 5,613                          | 5.613                           |
| 36°C              | 5,931                          | 5.931                           |
| 37°C              | 6,265                          | 6.265                           |
| 38°C              | 6,616                          | 6.616                           |
| 39°C              | 6,983                          | 6.983                           |
| 40°C              | 7,367                          | 7.367                           |

# Worked Example: Using the Saturation Pressure Table

## Question
If the temperature of an air container is 21°C and the RH is 75%, how much
moisture is there in 1,000 kg of air? What is the wet bulb temperature?
How much must the temperature be adjusted to achieve an RH of 45%?

## Given
- Air temperature: 21°C
- Relative humidity: 75%
- Mass of air: 1,000 kg
- Atmospheric pressure: 101.325 kPa = 101,325 Pa

## Step 1 — Look up Ps at 21°C in the table
From the table row for 21°C:  Ps = 2,481 Pa

## Step 2 — Find the vapour partial pressure
pv = RH × Ps = 0.75 × 2,481 = 1,861 Pa

## Step 3 — Find the humidity ratio
W = 0.62198 × pv / (P − pv)
W = 0.62198 × 1,861 / (101,325 − 1,861)
W = 0.01164 kg water / kg dry air

## Step 4 — Moisture in 1,000 kg of air
mw = 1,000 × 0.01164 = 11.6 kg

## Step 5 — Wet-bulb temperature (from psychrometric chart)
At 21°C dry bulb / 75% RH, the chart gives  Twb ≈ 15.5°C

## Step 6 — Temperature needed for 45% RH
Moisture content is unchanged, so pv stays at 1,861 Pa.
For 45% RH:  Ps = pv / 0.45 = 1,861 / 0.45 = 4,136 Pa

### Using the table: interpolation between rows
4,136 Pa falls between two table rows:
- 29°C → 3,997 Pa
- 30°C → 4,234 Pa

1. Total gap between rows:      4,234 − 3,997 = 237 Pa
2. Distance past 29°C:          4,136 − 3,997 = 139 Pa
3. Fraction of the way across:  139 / 237 ≈ 0.59
4. Temperature:                 29 + 0.59 ≈ 29.6°C

## Final Answers
- Moisture in 1,000 kg of air: **11.6 kg**
- Wet-bulb temperature: **15.5°C**
- Temperature for 45% RH: **29.6°C** (interpolated)
- Temperature adjustment: 29.6 − 21 = **+8.6°C increase**

> Note: If rounding to the nearest whole table row instead of interpolating,
> 30°C gives an adjustment of 30 − 21 = 9°C.
