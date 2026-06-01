---
layout: page
title: MATSim Vienna
permalink: /matsim/
description:
nav: false
display_categories: 
horizontal: false
---

## Simulating the Future of Urban Mobility in Vienna

This page summarizes the **SimSAEV** project, short for *Simulating the Socio-economic and Environmental Effects of Shared Autonomous Electric Vehicles*.

The project uses Vienna as a case study to examine how shared, autonomous, electric vehicles could affect travel behavior, emissions, and exposure to traffic-related pollution. It combines agent-based transport simulation with detailed spatial analysis to study both system-wide effects and distributional outcomes.

The work resulted in two related papers. One focuses on traffic-related particulate matter exposure in Vienna. The other studies the introduction of shared, electric, autonomous vehicles in suburban zones at the edge of the city.

Together, the papers show both the promise and the limits of technological change in urban mobility.

## Why This Matters

Transport systems are complex, and a policy or technology that looks beneficial in one dimension may have unintended effects elsewhere.

Electric vehicles can reduce local emissions, but if they encourage more traffic, congestion and road-space use may increase. Shared autonomous vehicles can improve accessibility, but they may also attract people away from walking, cycling, or public transport. A city-wide average reduction in emissions may hide the fact that some neighborhoods or social groups remain highly exposed.

This is why simulation is useful. Instead of looking only at aggregate traffic volumes, the project uses an agent-based transport model to simulate how individual travelers move through the city over the course of a day.

The core tool is **MATSim**, a multi-agent transport simulation model. In the Vienna model, synthetic agents represent the population and follow daily activity schedules: going from home to work, school, shopping, leisure, errands, and back home. Their travel choices depend on available modes, travel times, routes, and personal characteristics.

The model was extended with an intermodal routing framework, allowing trips to combine different transport modes such as walking, cycling, public transport, cars, and shared autonomous electric vehicles. This is important because real urban travel is often multimodal: a person may walk to a station, take public transport, and then use another mode for the final part of the journey.

## Paper 1: Traffic-Related Exposure

The first paper studies the spatial and temporal exposure to traffic-related PM10 emissions in Vienna.

PM10 refers to particulate matter with a diameter of 10 micrometers or less. These particles can be inhaled and are associated with negative health effects. Road traffic produces PM10 not only through exhaust emissions, but also through non-exhaust sources such as brake wear, tire wear, and road friction.

The paper uses the Vienna MATSim model to simulate traffic-related PM10 emissions at street level. It then estimates how these emissions disperse across the city and how much exposure individuals experience depending on where they are and how they travel.

This distinction between emission concentration and exposure is crucial.

Concentration tells us where pollution is located.

Exposure tells us who is actually affected by it.

A street may have high emissions, but exposure depends on whether people live, work, study, walk, cycle, or travel nearby at the relevant time of day.

## How Exposure Was Modeled

The model simulates a representative day in Vienna. It tracks:

- where agents live, work, study, and spend time;
- which routes and modes they use;
- how much traffic occurs on each road link;
- when emissions occur during the day;
- how long agents spend in different locations and modes;
- how much PM10 they are exposed to.

The model estimates hourly PM10 concentration surfaces for the city using a spatial dispersion approach. These concentration levels are then linked back to agents' activity locations and travel behavior. Exposure is calculated for time spent at home, work, education, other locations, and while traveling by walking, cycling, car, public transport, or SAEV.

The study therefore goes beyond a static pollution map. It asks how air pollution exposure changes over time and across people.

## Main Findings on PM10 Exposure

The results show that PM10 concentrations peak during the morning and evening travel periods. Major roads and the inner-city road network are important exposure hotspots.

The model also shows that recommended PM10 thresholds can be exceeded during peak travel hours, especially at home, education, and work locations. Exposure at education facilities is particularly important because children and young people spend long periods there and may be especially vulnerable to air pollution.

A key finding is that exposure is socially uneven.

Groups with higher exposure include:

- people living in more urban locations,
- single-person households,
- children and young people aged 15 or below,
- people living closer to the city centre,
- pedestrians and cyclists using streets near traffic.

By contrast, car users are responsible for a large share of traffic-related PM10 emissions but tend to be less exposed while traveling. This creates a clear environmental justice problem: those who generate more emissions are not always those who bear the highest exposure burden.

The paper also introduces shared autonomous electric vehicles into the simulation. In this scenario, SAEVs reduce overall PM10 emissions and exposure. However, the benefits are not evenly distributed. Some groups benefit more than others, and within-group inequality can even increase. Cleaner vehicle technology alone therefore does not automatically solve exposure inequality.

## Paper 2: Suburban Mobility

The second paper focuses on a different but related question: what happens if shared, electric, autonomous vehicles are introduced in suburban zones at the outskirts of Vienna?

These zones are relatively low-density areas with weaker conventional public transport coverage, but they still have access to at least one rail-based public transport station. The idea is to test whether SAEVs can serve as a first-mile and last-mile solution: instead of replacing the entire public transport system, they help people reach high-capacity rail or subway services.

The study simulates SAEVs as demand-responsive vehicles. They do not follow fixed routes. Instead, people request rides and vehicles are dynamically assigned. Each vehicle can carry up to four passengers.

The simulations vary:

- fleet size,
- fare level,
- whether private car use or ownership becomes more expensive.

This allows the paper to examine whether SAEVs can meaningfully replace private car trips under different policy conditions.

## What Happens When SAEVs Are Introduced?

The results are sobering.

