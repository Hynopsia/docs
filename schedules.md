---
title: "Schedules"
description: "Search current official routes, book flights, generate itineraries, and suggest missing recent routes."
---

<iframe src="https://www.youtube.com/embed/2-IlgTrcdRw" title="YouTube video player" frameborder="0" className="w-full aspect-video rounded-xl" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen />

<iframe src="https://www.youtube.com/embed/JtnQWu_GHqM" title="YouTube video player" frameborder="0" className="w-full aspect-video rounded-xl" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen />

# Schedules

Schedules is the main Free Flight page for current official airline routes.

Use it to search routes manually, generate an itinerary, and submit missing recent schedule routes for review.

This page is for Free Flight Mode. Career Mode has its own dispatch flow.

## Modes

Schedules has two modes:

| Mode | Use it when |
| --- | --- |
| Manual Bid | You want to search specific routes and book one flight at a time. |
| Scheduler | You want FlyHub to generate a multi-leg itinerary from your filters. |

You can switch between Manual Bid and Scheduler from the top of the page.

## Free and premium access

Free users can book routes from:

- The five weekly rotating airlines.
- Their one monthly airline choice.

Premium users can book from all active official FlyHub airlines.

Schedules only uses airlines in the official FlyHub roster. If you want to fly a non-roster airline, use [Manual Flights](/manual-flights) as a premium user.

## Manual Bid overview

<Frame>
  ![Screenshot 2026 05 02 202008](/images/Screenshot-2026-05-02-202008.png)
</Frame>

Manual Bid lets you search the current schedule database.

Use it when you already know what you want to fly, or when you want to browse by airline, aircraft, airport, distance, or flight time.

## Manual Bid filters

### Airline

Use Airline to select one or more carriers.

Free users can only select airlines available through the weekly rotation or monthly choice. Locked airlines may appear unavailable or show a premium prompt.

Premium users can select any active official airline.

### Airline type

You can narrow the airline list by operation type:

- Passenger.
- Cargo.
- Passenger/cargo.

Use this when you want to avoid cargo-only or passenger-only operators.

### Aircraft

Use Aircraft to select the aircraft types you want to fly.

The aircraft list is based on the selected airlines and available schedule fleet data.

If you select no aircraft, FlyHub searches all aircraft types that match your other filters.

### Match aircraft

Match aircraft filters the airline list based on your selected aircraft.

Use it when you want the airline list to show only carriers that operate the aircraft types you selected.

Example: if you select A320 and enable Match aircraft, FlyHub hides airlines that do not have A320 routes in the available schedule data.

### Departure and arrival

Use Departure and Arrival to search by airport.

You can enter:

- A full ICAO code, such as `KJFK`.
- A partial prefix, such as `KJ`, to browse airports that start with that prefix.

Use the swap button to switch departure and arrival.

### Distance range

Distance Range filters routes by nautical miles.

Use it to find:

- Short hops.
- Medium-haul routes.
- Long-haul routes.

### Flight time

Flight Time filters by estimated duration.

Use it when you know how much time you have to fly.

When aircraft filters are selected, FlyHub also checks aircraft-specific flight time estimates when available.

## Manual Bid step-by-step

1. Open Schedules.
2. Choose Manual Bid.
3. Select airlines, aircraft, departure, arrival, distance, or flight time filters.
4. Click Search Routes.
5. Review the route results.
6. Click Book on the route you want.
7. If the route has multiple aircraft types, choose the aircraft you will fly.
8. Confirm the booking.
9. Open My Flights when you are ready to start.

## Route results

Route results can show:

- Airline.
- Flight number.
- Origin.
- Destination.
- Distance.
- Estimated flight time.
- Aircraft options.
- Book action.

If a route has more than one aircraft option, FlyHub asks you to select one before booking.

## Scheduler overview

<Frame>
  ![Screenshot 2026 05 02 202110](/images/Screenshot-2026-05-02-202110.png)
</Frame>

Scheduler generates a multi-leg itinerary from your rules.

Use it when you want FlyHub to build a trip instead of searching one route at a time.

## Scheduler settings

### Number of legs

Choose how many flights you want in the itinerary.

