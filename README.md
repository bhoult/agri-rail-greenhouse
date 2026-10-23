# Agri-Rail

A simulation of a one-person food farm: a hoop house built from bolt-together 3 m bays, with
a rail down the ridge that carries two robot arms, cameras on the hoops, and an AI that turns
what the cameras see into a task queue for the arms. They sow, transplant, weed, water and
harvest, starting from bare soil. Around the greenhouses are a solar array and battery, a
cistern, a cold store, a dehydrator, compost, a tilapia pool, five hens and the tiny house the
owner lives in, and all of it is metered.

Live at https://experiments.galedra.org/agri-rail-greenhouse/

![The farm in June: the hoop house with crops in its beds, the two arms on the ridge rail, the tiny house, coop and fish pool](https://experiments.galedra.org/agri-rail-greenhouse.jpg)

## What it does

- **Grows crops on the real calendar.** Lettuce is ready about 40 days after transplant,
  potatoes at about 100, tomatoes give their first truss at about 70. Temperature and
  daylight drive development; heat makes tomato, pepper and pumpkin flowers drop.
- **Follows a real site's weather.** Nairobi, Miami, Phoenix, Little Rock, Seattle,
  Minneapolis or Anchorage, from each station's 1991–2020 normals with random spells,
  storms and snow. The AI opens the sides, runs fans and pads, draws shade cloth and heats
  only as much as the crops in the beds need.
- **Sizes the farm to feed one person** from year 2 on, by growing every bed through two
  normal years first, and then checks that sizing against the simulation. The Diet tab
  tracks what the person eats against their Dietary Reference Intakes.
- **Counts everything that comes in and goes out:** energy (PV, battery, optional wind
  turbines and generator, each sized for the lowest 20-year cost), water, nutrients,
  compost, feed and money. Every component can be switched off to see what it was worth.
- **Exports** its inputs and results as a spreadsheet or a printable report.

The page's **?** button explains the rest: controls, the scenarios (pest outbreak, heat
wave, snowstorm, a person entering the greenhouse) and how each part is modelled. Crop
timings, yields and nutrients come from extension-service trials and USDA FoodData Central,
climate from NOAA, prices from US retail listings; the sources are listed in the page.
Robot dimensions, payloads and costs marked EST are illustrative.

## Running it

It is one self-contained HTML file with no build step and nothing fetched from the network.
Open `index.html` in a browser with WebGL. At up to a day per second it wants a real GPU.

## License

GPL-3.0; see `LICENSE`. The page embeds [three.js](https://threejs.org) r149, which is
MIT-licensed (Copyright 2010-2023 Three.js Authors); its license header is kept where it
starts in `index.html`.
