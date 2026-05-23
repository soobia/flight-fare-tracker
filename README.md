# Flight Fare Tracker

A Claude-powered flight fare monitor that searches and summarizes round-trip 
fares for a configured route across multiple aggregator sites and airlines.

Currently runs as a manually triggered scheduled task. Kick it off when you 
want a fresh fare check -- no automation yet, but that is on the roadmap.

---

## What it does today

- Searches Google Flights, Kayak, Skyscanner, Momondo, and Expedia for 
  current round-trip fares on your configured route
- Filters by cabin class, number of stops, and traveler count
- Focuses on major airlines serving the route
- Returns a clean summary with cheapest fare, top options, prices, 
  layover cities, and direct booking links
- Notes any pricing trends (fares rising, best days to fly, etc.)

---

## Configuration

| Setting | Value | Notes |
|---|---|---|
| Origin | JFK | Replace with your departure airport |
| Destination | KHI | Replace with your destination airport |
| Outbound window | Mid-May | Adjust to your target travel dates |
| Return window | Mid-June | Adjust to your target return dates |
| Stops | 1 stop only | Change to nonstop or 2+ as needed |
| Cabin | Economy | Change to Business or First as needed |
| Travelers | 1 adult | Adjust as needed |

---

## How to use

1. Open Claude with the scheduled task
2. Update the date ranges in the script to your target travel window
3. Trigger manually
4. Claude searches the web across multiple aggregators and returns a 
   summary within a minute or two

---

## Current limitations

- Date ranges must be updated manually before each run
- No price history tracking yet -- each run is a snapshot
- No automatic alerts when fares drop below a threshold
- No calendar integration

---

## Roadmap

- Auto-detect and update date ranges based on a configured trip window
- Track fare history across runs and flag when prices drop significantly
- Email alert when a fare drops below a configured threshold
- Expand to multiple routes in a single run
- Compare one-way vs round-trip pricing automatically

---

## Built with

- Claude scheduled tasks
- Claude web search
- Python (planned for fare history tracking and email alerts)

---

*Built for JFK to KHI. Adaptable to any route by updating the origin, 
destination, and airline list in the script.*
