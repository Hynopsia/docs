---
title: Scoring and XP
description: Learn how FlyHub scores flights, applies penalties, awards XP, and ranks pilots in online and offline tracking modes.
---

# Scoring and XP

FlyHub uses scoring to measure how safely and realistically a flight was completed.

There are two separate results:

- **Flight score** is the performance score for the flight, shown out of 10.
- **XP** is the experience earned from the flight, based on distance, final score, and any XP modifiers.

Online flights are scored from simulator telemetry. Offline flights are scored from your check-ins, debrief, trust, plausibility, and punctuality.

## Online and offline scoring

| Tracking mode | How it is scored | XP behavior |
| :--- | :--- | :--- |
| Online tracking | FlyHub reads simulator telemetry during the flight. It can score the landing, runway use, OFP weight and fuel compliance, speed restrictions, taxi speed, lights, gear, altimeter, approach stability, bounces, crashes, and telemetry events. | Full XP is available unless penalties, crash detection, SimRate, or other modifiers reduce it. |
| Manual and Offline Mode | You complete the flight through required check-ins and a final debrief. FlyHub scores the flight from your inputs, route plausibility, timing, and trust. | Offline XP is reduced because FlyHub cannot verify full telemetry. Punctuality and trust can improve the offline multiplier. |

## What the flight score means

FlyHub starts with the landing and then adjusts the score for the rest of the flight.

The score shown in the logbook is the **final score**, not only the raw touchdown score.

The final score can include:

- Original landing score.
- Runway alignment and touchdown-zone analysis.
- Operational penalties.
- Approach and landing penalties.
- Crash or cheating detection.
- Difficult-condition compensation when the flight was harder than normal.

The final score is capped to the normal 0 to 10 range. A severe crash or cheating detection can force the score to 0.

## XP formula

FlyHub calculates base XP from distance and final score:

```text
XP = (Distance NM x 0.5) + (Final Score x 50)
```

Example:

```text
1000 NM flight with a 9.5 final score

(1000 x 0.5) + (9.5 x 50) = 975 XP
```

This means long flights matter, but a clean flight still matters. A long flight with a poor final score earns less than the same route flown well.

## XP modifiers

XP can be changed after the base XP is calculated.

| Modifier | What it does |
| :--- | :--- |
| Online flight with no XP penalties | Uses the full base XP. |
| Offline flight | Applies an offline multiplier based on trust, plausibility, debrief quality, and punctuality. |
| SimRate or time compression | Reduces XP when the flight is completed much faster than the planned airborne time. |
| VATSIM or IVAO network bonus | Adds a +10% XP bonus when FlyHub can verify that at least 80% of the flight was flown online on the matching network account. |
| Crash | Awards 0 XP for the flight. |
| Cheating detection | Can force the score and XP to 0. |

## Landing score

For online flights, FlyHub primarily evaluates landing impact through **touchdown G-force**.

Vertical speed is still shown in the flight report, but G-force is the better measure of what the aircraft actually experienced at touchdown. A touchdown can look low in feet per minute but still hit hard because of aircraft attitude, bounce, sink rate changes, runway slope, or gear compression.

| Touchdown result | General G-force range | Meaning |
| :--- | :--- | :--- |
| Great touchdown | Up to about 1.4 G | Controlled touchdown with low impact. |
| Good touchdown | About 1.4 G to 1.8 G | Normal landing impact. |
| Firm touchdown | About 1.8 G to 2.2 G | Acceptable but clearly firm. |
| Hard touchdown | Above about 2.2 G | Strong impact and larger score deductions. |

FlyHub also checks whether the touchdown was usable and safe. A soft touchdown is not automatically perfect if it causes a long float, poor runway placement, runway overrun risk, or weak directional control.

## The "Butter" Myth

In real-world aviation, searching for the smoothest possible touchdown is not always good technique. A controlled positive touchdown is often safer, especially on wet, short, contaminated, or windy runways.

1. **Sensor delay**
   A very soft touchdown may delay weight-on-wheels detection. That can delay spoiler deployment and reverse thrust, increasing the risk of a runway overrun.

2. **Stopping distance**
   Floating to chase a smooth touchdown can waste thousands of feet of runway that should be used for braking.

3. **Surface grip**
   On wet runways, a positive touchdown helps the tires break through water and gain grip. A very soft touchdown can increase hydroplaning risk.

4. **Crosswinds**
   A positive touchdown helps plant the aircraft on the runway so the tires can provide directional control.