When SAEVs are introduced in suburban zones, only a relatively small share of private car trips is replaced. Depending on fleet size and fare level, around **7% to 14% of car trips** by residents of the SAEV zones are replaced by SAEVs.

This generates **CO2 emission reductions of around 5% to 11%**.

However, a substantial number of SAEV trips come from people who previously walked, cycled, or used public transport. The simulations find that **23% to 35% of trips previously made by walking or cycling** are replaced by SAEVs, as well as **10% to 20% of public transport trips**.

This is a critical result. From a climate and public health perspective, replacing car trips with SAEVs is beneficial. But replacing walking, cycling, or public transport with SAEVs can be counterproductive. It may increase vehicle kilometers, reduce active mobility, weaken public transport ridership, and worsen the use of public space.

In other words, SAEVs are not automatically sustainable. Their impact depends on what they replace.

## The Role of Pricing and Car Policy

The simulations show that SAEVs become more effective when car use and car ownership become more expensive.

When the model assumes higher costs for private car ownership and use, the share of car trips replaced by SAEVs increases to around **17% to 20%**, and CO2 emission reductions can reach up to **32%**.

This finding has an important policy implication. SAEVs on their own are unlikely to produce a major shift away from private cars. They need to be combined with policies that make private car use less attractive, such as higher car ownership costs, fuel costs, road pricing, parking restrictions, or access restrictions in dense urban areas.

But there is a trade-off. When car users switch away from private cars, travel times often increase. The model therefore shows that stronger emission reductions may come at the cost of longer travel times unless accompanied by better public transport, cycling infrastructure, and integrated mobility services.

## What the Two Papers Show Together

The two papers address different parts of the same problem.

The PM10 paper shows that transport emissions are not only an environmental issue, but also an exposure and equity issue. It matters who emits, who is exposed, where exposure occurs, and when it occurs.

The SAEV zoning paper shows that new mobility technologies do not automatically replace private cars. Without accompanying policy measures, SAEVs may attract users away from public transport, walking, and cycling instead.

Together, the papers suggest three broader lessons.

First, **technology alone is not enough**. Electric and autonomous mobility can reduce emissions, but the benefits depend on how the technology is integrated into the broader transport system.

Second, **distribution matters**. Average reductions in emissions can hide unequal exposure outcomes. Some groups may continue to face high pollution exposure even after total emissions decline.

Third, **policy design is decisive**. SAEVs are more likely to support environmental goals if they are used to complement public transport, especially in areas where conventional public transport is difficult to provide efficiently. But they should be paired with measures that discourage unnecessary car use and protect walking, cycling, and public transport.

## Why Vienna Matters

Vienna is a particularly useful case study because it already has a strong public transport system, a dense urban core, and ambitious climate and smart-city goals. At the same time, the metropolitan region includes suburban areas where car dependence is higher and public transport is less dense.

This makes Vienna a good laboratory for testing how future mobility technologies might work in practice.

The simulations show that SAEVs could play a role in improving accessibility in peripheral areas. But they also show that Vienna's existing strengths -- public transport, walking, and cycling -- should not be undermined by making automated vehicle services too cheap or too attractive relative to sustainable modes.

## Policy Implications

The findings point toward a cautious but constructive approach to SAEVs.

Shared autonomous electric vehicles may be useful as part of a broader public transport strategy, especially for first-mile and last-mile connections in suburban areas. They could help reduce reliance on private cars where fixed-route public transport is difficult to provide at high frequency.

However, their introduction should be carefully regulated.

Important design principles include:

- using SAEVs as feeders to rail-based public transport rather than as full substitutes for public transport,
- avoiding pricing structures that draw too many users away from walking, cycling, and public transport,
- combining SAEVs with restrictions or pricing measures for private cars,
- targeting areas with poor accessibility rather than dense urban cores where walking, cycling, and public transport already work well,
- monitoring distributional impacts, especially exposure impacts for children, pedestrians, cyclists, and residents near major roads,
- integrating air quality goals into transport simulation and planning.

The PM10 exposure results also suggest that traffic reduction around schools, residential streets, and high-exposure corridors could have important health benefits. Zero-emission zones, congestion pricing, traffic calming, and improved cycling infrastructure could be tested in the same modelling framework.

## Sponsors and Partner Institutes

The SimSAEV project was developed as a collaborative effort across several Austrian research institutions. The project materials and poster highlight the roles of:

- the **Austrian Climate and Energy Fund (Klima- und Energiefonds)** as the funding body,
- the **International Institute for Applied Systems Analysis (IIASA)**,
- the **Austrian Institute of Technology (AIT)**,
- and the **Vienna University of Economics and Business (WU)**.

These partners reflect the interdisciplinary structure of the project, bringing together transport simulation, systems analysis, engineering, and economic research.

The project poster is the compact summary version of the work used for dissemination, while the logos provide the institutional and funding context for the research.

## Conclusion

The SimSAEV work shows how detailed transport simulation can help cities think through the consequences of emerging mobility technologies before they are deployed at scale.

For Vienna, shared autonomous electric vehicles can reduce emissions under some conditions, but they are not a silver bullet. Their benefits depend on where they operate, how they are priced, what modes they replace, and whether they are combined with policies that reduce private car dependence.

The broader message is that future mobility should not be evaluated only by whether vehicles are electric or autonomous. It should be evaluated by whether the transport system becomes cleaner, healthier, more equitable, and more efficient.

That requires looking not only at emissions, but also at exposure. Not only at vehicles, but also at people. Not only at technology, but also at policy.
