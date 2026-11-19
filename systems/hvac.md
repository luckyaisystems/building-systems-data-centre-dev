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

# Assignment 7 — Psychrometrics (Questions 2–4)

## Question 2 — Room RH and comfort range (2 marks)
A room is 25 m × 15 m × 5 m. If there is 20 kg of moisture in the air and
the temperature is 21°C, what is the RH? Is the room within the "comfort
range" for most people?

### Given
- Room dimensions: 25 m × 15 m × 5 m
- Room volume: 1,875 m³
- Moisture in air: 20 kg
- Air temperature: 21°C

### Solution
- Moisture concentration = 20 kg / 1,875 m³ = 0.01067 kg/m³
- pv = ρv × Rv × T = 0.01067 × 461.5 × 294.15 = 1,448 Pa
- RH = pv / Ps × 100 = 1,448 / 2,481 × 100 = 58.4%

### Answer
At 21°C, the RH is 58% (Ps at 21°C = 2,481 Pa), which is within the
"comfort range" for most people.

## Question 3 — Moisture in 1,000 kg of air, wet bulb, and RH adjustment (2 marks)
If the temperature of an air container is 21°C and the RH is 75%, how much
moisture is there in 1,000 kg of air? What is the wet bulb temperature?
How much must the temperature be adjusted to achieve an RH of 45%?

### Given
- Air temperature: 21°C
- Relative humidity: 75%
- Mass of air: 1,000 kg
- Atmospheric pressure: 101,325 Pa

### Solution
- pv = RH × Ps = 0.75 × 2,481 = 1,861 Pa
- W = 0.62198 × pv / (P − pv) = 0.62198 × 1,861 / (101,325 − 1,861)
  = 0.01164 kg water / kg dry air
- Moisture in 1,000 kg of air = 1,000 × 0.01164 = 11.6 kg
- Wet-bulb temperature (psychrometric chart): 18°C
- Temperature needed for 45% RH: moisture content is unchanged, so pv
  stays at 1,861 Pa. Ps = pv / 0.45 = 1,861 / 0.45 = 4,136 Pa

### Interpolation between table rows
4,136 Pa falls between two table rows:
- 29°C → 3,997 Pa
- 30°C → 4,234 Pa

1. Total gap between rows: 4,234 − 3,997 = 237 Pa
2. Distance past 29°C: 4,136 − 3,997 = 139 Pa
3. Fraction of the way across: 139 / 237 ≈ 0.59
4. Temperature: 29 + 0.59 ≈ 29.6°C

### Answer
- Moisture in 1,000 kg of air: **11.6 kg**
- Wet-bulb temperature: **18°C**
- Temperature for 45% RH: **29.6°C** (interpolated)
- Temperature adjustment: 29.6 − 21 = **+8.6°C increase**

## Question 4 — Wet bulb and moisture removal (2 marks)
If the temperature of a room is 20°C and the current RH is 65%, what is
the wet bulb temperature? How much moisture must be removed from the air
to lower the RH to 50%?

### Given
- Air temperature: 20°C
- Current RH: 65%
- Target RH: 50%
- Atmospheric pressure: 101,325 Pa
- Ps at 20°C = 2,339 Pa

### Solution
- Current moisture content: pv = RH × Ps = 0.65 × 2,339 = 1,520 Pa
- W = 0.62198 × 1,520 / (101,325 − 1,520) = 0.00947 kg water / kg dry air
- Target moisture content at 50% RH (temperature unchanged):
  pv new = 0.50 × 2,339 = 1,169 Pa
- W new = 0.62198 × 1,169 / (101,325 − 1,169) = 0.00719 kg water / kg dry air
- Moisture to remove = 0.00947 − 0.00719 = 0.00228 kg water per kg of dry air

### Answer
- Wet-bulb temperature (psychrometric chart): **16°C**
- Moisture to remove: **0.00228 kg water per kg of dry air** (about 2.3 g
  per kg of dry air)
