# Tide Guide

A one-page tide chart you can put on your phone's home screen. Open it and you
see the day's tide curve, where the tide is right now, the wind for the next few
hours, and when the sun comes up and goes down.

Two versions:

| | Covers | Tide data |
|---|---|---|
| `tide-guide.html` | United States | NOAA CO-OPS predictions |
| `tide-guide-au.html` | Australia | Open-Meteo marine model |

**Live links**

- US — https://flowbanacci.github.io/Jay-Swimmys-Tide-Guide/tide-guide.html
- Australia — https://flowbanacci.github.io/Jay-Swimmys-Tide-Guide/tide-guide-au.html

No account, no install, no tracking. Each page is a single HTML file that fetches
fresh data every time you open it.

## What you get

**The chart**

- Tide curve for the day, midnight to midnight
- High and low points labelled with height and time
- A red "now" line showing the current tide height (today only, updates each minute)
- A dashed orange swim line — 1 ft on the US chart, 0.3 m on the Australian one
- Fixed height scale so the chart reads the same every day: −3 to 10 ft (US,
  1 ft lines) and −2 to 5 m (Australia, 0.5 m lines). It stretches automatically
  at big-tide places like Olympia, Broome or Derby so nothing gets cut off.

**Wind** — direction, speed and gusts for right now and the next three hours.
Letters are the direction the wind is coming *from*; the arrow points the way
it's blowing *to*. Miles per hour in the US, km/h in Australia.

**Below that** — next high and low tide, sunrise, sunset, moon phase, and the
current water temperature.

**Places** — a favourites dropdown, a search box, and a date picker for any past
or future day. Tide predictions are astronomical, so past and future dates are
equally accurate.

US favourites: Bellingham (default), Tacoma, Neah Bay, Newport OR, Olympia.
Australian favourites: Byron Bay (default), Brunswick Heads, Lennox Head,
Ballina, Gold Coast. You can add your own.

## Put it on your phone

1. Open the link in **Safari** (iPhone) or **Chrome** (Android).
2. Tap **Share → Add to Home Screen**.

You get an icon that behaves like an app. Your favourites and last-viewed spot
save privately on your own device — nothing is sent anywhere.

## Where the data comes from

- **US tides** — [NOAA CO-OPS](https://api.tidesandcurrents.noaa.gov/) predictions,
  MLLW datum, feet, station local time. Bellingham and most stations are
  *subordinate*, meaning NOAA publishes only the high and low points; the curve
  between them is drawn by cosine interpolation, which is standard practice.
- **Australian tides** — [Open-Meteo](https://open-meteo.com/) marine model,
  metres against mean sea level. Australia's Bureau of Meteorology has no free
  public tide API, so this is a **model estimate, not the official tide tables**.
  Fine for planning a swim or a paddle. **Do not use it for navigation.**
  Range is roughly three months back to two weeks ahead.
- **Wind** — Open-Meteo forecast, 10 m above ground, refreshed about every
  15 minutes.
- **Water temperature** — the station's own NOAA sensor where one exists,
  otherwise a satellite estimate for that spot, otherwise the nearest NOAA sensor
  within 60 miles. The US page always shows the closest sensor reading as a
  second line. Australia uses the satellite estimate.
- **Sunrise, sunset and moon phase** — calculated in the page itself. No API,
  works offline once loaded.

## Good to know

- If NOAA has an outage the US page says so plainly and offers a retry — sun,
  moon and water temperature keep working, since they come from elsewhere.
- Wind only shows for today. "Now, +1h, +2h, +3h" has no meaning on another date.
- Nothing is stored on a server. Favourites live in your browser's local storage.

## Buy me a coffee 🍻

There's a tip link at the bottom of each page — Venmo and PayPal on the US
version, PayPal on the Australian one. Entirely optional, and the guide works
exactly the same either way.