FlyHub rewards controlled, safe landings. It does not reward floating forever just to make the touchdown feel soft.

## Runway scoring

FlyHub reviews runway behavior during takeoff and landing when telemetry has enough data.

### Landing runway checks

FlyHub can score:

- Whether you landed on or near the correct runway surface.
- Whether the aircraft was aligned with the runway centerline.
- Whether the touchdown was inside a reasonable touchdown zone.
- Whether the landing was short, long, or beyond the safe touchdown area.
- Whether the aircraft left the runway edges during landing rollout.
- Whether the aircraft overran the runway.
- Whether difficult conditions, such as crosswind, affected the landing.

Landing on the centerline and touching down in a reasonable zone helps protect the score. Touching down far down the runway, landing off-center, leaving the pavement, or overrunning the runway can create penalties even if the touchdown G-force was low.

### Takeoff runway checks

FlyHub can also review the takeoff roll.

It can detect:

- Takeoff alignment with the runway.
- Whether the aircraft was too far from the centerline.
- Whether the aircraft lifted off outside the runway surface.
- Whether the aircraft left the runway during takeoff.
- Takeoff overrun behavior.
- Difficult conditions during the takeoff roll.

These checks are meant to catch unsafe runway use, not punish normal small corrections.

## Operational compliance scoring

Online tracked flights can also be checked against operational limits and procedures.

Some operational checks use only simulator telemetry. Other checks need a SimBrief OFP because FlyHub must know the planned limits, fuel, or scheduled time for that flight.

Operational compliance can affect the final flight score. The flight report shows the penalty name, the amount deducted, and the telemetry values FlyHub used for the decision.

### When OFP data is required

FlyHub can only apply OFP-based penalties when the needed SimBrief data is present and FlyHub can read the units safely.

The OFP can be in kilograms or pounds. FlyHub converts the OFP values to match the simulator telemetry before comparing them.

If FlyHub is missing a required OFP field, the OFP units are unclear, or the telemetry sample is not available, FlyHub skips that specific penalty instead of guessing.

OFP-based checks include:

- Maximum zero-fuel weight.
- Maximum takeoff weight.
- Maximum landing weight.
- Takeoff fuel mismatch.
- Insufficient fuel reserves.
- Career departure punctuality.

Telemetry-only checks include:

- Taxi speed.

### Maximum zero-fuel weight

Maximum zero-fuel weight checks whether the aircraft's zero-fuel weight exceeded the maximum allowed by the SimBrief OFP.

FlyHub checks this during the flight when online telemetry is available.

The check uses:

- The OFP maximum ZFW limit.
- The aircraft zero-fuel weight reported by telemetry.
- If direct zero-fuel weight is not available, FlyHub may derive it from total weight minus fuel weight when those values are available.

The flight report can show:

- The telemetry maximum ZFW observed.
- The OFP ZFW limit.
- How far over the limit the aircraft was.
- When the maximum sample was seen.
- When the exceedance was first detected.

Small rounding differences are ignored. FlyHub uses a tolerance before applying the penalty.

### Maximum takeoff weight

Maximum takeoff weight checks whether the aircraft was too heavy for takeoff according to the SimBrief OFP.

FlyHub checks this before takeoff and during the takeoff phase. It does not keep re-scoring takeoff weight later in cruise.

When SimBrief provides a structural maximum takeoff weight, FlyHub uses the structural value. If a structural value is not available, FlyHub uses the regular OFP maximum takeoff weight.

The flight report can show:

- The maximum takeoff weight FlyHub observed.
- The OFP maximum takeoff weight used for comparison.
- The amount above the limit.
- The UTC time of the maximum sampled value.
- The UTC time when the exceedance first triggered.

### Maximum landing weight

Maximum landing weight checks whether the aircraft was too heavy at landing.

FlyHub only samples landing weight after there is touchdown or taxi-in evidence. It does not apply a maximum landing weight penalty just because the aircraft is heavy while still airborne on final approach.

Landing weight can be sampled when:

- The flight has already taken off.
- The aircraft has landed, is on the ground, or is in taxi-in.
- Total aircraft weight telemetry is available.

When SimBrief provides a structural landing-weight or maximum landing-weight value, FlyHub uses that first. If no structural value is available, FlyHub uses the regular OFP maximum landing weight.

The flight report can show:

- The maximum landing weight FlyHub observed after landing evidence.
- The OFP maximum landing weight used for comparison.
- The amount above the limit.
- The UTC time of the maximum sampled value.
- The UTC time when the exceedance first triggered.

