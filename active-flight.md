# Active Flight

Your cockpit companion when flying. FlyHub tracks your flight in real time on PC, or lets you log it manually on console or offline.

---

## Overview

The Active Flight page appears when you’ve started a flight and are flying it. You see route info, telemetry (if connected), and controls to finish or cancel the flight. It works in both the desktop app and the web.

For a full explanation of tracking choices, see [Tracking Methods](/tracking-methods), [Online Tracking](/online-tracking), and [Manual and Offline Mode](/manual-mode).

---

## PC Telemetry Tracking

### Microsoft Flight Simulator (2020 & 2024)

- FlyHub connects automatically via **SimConnect**.  
- No plugin needed.  
- Start your sim, spawn at the departure airport, then start the flight in FlyHub.  

### X-Plane 12

- Requires the **FlyHub plugin**.  
- Install it from **Settings → X-Plane Plugin**: select your X-Plane folder, then Install Plugin.  
- **Restart X-Plane** after installation.  

---

## What FlyHub Detects (At a User Level)

When telemetry is connected, FlyHub tracks:

- **Phases:** Preflight → Taxi → Takeoff → Climb → Cruise → Descent → Approach → Landing → Taxi-in  
- **Events:** Gear up/down, flaps, lights, touchdown  
- **Position, altitude, speed, G-force** at touchdown for scoring  

You don’t need to do anything special — fly normally and FlyHub records it.

---

## Console / Manual (Offline) Mode

If you fly on Xbox or PlayStation, or prefer not to use telemetry:

1. Choose **Offline** when starting the flight (or set it as your default in Settings).  
2. The Active Flight page opens the offline mission tracker.  
3. Click **Start Flight** and enter the actual UTC time you began preflight.  
4. Record each required check-in as the flight progresses:
   - Pushback
   - Takeoff
   - Required route checkpoints
   - Landing
   - Parked
5. Record optional OFP fixes if you want extra detail.
6. After Parked is recorded, open the debrief and enter the final flight result, landing quality, and any issues.

Offline flights are logged and scored from your check-ins and debrief. Offline XP is based on trust, plausibility, punctuality, and reported issues.

---

## How to Start a Flight

1. Go to **My Flights**.  
2. Select your next or active booking.  
3. Click **Start Flight**.  
4. Choose **Online** (PC with telemetry) or **Offline** (console/manual).  
5. You’re taken to the Active Flight page.  
6. **Online:** Ensure your sim is running and you’re at the departure airport.  
7. Fly normally — FlyHub tracks everything in the background.  

---

## How to Properly Finish a Flight

### Online (Telemetry)

1. Land and taxi to the gate.  
2. Shut down engines (or follow your in-sim flow).  
3. The app will prompt you to **Close Flight** — in the overlay (if enabled) or on the Active Flight page.  
4. Click **Close Flight** and confirm.  
5. FlyHub computes your score, saves the log, and updates your XP.  

### Offline (Manual)

1. Use the offline mission tracker during the flight.  
2. Record pushback, takeoff, required checkpoints, landing, and parked.  
3. After the Parked check-in is saved, click **Open Debrief**.  
4. Enter the landing quality and any issues.  
5. Review the offline XP multiplier and plausibility warnings if shown.  
6. Submit the debrief. The flight is then logged with the offline XP multiplier shown in the form.  

---

## Flight Recovery After CTD

If your simulator crashes or closes mid-flight:

1. **Reopen FlyHub** as soon as you can.  
2. On the **Dashboard** or **My Flights**, look for the **Recover Flight** button (amber).  
3. Click it to open the recovery flow.  
4. FlyHub restores your last known position (location, altitude, fuel, etc.).  
5. **Match your sim:** Load the same aircraft, set fuel (ZFW) and payload to match what FlyHub shows.  
6. Spawn at the restored position (or as close as possible).  
7. Continue the flight and finish normally.  

**When recovery appears:** Only when FlyHub had telemetry and saved a snapshot.  
**Expiry:** Recovery snapshots expire after **6 hours**. After that, start the flight again.

For the full step-by-step recovery process, see [Recovery Wizard](/recovery-wizard).

---

## Overlay (Desktop App)

When enabled in Settings (desktop app only):

- A small overlay appears **inside the simulator window**.  
- It shows landing feedback (e.g. G-force, rating) and the **Close Flight** prompt when you’ve landed.  
- You can finish the flight without leaving the sim.  

---

## Quick Tips

- Keep FlyHub and your sim running together; don’t close FlyHub mid-flight.  
- In Offline Mode, keep the Active Flight page available so you can record required check-ins.  
- For X-Plane, install the plugin and restart the sim before your first flight.  
- After a crash, return to FlyHub quickly so recovery is still available.  
- Use the overlay (desktop) to close the flight without alt-tabbing.  

---

## Common Mistakes

- **Forgetting to start the flight** — You must click Start Flight in My Flights; telemetry won’t record otherwise.  
- **Closing the sim before Close Flight** — Always close the flight in FlyHub first so it’s scored and saved.  
- **Skipping offline check-ins** — Offline Mode requires mission check-ins before the final debrief.  
- **X-Plane not connecting** — Check that the plugin is installed and X-Plane was restarted.  
- **Recovery expired** — If it’s been more than 6 hours since the crash, recovery won’t be available.  
