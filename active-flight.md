---
title: "Active Flight"
description: "Use the Active Flight page to prepare, file, track, and manage a booked FlyHub flight."
---

# Active Flight

The Active Flight page is where you manage the flight you are about to fly or are currently tracking.

Use this page to review the route, file your flight plan, connect telemetry, read the OFP, change aircraft before dispatch, take notes, start tracking, and finish or abort the flight.

<Frame>
  ![Active Flight page](/images/Screenshot-2026-05-02-203247.png)
</Frame>

## When to use Active Flight

Open Active Flight after you have a booked flight in My Flights.

You can reach it from:

- My Flights.
- A booked schedule route.
- A historical route booking.
- A manual flight.
- A VIP booking.
- A tour leg.

The page changes depending on the flight type, whether an OFP has been generated, and whether tracking has started.

## Flight header

The top of the page shows the main flight information.

This can include:

- Airline or operator.
- Flight number.
- Departure airport.
- Arrival airport.
- Aircraft type.
- Aircraft registration when available.
- Current tracking actions.

Use this section to confirm you are opening the correct flight before starting.

## Departure and arrival information

The departure and arrival panels show key airport and schedule details.

This can include:

- Departure time in Zulu.
- Arrival time in Zulu.
- Terminal.
- Gate.
- Origin airport.
- Destination airport.

Use these details to set up your simulator flight, pick the correct airport, and prepare the route.

If terminal or gate information is available, FlyHub shows it here so you can start and park in the right place.

**Note: not every flight will have gate/terminal information**

## External flight tools

The Active Flight page includes quick buttons for external flight services.

Depending on the flight, you may see buttons for:

- FlightAware.
- VATSIM.
- IVAO.
- PilotEdge.

### FlightAware

Use FlightAware when you want to check real-world flight information for the route or flight number.

This is useful for comparing timing, route context, or real-world operation details when available.

### VATSIM

Use VATSIM to file or prefill the flight plan for online flying on VATSIM.

Before filing, review the aircraft, route, departure, arrival, callsign, and remarks.

### IVAO

Use IVAO to file or prefill the flight plan for IVAO.

Review the route and aircraft details before submitting.

### PilotEdge

Use PilotEdge if you are flying on PilotEdge and want to file or prepare the flight for that network.

These buttons are shortcuts. Always review the information before submitting anything to an online network.

## Change aircraft

The Active Flight page can let you change the aircraft for the booking before the flight is dispatched.

Use Change Aircraft if:

- You booked a route with multiple valid aircraft options.
- You selected the wrong aircraft.
- You want to fly another compatible aircraft type.
- You need to match the aircraft you actually have loaded in the simulator.

Aircraft changes are only available before certain steps are completed.

Once an OFP has been generated or imported, FlyHub may lock the aircraft because the route planning, weights, fuel, and aircraft-specific data are already tied to that aircraft.

If you need to change aircraft after that point, you may need to refresh or recreate the flight planning data depending on the flight type.

## Telemetry connection

The Telemetry section shows whether FlyHub is connected to your simulator.

For PC tracking, this is where you confirm that FlyHub can read simulator data.

You may see a telemetry provider such as:

- SimConnect for Microsoft Flight Simulator.
- X-Plane plugin telemetry for X-Plane.

The connection state can show whether telemetry is connected or disconnected.

If telemetry is disconnected, use the Connect button.

Before starting online tracking, make sure:

- The simulator is running.
- The correct aircraft is loaded.
- The FlyHub desktop app is open.
- The simulator connection is working.
- The X-Plane plugin is installed if you are using X-Plane.
- SimConnect is available if you are using Microsoft Flight Simulator.

If telemetry is not connected, FlyHub cannot track the flight online.

For a full explanation of tracking choices, see [Tracking Methods](/tracking-methods), [Online Tracking](/online-tracking), and [Manual and Offline Mode](/manual-mode).

## Cabin Announcements

FlyHub Desktop can play automatic cabin announcements during an active flight.

Use the Cabin Announcements panel in the Active Flight sidebar to choose the audio device, select or scan sound packs, manually play announcements, force announcement phases, adjust trigger behavior, and enable GSX integration for MSFS.

For setup, custom pack folder rules, required file names, overlay usage, and every sidebar setting, see [Cabin Announcements](/cabin-announcements).

## Operational Flight Plan

The OFP section shows the route briefing for the flight.

Use the OFP to prepare the flight before departure.

The OFP can include:

- Route summary.
- Fuel planning.
- Routing.
- Flight impacts.
- Times and weights.
- Flight log.
- Wind information.
- Runway analysis.
- Airport weather.
- NOTAM information.
- Company NOTAMs when available.

The OFP is generated from the flight data and selected aircraft.

Review it before starting the flight so you understand the route, fuel, cruise planning, and expected timing.

## Refresh OFP

Use Refresh OFP when you need FlyHub to regenerate the operational flight plan.

This is useful if:

- The OFP is missing.
- The OFP failed to load.
- You changed planning information before the OFP was locked.
- You want to regenerate the dispatch package.

If the aircraft or route is already locked, some changes may no longer be available.

## OFP units

The OFP can use your selected units.

For example, fuel and weight may show in kilograms or pounds depending on your SimBrief/FlyHub unit setting.

You can change your default SimBrief units in Settings.

## OFP outline

The outline on the left lets you jump through OFP sections quickly.