### Takeoff fuel mismatch

Takeoff fuel mismatch checks whether the aircraft took off with less fuel than planned by the OFP.

FlyHub captures takeoff fuel at the first takeoff, climb, or airborne evidence.

The check uses the aircraft fuel weight reported by telemetry and compares it against the best OFP takeoff-fuel value available.

FlyHub looks for the OFP value in this order:

1. Minimum takeoff fuel.
2. Planned takeoff fuel.
3. Planned ramp fuel minus taxi fuel.

The penalty is for under-fueling. FlyHub does not penalize a pilot for taking more fuel than the minimum/planned takeoff fuel.

The flight report can show:

- Actual fuel at takeoff.
- Required takeoff fuel from the OFP.
- The OFP source used for the requirement.
- The fuel shortfall.
- The UTC time when takeoff fuel was captured.

Small rounding and unit differences are ignored before a penalty is applied.

### Insufficient fuel reserves

Insufficient fuel reserves checks whether the flight landed with enough reserve fuel remaining.

FlyHub captures landing fuel only after the aircraft has landed, is on the ground, or is in taxi-in. It uses the simulator fuel weight telemetry.

The check compares landing fuel against the stricter available reserve requirement:

- At least 90% of the OFP final reserve fuel.
- At least 25 minutes of fuel, when the OFP reserve time is available.

If the OFP final reserve is available but reserve time is not available, FlyHub can still check the 90% final-reserve requirement. If the needed reserve data is missing, this penalty is skipped.

Example:

```text
OFP final reserve: 1003 kg
90% reserve requirement: 903 kg
Landing fuel: 700 kg

Result: insufficient fuel reserves
```

Insufficient fuel reserves is treated as a major fuel-management issue. When it applies, it deducts 2.00 points from the flight score.

The flight report can show:

- Landing fuel.
- Required landing fuel.
- OFP final reserve fuel.
- Estimated reserve minutes remaining.
- The reserve requirement that was not met.

### Taxi speed

FlyHub checks taxi speed during taxi out and taxi in.

The check uses ground speed while the aircraft is on the ground.

The violation starts when:

- The aircraft is in taxi out or taxi in.
- The aircraft is on the ground.
- Ground speed is above 32 knots.

The violation clears when:

- The aircraft leaves taxi out or taxi in.
- The aircraft is no longer on the ground.
- Ground speed drops to 28 knots or below.

The scored taxi limit is 30 knots. The 32-knot start threshold and 28-knot stop threshold are used as hysteresis to avoid false triggers from brief speed fluctuations.

FlyHub requires at least 5 seconds above the trigger threshold before the taxi-speed penalty can register.

The flight report can show:

- Maximum ground speed observed during the taxi violation.
- Taxi-out violation time.
- Taxi-in violation time.
- Chargeable violation time after the grace period.
- The UTC time when the violation first started.

### Career departure punctuality

Career Mode flights can be scored for departure punctuality.

FlyHub compares the planned SimBrief OUT time against the actual departure detected by FlyHub.

This check always uses real UTC time. It does not use the simulator clock, because pilots may intentionally fly with a different simulator time of day.

The planned time comes from the SimBrief OFP scheduled OUT time when available. If that is unavailable, FlyHub can use the OFP estimated OUT time.

Actual departure is captured when FlyHub detects the flight leaving the gate or beginning departure movement, such as pushback, taxi out, takeoff, climb, or ground movement with engines running.

Late departures are scored progressively at 0.05 points for every full minute late.

Early departures have a 15-minute grace window. If you leave more than 15 minutes before the OFP OUT time, FlyHub scores only the minutes beyond that 15-minute early allowance at 0.05 points per minute.

The departure punctuality penalty is capped at 2.50 points.

Example:

```text
Planned OUT: 1930Z
Actual departure: 1931Z
Deviation: 1 minute
Penalty: 0.05 points
```

```text
Planned OUT: 1930Z
Actual departure: 1914Z
Early departure: 16 minutes
Scored minutes: 1 minute
Penalty: 0.05 points
```

The flight report can show:

- Planned OUT time in UTC.
- Actual departure time in UTC.
- Whether the departure was early or late.
- Total minutes off schedule.
- Scored minutes after any early-departure grace.
- Penalty per minute.
- Maximum departure punctuality penalty.

This penalty is Career Mode only. It does not apply to regular Free Flight tracking.

