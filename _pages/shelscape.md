---
layout: page
title: SHELScape
permalink: /shelscape/
description: A spatially explicit, multi-layer agent-based model (ABM) to simulate how climate- and disaster-related shocks cascade
nav: false
horizontal: false
related_publications: true
---

*(NOTE: this page is still in the process of being updated)*

Understanding how natural disasters reshape economies requires more than measuring what is lost when a flood destroys crops or a storm disrupts transport routes. Increasingly, research shows that the most severe impacts arise not only from the immediate damage, but from how people and firms respond in the days, weeks, and months that follow. These behavioral adjustments, or how households cope with income losses, how firms reorient trade, how migration patterns shift, can generate ripple effects that extend far beyond the disaster zone.

To capture these dynamics, our research introduces SHELScape, a spatially explicit, multi-layer agent-based model (ABM) designed to simulate how climate- and disaster-related shocks cascade through interconnected socioeconomic systems. SHELScape brings together insights from several strands of literature, including earlier work on food trade networks, disaster-driven migration, and multi-layer network risk measures, and synthesizes them into a unified modeling approach.

## A Multi-Layer View of the Economy

At its core, SHELScape represents the economy as a set of interconnected locations linked through two fundamental layers:

1. A production–trade layer, describing how firms produce goods and respond to price and profit signals by reallocating supplies across space.
2. A household–migration layer, describing how households adjust consumption, labor supply, and migration decisions in response to wage and income changes.

This multi-layer perspective builds directly on earlier theoretical and empirical research showing that shocks rarely remain confined to a single sector or region. For example:

1. Our paper Assessing the cascading impacts of natural disasters in a multi-layer behavioral network framework {% cite Naqvi2021b %} demonstrates how even localized agricultural losses can set off destabilizing cycles of price increases, labor shifts, and migration flows across a broader food system.
2. Complementary work on breadbasket failures and compound climate risks shows how disruptions in one part of a trade network can transmit stress globally, depending on the structure and density of inter-regional linkages.
3. Parallel studies employing geo-simulations and migration models highlight how households respond to risks by smoothing consumption or relocating, creating economic pressures in both sending and receiving regions.

By embedding these mechanisms in a common model, SHELScape allows us to analyze how such channels interact, reinforce one another, or, under certain conditions, amplify initial shocks into widespread socioeconomic stress.

## How Agents Make Decisions

SHELScape simulates the decisions of two types of agents: firms and households, each following behavioral rules grounded in empirical studies of migration, consumption smoothing, and supply-chain adaptation.

Firms choose where to sell their goods based on relative prices, profitability, and the evolving market conditions in neighboring locations.

Households allocate income between essential goods and other consumption, adjust labor supply in response to wages, and relocate if they cannot meet minimum consumption thresholds.

These decisions are not optimized, instead, they reflect bounded rationality, allowing agents to react to imperfect information and local conditions. This design mirrors real-world behavior under uncertainty, especially during crises scenarios where decisions need to make in a highly uncertain environment.

## Tracking How Shocks Cascade

Because SHELScape explicitly models both layers of the system and their feedback loops, it reveals how a shock introduced at a single location propagates across regions and over time. A loss in food production, for example, may simultaneously:

1. raise local prices,
2. reduce real incomes,
3. trigger out-migration,
4. redirect supply chains, and
5. alter wages and prices in distant parts of the network.

These interactions can generate cyclical patterns of vulnerability, a result first documented in our Scientific Reports paper. Instead of a smooth return to equilibrium, economies may experience waves of adjustment marked by spikes in prices, shifting population flows, and periodic stress on vulnerable households.

The model also introduces a novel risk metric—the Vulnerability Rank (VRank), which summarizes a location's exposure to deprivation across multiple layers of the system. VRank accounts for a location's own purchasing power as well as the vulnerability of its neighbors, reflecting the fact that risks in networked systems are interdependent.

## Why This Matters

As climate change increases the frequency and severity of natural disasters, understanding indirect and cascading effects becomes critical. Traditional economic models tend to focus on direct damages or long-run equilibria, missing the complex transition dynamics that shape real-world recovery. SHELScape addresses this gap by providing a tool that captures:

1. spatial heterogeneity,
2. behavioral responses under stress,
3. feedback loops across economic layers, and
4. emergent vulnerabilities that cannot be inferred from direct impacts alone.

This richer understanding can inform more targeted resilience strategies, from emergency response and social protection design to infrastructure planning and climate-risk stress testing.


## Over a decade of SHELScape development (2008-2021)

SHELscape started as my dissertation project during the joint UMASS-Amherst and New School conference in 2008. At that point, ABM were in their infancy and climate shocks was not a topic of research. There were also computational limitations and access to software, that would allow the development of multi-agent systems with complex interactions, was limited. If one was doing Markov chains type analysis, then MATLAB was the way to go (R was too new back then). Mathematica was there but, despite being super powerful, it was (or is) not the easiest software to use. So the decision was to go with NetLogo, an open-source project from Northwestern University's Center for Connected Learning and Computer-Based Modeling (CCL). NetLogo is based on Logo, a program that has turtles, and we can give turtles instructions to move: `ask turtle 0 [fd 1]`. This visual element made NetLogo appealing and easy and intuitive to use. Similar logic also exists is Scratch, an MIT open-source program taught to kids in school these days (also a fun language to explore!).

Turtles can be assigned behavior, and since it was an economic model, the behavior had to come from economic literature. So two parallel developments has to take place. Learn and master NetLogo, and find the relevant literature on how agents deal with shocks. This opened up the rabbit hole of diving deeper into the literature on decision-making under uncertainity and income and consumption smoothing hypotheses. Since I wanted the model to be spatially explicit, with agents moving from one location to another, there was another challenge. Pathing routines from one node to another node did not exist. This resulted in countless hours learning about Djikstra and A-Star algorithms. Even though I abandoned this micro agent-level focus later (for reasons we will discuss below), I did manage to implement the Djikstra algorithm, which was its own reward! Later versions of NetLogo did incorporate shortest distance routines with the network extension but I had built a much more flexible path-finding function for minimizing distances (link lengths) or hops (fewest node changes), which could be combined with different probability weights (income, distance, community at destination etc.) for running different scenarios.


The first version of the model (2008-2012) led to my first publication in 2014 in the Journal of Economic Interaction and Coordination (JEIC) {% cite NaqviRehm2014 %}. The paper looked at 2010 flooding impact in Pakistan and modeled displacement of populations and markets adjustments. In 2012, the Young Scientist Summer Program (YSSP) at IIASA, led to the development of the second version of SHELscape that was considerably more aggregate and more policy oriented. It was a meso-level upgrade to the first version. There were no longer actual agents traveling from location to location, but nodes were sending flows of people and goods. This version also had a stronger focus on better market mechanisms, better implementation of probabilitic decision making, and ring-fencing spatial extents for faster results. SHELScape 2.0, led to several publications in the 2017 paper in World Development, that explored 2008 post-earthquake in northern Pakistan {% cite Naqvi2017b %}, 2020 paper on bread-basket failures in India using Copulas {% cite Naqvi2020 %}, and the 2021 paper in Nature Scientific Reports, that contextualized the framework and the broader research agenda, and introduced VRank, a multi-layer indicator for synthesizing the complexity of different market adjustments {% cite Naqvi2021b %}.