Use it when you only need a specific part of the briefing, such as:

- Summary and fuel.
- Routing.
- Times and weights.
- Flight log.
- Wind information.
- Runway analysis.
- Weather.
- NOTAMs.

This is useful on long OFPs where scrolling through the entire dispatch package would take too long.

## OFP zoom

The zoom controls let you change the OFP text size.

Use this if the OFP is too small or too large for your display.

This is especially useful for users on smaller monitors or high-resolution screens.

## Notepad

<Frame>
  ![Screenshot 2026 05 02 205343](/images/Screenshot-2026-05-02-205343.png)
</Frame>

The Notepad button opens a flight note panel.

Use the notepad to write anything you want to keep during the flight.

Examples:

- ATC clearances.
- Assigned runway.
- SID or STAR changes.
- Cruise altitude.
- Step climbs.
- Fuel notes.
- VATSIM, IVAO, or PilotEdge instructions.
- Personal reminders.
- Approach briefing notes.

The notepad is meant to help you keep quick operational notes without leaving the Active Flight page.

## Start Tracking

Use Start Tracking when you are ready to begin the flight in FlyHub.

Before clicking Start Tracking, check that:

- The correct flight is open.
- The correct aircraft is selected.
- Your simulator is running.
- Telemetry is connected if you are using online tracking.
- The OFP is ready if you plan to use it.
- You are at the correct departure airport.
- You are ready to begin the flight flow.

After tracking starts, FlyHub begins recording the flight according to the selected tracking mode.

For online tracking, FlyHub records simulator telemetry.

For offline/manual tracking, FlyHub follows the manual check-in flow instead.

## During the flight

While the flight is active, FlyHub can track or display flight progress depending on the tracking mode.

For online tracking, FlyHub can record:

- Position.
- Altitude.
- Ground speed.
- Vertical speed.
- Heading.
- Aircraft state.
- Flight phases.
- Takeoff.
- Landing.
- Touchdown data.
- Telemetry events.
- Scoring-related events.

This data is used later for the flight report, logbook entry, scoring, XP, telemetry graphs, and map review.

## Console and Manual Offline Mode

If you fly on Xbox or PlayStation, or prefer not to use telemetry, choose Offline when starting the flight.

Offline flights use the Active Flight page as a manual mission tracker.

During the flight, record the required check-ins as the flight progresses:

- Preflight.
- Pushback or departure preparation.
- Takeoff.
- Required route checkpoints.
- Landing.
- Parked or completed.

After the Parked check-in is saved, open the debrief and enter the final flight result, landing quality, and any issues.

Offline flights are logged and scored from your check-ins and debrief. Offline XP is based on trust, plausibility, punctuality, and reported issues.

## Finish Flight

When the flight is complete, FlyHub saves the result and creates a logbook entry.

For online tracking:

1. Land and taxi in.
2. Finish your normal shutdown or arrival flow.
3. Use the Close Flight or Finish Flight action when FlyHub prompts you.
4. Confirm the completion.
5. FlyHub computes the score, saves the logbook entry, and updates XP.

For offline tracking:

1. Record the required check-ins during the flight.
2. Save the Parked or completed check-in.
3. Open the debrief.
4. Enter landing quality and any issues.
5. Review any offline XP or plausibility warnings shown.
6. Submit the debrief.

After the flight is saved, you can open the flight entry from your logbook to review:

- Score.
- XP.
- Landing data.
- Penalties.
- Telemetry.
- Map path.
- Event markers.
- Flight details.

## Abort Flight

Use Abort Flight only when you need to cancel the active flight.

This is useful if:

- You started the wrong flight.
- You selected the wrong booking.
- You need to stop before departure.
- You no longer want to continue the flight.

Aborting a flight is different from finishing a flight.

Only finish the flight when you actually completed it.

## Flight Recovery After CTD

If your simulator crashes or closes mid-flight:

1. Reopen FlyHub as soon as you can.
2. On the Dashboard or My Flights, look for the Recover Flight button.
3. Click it to open the recovery flow.
4. FlyHub restores the last known flight position and state when a recovery snapshot is available.
5. Load the same aircraft in the simulator.
6. Match the fuel and payload values shown by FlyHub as closely as possible.
7. Spawn at the restored position, or as close as your simulator allows.
8. Continue the flight and finish normally.

Recovery only appears when FlyHub had enough telemetry to save a recovery snapshot.

Recovery snapshots expire after 6 hours.

For the full step-by-step recovery process, see [Recovery Wizard](/recovery-wizard).

## Overlay in the desktop app

When enabled in Settings, the simulator overlay can appear inside the simulator window.

The overlay can show:

- Tracking status.
- Landing feedback.
- Touchdown data.
- Close Flight prompt after arrival.

Use the overlay if you want to finish the flight without leaving the simulator window.

See [Simulator Overlay](/simulator-overlay) for the setup guide.

## Common mistakes

- Starting tracking before the simulator is connected.
- Forgetting to check the selected aircraft.
- Generating an OFP before changing aircraft.
- Filing to VATSIM, IVAO, or PilotEdge without reviewing the prefilled flight plan.
- Ignoring the OFP fuel and route information.
- Forgetting to use the notepad for ATC changes.
- Aborting when you meant to finish.
- Finishing when the flight was not actually completed.
- Closing the simulator before closing the flight in FlyHub.
- Skipping offline check-ins when using Offline Mode.