Each generated leg becomes a booking when you save the itinerary.

### Routing type

| Type | What it does |
| --- | --- |
| Random | Builds a set of valid routes from your filters. |
| Continuous | Builds a chain where each leg continues from the previous arrival airport when possible. |
| Roundtrip | Builds hub-based pairs that return to the same hub. |

### Start and end airports

For Continuous routing, you can enter a starting airport and an ending airport.

Use these when you want the itinerary to begin or finish at a specific place.

### Round-trip hub

For Roundtrip routing, enter the hub airport.

Roundtrip itineraries require an even number of legs because each outbound leg needs a return leg.

### Avoid round-trip duplicates

This option avoids duplicate reverse pairs when generating non-roundtrip itineraries.

Example: if FlyHub already used `KJFK -> KBOS`, it tries not to also use `KBOS -> KJFK` in the same itinerary.

### Airline and aircraft

Select airlines and aircraft before generating.

Scheduler needs at least one eligible airline. Aircraft filters narrow the generated routes to matching types.

### Distance and flight time

Distance and Flight Time work like Manual Bid filters, but they apply to every generated leg.

### Airport Rules

<Frame>
  ![Image](/images/image.png)
</Frame>

Airport Rules let you control which airports the generator can use.

You can:

- Include required airports.
- Exclude airports.
- Save presets.
- Load presets later.
- Use scenery preference rules.

Airport Rules and scenery preferences use the same scenery airport list explained in [Scenery Scanner](/scenery-scanner).

Included airports tell FlyHub to try to include those airports in the itinerary.

Excluded airports tell FlyHub not to use those airports.

An airport cannot be both included and excluded.

### Scenery preference

If you use the [Scenery Scanner](/scenery-scanner), Scheduler can use your scanned and manually added scenery airports.

Options include:

- Off: no scenery filtering.
- Prefer: FlyHub prefers airports you have scenery for.
- Only: FlyHub only uses airports found in your scenery list when possible.

You can also choose which scenery sources count, such as MSFS, X-Plane, or manual entries. See [Scenery Scanner](/scenery-scanner) for the setup tutorial.

## Scheduler step-by-step

1. Open Schedules.
2. Choose Scheduler.
3. Select number of legs.
4. Choose Random, Continuous, or Roundtrip.
5. Set start, end, or hub airport if needed.
6. Choose airlines.
7. Choose aircraft types if you want to restrict the fleet.
8. Set distance and flight time ranges.
9. Add airport rules if needed.
10. Choose scenery preferences if needed.
11. Click Generate Itinerary.
12. Review the generated legs on the map and list.
13. Select aircraft for any leg that still needs an aircraft choice.
14. Click Save to My Flights.

## Saving an itinerary

When you save an itinerary, FlyHub adds all generated legs to My Flights.

Each leg becomes an upcoming booking. You can then schedule them on the Calendar or start them from My Flights in order.

## Suggest a route

<Frame>
  ![Screenshot 2026 05 02 202218](/images/Screenshot-2026-05-02-202218.png)
</Frame>

Use Suggest a route only for current official schedule routes.

Submit a Schedules suggestion when:

- The route has operated within the last 2 months.
- The airline is already part of FlyHub's official roster.
- The route is missing from the latest data update.

Do not use Schedules suggestions for older routes.

Older routes belong in [Historical Routes](/historical-routes).

Do not submit Schedules suggestions for airlines that are not part of FlyHub's official roster. Premium users who want to fly a non-roster airline should use [Manual Flights](/manual-flights).

## Suggest a route step-by-step

1. Click Suggest a route.
2. Enter airline ICAO.
3. Enter flight number.
4. Enter origin ICAO.
5. Enter destination ICAO.
6. Enter aircraft type or types.
7. Add a proof link if you have one.
8. Submit the suggestion.

Admins review suggestions before they appear in FlyHub.

## Common mistakes

- Suggesting an old route in Schedules instead of Historical Routes.
- Suggesting a route for an airline that is not in the official FlyHub roster.
- Forgetting to select aircraft before saving a generated itinerary.
- Using Roundtrip with an odd number of legs.
- Excluding the same airport you entered as a departure, arrival, or hub.