### Operational event markers

Operational penalties can create event markers on the logbook map.

Markers are designed to show the first point where a penalty registered. They are not created repeatedly every telemetry sample.

FlyHub can create these operational marker types:

| Marker | When it appears |
| :--- | :--- |
| Weight exceedance | First confirmed ZFW, takeoff-weight, or landing-weight exceedance. |
| Takeoff fuel | First confirmed takeoff fuel shortfall. |
| Taxi speed | First confirmed taxi-speed violation after the grace period. |
| Fuel reserve | Landing or taxi-in point where insufficient reserves are confirmed. |
| Departure time | Career departure point where planned OUT and actual departure differ enough to create a penalty. |

For weight penalties, the marker shows when the exceedance first registered. The final flight report can show the maximum telemetry value that was actually scored. These can be different if the aircraft became even heavier after the first trigger.

Each operational marker type is emitted only once per applicable rule for a flight. For example, a flight can have one maximum ZFW marker, one maximum takeoff-weight marker, and one maximum landing-weight marker, but it will not create a new marker every second while overweight.

## Lights scoring

FlyHub checks common aircraft light procedures during online tracking.

| Light | Expected behavior |
| :--- | :--- |
| Beacon | Should be on while engines are running and during pushback. |
| Strobe | Should be on while airborne and during runway operations. |
| Navigation lights | Should be on during aircraft operations. |

If a required light is off for a monitored period, FlyHub records the violation duration and applies a penalty. Longer violations are usually worse than brief mistakes.

## Gear scoring

Gear procedure is scored during online flights when gear data is available.

FlyHub can penalize:

- Retracting the landing gear too late after liftoff.
- Flying with the gear extended above safe limits when gear overspeed is detected.
- Landing with the gear up.

Gear penalties are shown in the flight report when FlyHub detects the issue.

## Altimeter scoring

FlyHub checks the altimeter during online tracking to confirm that the aircraft is using a reasonable pressure setting.

The check is normally made around:

- Takeoff.
- Final touchdown.

FlyHub compares the aircraft altimeter setting against the best available ambient pressure source. That can include simulator weather and VATSIM METAR data when available.

The normal tolerance is about **2 hPa**, or about **0.059 inHg**.

If the altimeter is outside tolerance during the monitored window, FlyHub can apply an altimeter penalty. The flight report can show the set pressure, the expected pressure, the source used, and the deviation.

## Stable approach scoring

FlyHub monitors the final approach, especially below about 1000 feet AGL.

Unstable approach penalties can be triggered by sustained problems such as:

- Excessive vertical speed.
- Excessive bank.
- Excessive pitch.
- Speed deviation.
- Repeated or severe instability close to landing.

A single small correction should not be treated the same as a sustained unstable approach. FlyHub looks for meaningful instability over the monitored part of the approach.

## Bounce scoring

FlyHub can detect landing bounces when telemetry shows the aircraft touching down, becoming airborne again, and touching down again.

Bounce penalties depend on how many bounces were detected and how severe the landing sequence was. A bounce can reduce the final score even if the first touchdown looked acceptable.

## Crash detection

Crash detection can force the flight score and XP to 0.

FlyHub can treat a flight as a crash when the landing or flight data shows severe unsafe behavior, such as:

- Extremely hard impact.
- Extreme descent rate at touchdown.
- Severe aircraft attitude at touchdown.
- Crash signals from the simulator.
- Other telemetry that indicates the aircraft did not complete a safe flight.

If a crash is detected, the flight report will show the crash result instead of treating the flight as a normal low-score landing.

## Cheating and invalid telemetry

FlyHub can detect telemetry that is not physically plausible.

Examples include:

- Slew behavior.
- Teleporting.
- Large position jumps that cannot be flown normally.
- Telemetry manipulation that makes the route impossible.

Cheating detection can force the score to 0 and remove XP for the flight.

## Difficult conditions compensation

Some flights are harder than others. FlyHub can account for difficult conditions when scoring runway and landing behavior.

Examples include:

- Strong crosswind.
- Windshear-like conditions.
- Difficult runway alignment situations.
- Challenging takeoff or landing conditions.

This does not erase unsafe flying. It helps avoid over-penalizing a flight when the conditions made normal handling harder.

## Online tracking score review

After an online flight, open the flight entry from your logbook to review the score.

You can review:

- Final score.
- Original landing score.
- XP earned.
- Touchdown G-force.
- Touchdown vertical speed.
- Penalties and bonuses.
- Takeoff and landing runway analysis.
- Event markers.
- Telemetry graphs.
- Recorded flight path.

See [Your Profile and Logbook](/profile-logbook) for how to open a flight entry.

## Offline scoring

Manual and Offline Mode is for console pilots, simulator setups without telemetry, or users who choose not to track live simulator data.

Offline flights are not scored like online telemetry flights because FlyHub cannot directly verify the full flight path, aircraft state, lights, gear, altimeter, G-force, or runway alignment.

Instead, offline scoring uses:

- Required check-ins during the flight.
- Required route checkpoints when the flight type includes them.
- Final debrief inputs.
- Landing quality selected by the user.
- Reported issues such as unstable approach or other problems.
- Flight time and route plausibility.
- Punctuality.
- Trust score.

### Offline check-ins matter

Offline flights are not just entered at the end.

You are expected to progress through the flight in FlyHub and complete the required check-ins as you fly. Depending on the flight, this can include:

- Preflight.
- Pushback or departure preparation.
- Takeoff.
- Enroute checkpoints.
- Landing.
- Parked or completed.

Missing check-ins, unrealistic timing, or skipping the expected flow can reduce trust and XP.

### Offline debrief

At the end of an offline flight, FlyHub asks for the debrief information it needs to score the flight.

This can include:

- Actual flight time.
- Landing quality.
- Operational issues.
- Any supporting information requested by the flight flow.

The debrief should match what actually happened. Entering a perfect debrief for every flight will not automatically protect the score if timing, checkpoints, or route plausibility do not make sense.

### Offline XP multiplier

Offline flights use a reduced XP multiplier for fairness.

The multiplier is affected by:

- Your offline trust score.
- Whether the check-ins were completed properly.
- Whether the flight time is plausible.
- Whether the route progress makes sense.
- Punctuality.
- Debrief quality.

Higher-trust offline flights can earn more XP than low-trust offline flights, but offline XP is still capped below a fully verified online flight.

See [Manual and Offline Mode](/manual-mode) for the step-by-step offline tracking guide.

## SimRate and time compression

FlyHub can reduce XP when a flight is completed much faster than expected.

For online flights with enough plan data, FlyHub compares:

- Planned airborne time.
- Actual airborne time.

If the actual airborne time is too short, FlyHub treats the flight as time-compressed and reduces XP. The larger the time compression, the larger the reduction.

This check is meant to keep XP fair between pilots who fly the route normally and pilots who speed through it.

## Network bonus

FlyHub can award a +10% XP bonus for verified VATSIM or IVAO flights.

To receive the bonus:

- Add your VATSIM CID or IVAO VID in Settings.
- Fly online on that network.
- Make sure FlyHub can match your network account to the flight.
- Stay connected for at least 80% of the flight.

If the network ID is missing, wrong, or not online for enough of the flight, the bonus may not apply.

## Ranks

XP increases your Free Flight pilot rank.

| Rank | XP needed |
| :--- | :--- |
| Cadet | 0 |
| Junior First Officer | 2,500 |
| First Officer | 7,500 |
| Senior First Officer | 17,500 |
| Junior Captain | 35,000 |
| Captain | 65,000 |
| Senior Captain | 115,000 |
| Training Captain | 190,000 |
| Chief Pilot | 300,000 |
| Fleet Captain | 475,000 |
| Legend | 750,000+ |

Ranks are shown on your profile and may also affect badges, profile display, and community status.

## Common scoring mistakes

These are the most common reasons a flight scores lower than expected:

- Landing softly but too far down the runway.
- Floating to chase a smooth touchdown.
- Touching down off-center.
- Leaving the runway during rollout.
- Forgetting beacon, strobe, or navigation lights.
- Leaving the gear down too long after takeoff.
- Departing with aircraft weight above the OFP limits.
- Taking off with less fuel than the OFP required.
- Landing below the OFP reserve fuel requirement.
- Taxiing too fast during taxi out or taxi in.
- Departing early or late in Career Mode.
- Flying an unstable approach below 1000 feet AGL.
- Bouncing the landing.
- Setting the wrong altimeter.
- Using SimRate or completing the route unrealistically fast.
- Missing offline check-ins.
- Entering offline debrief data that does not match the route or timing.

The best way to improve your score is to fly the full procedure cleanly: plan the flight, use the correct tracking mode, fly stable, manage the aircraft systems, land in the touchdown zone, stay on the runway, and review the flight report afterward.
