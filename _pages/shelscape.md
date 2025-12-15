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

Understanding how natural disasters reshape economies requires more than measuring what is lost when a flood destroys crops or a storm disrupts transport routes. Increasingly, research shows that the most severe impacts arise not only from the immediate damage, but from how people and firms respond in the days, weeks, and months that follow. These behavioral adjustments—how households cope with income losses, how firms reorient trade, and how migration patterns shift—can generate ripple effects that extend far beyond the disaster zone.

To capture these dynamics, this research introduces **SHELScape**, a spatially explicit, multi-layer agent-based model (ABM) designed to simulate how climate- and disaster-related shocks cascade through interconnected socioeconomic systems. SHELScape brings together insights from food trade networks, disaster-driven migration, and multi-layer risk modeling, synthesizing them into a unified analytical framework.


## Why Agent-Based Models?

Physical shocks propagate through economic systems under conditions of **high uncertainty**, **limited data**, and **severe time constraints for policy response**. Traditional equilibrium-based models struggle in this setting, as they are ill-equipped to represent transitions, thresholds, and non-linear feedbacks.

Agent-based models (ABMs) are particularly well suited because they:
- explicitly model decision-making under uncertainty,
- capture non-linear interactions and tipping points,
- allow for adaptation and learning,
- and link **micro-level behavior** to **meso- and macro-level outcomes**.

<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/transition.png" title="Transitions, thresholds, and feedbacks can result in non-linear dynamics" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   Transitions, thresholds, and feedbacks can result in non-linear dynamics {% cite Naqvi2021b %}.
</div>



## Viewing the economy through a multi-layer lens

At its core, SHELScape represents the economy as a system of interconnected locations embedded in **multiple interacting network layers**:

1. **Production–trade layer**  
   Firms produce goods and allocate supply across locations in response to prices, profits, and market access.

2. **Household–migration layer**  
   Households adjust consumption, labor supply, and migration decisions based on wages, prices, and minimum consumption requirements.

These layers interact continuously. Production decisions affect wages and prices; household decisions affect labor availability and demand. Shocks introduced in one layer propagate through the other, often amplifying initial impacts.


<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/layers.png" title="Stylized multi-layer behavioral network framework (production–trade and household–migration layers)" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   This conceptualization is formalized in {% cite Naqvi2021b %}, which shows how localized shocks can trigger system-wide dynamics through network interactions.
</div>



## How agents make decisions

SHELScape simulates two types of agents:

- **Firms** choose where to sell goods based on relative prices, profitability, and access costs. They can redirect supply across space as markets evolve.
- **Households** allocate income between essential and non-essential goods, supply labor locally, and migrate if they can no longer meet minimum consumption thresholds.

Decisions are **probabilistic rather than optimizing**, reflecting bounded rationality and imperfect information. Agents may choose sub-optimal options, particularly under stress, which allows the model to generate realistic transition dynamics rather than instantaneous adjustment.


<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/shelscape_framework.png" title="Stylized multi-layer behavioral network framework (production–trade and household–migration layers)" class="img-fluid rounded z-depth-1" %}
    </div>
</div>



## Thresholds and tipping dynamics

A central feature of SHELScape is the explicit modeling of **economic thresholds** that can trigger regime changes:

- **Household thresholds:**  
  When real income falls below the level required to purchase a minimum consumption bundle, households shift behavior, first reallocating consumption, running down savings, and then migrating.

- **Firm thresholds:**  
  Firms stop supplying markets where prices fall below production costs and reallocate output to more profitable locations.

Crossing these thresholds can generate **non-linear transitions**, including cascading failures, spatial polarization, and persistent vulnerability.


<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/shelscape_thresholds.png" title="Thresholds in household consumption and firm production decisions" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
	These mechanisms play a key role in work on compound shocks and breadbasket failures {% cite Naqvi2020 %}, where correlated climate risks push systems beyond critical tipping points.
</div>




## Tracking cascading impacts

Because SHELScape integrates multiple layers and feedback loops, it captures how a localized shock—such as a food production loss—can simultaneously:
1. raise local prices,
2. reduce real incomes,
3. trigger out-migration,
4. redirect trade flows,
5. and alter wages and prices in distant regions.

Rather than converging smoothly to a new equilibrium, the system often exhibits **cyclical adjustment paths**, with repeated waves of stress during the transition phase.


<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cyclical_vulnerability.png" title="Cyclical vulnerability and post-shock transition dynamics" class="img-fluid rounded z-depth-1" %}
    </div>
</div>



## Quantifying multi-layer vulnerability

To synthesize these complex dynamics, SHELScape introduces **Vulnerability Rank (VRank)**, a multi-layer risk indicator inspired by systemic risk measures in financial networks.

VRank captures:
- a location's own purchasing power relative to minimum consumption needs,
- its dependence on neighboring locations through trade and migration,
- and the propagation of vulnerability across the network.

This allows the identification of **vulnerability hotspots**, even in regions not directly hit by the initial shock.


<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/vrank_evolution.png" title="Spatial-temporal evolution of vulnerability (VRank)" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


## Applications and empirical case studies

SHELScape has evolved through multiple applied studies:

- **2010 Pakistan floods**: Market search algorithms and displacement dynamics {% cite NaqviRehm2014 %} 
- **2005 Kashmir earthquake**: GIS-integrated spatial spillovers and recovery dynamics {% cite Naqvi2017b %} 
- **2003 droughts in India**: Copula-based climate risk structures and multi-layer cascades {% cite Naqvi2020 %} 
- **General framework and VRank**: Cascading impacts and cyclical vulnerability {% cite Naqvi2021b %} 



## Going beyond disaster impacts

The SHELScape framework naturally extends to:
- cascading value-chain risks,
- balance-of-payments pressures,
- balance-sheet vulnerabilities,
- disaster financing and gap models,
- and the interaction between supply-side and demand-side recovery.

These extensions allow the model to connect disaster risk analysis with broader macro-financial and development questions.

<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/MD_networks.png" title="Generic approach to multi-layer networks" class="img-fluid rounded z-depth-1" %}
    </div>
</div>





## Over a decade of development (2008–2021)

SHELscape started as my dissertation project during the joint UMASS-Amherst and New School conference in 2008. At that point, ABM were in their infancy and climate impacts on economic systems was not a major topic of research. There were also computational limitations and access to software, that would allow the development of multi-agent systems with complex interactions, was limited. If one was doing Markov chains-type analysis, then MATLAB was the way to go (R was too new back then). Mathematica was there, but despite being a super powerful software, it was (or is) not the easiest program to use. My supervisor [Duncan Foley](https://www.newschool.edu/nssr/faculty/duncan-foley/) did use it extensively for his own models. So my decision was to go with [NetLogo](https://www.netlogo.org/), an open-source project from Northwestern University's [Center for Connected Learning and Computer-Based Modeling (CCL)](https://ccl.northwestern.edu/). NetLogo is based on Logo, a program that has turtles, and we can give turtles instructions to move in an intuitive way, e.g. `ask turtle 0 [fd 1]`, which would make Turle 0 move forward one step on the screen. This visual element made NetLogo appealing and relatively easier to use but there were some challenges along the way. On a side note, similar Logo-type logic also exists in [Scratch](https://scratch.mit.edu/), an open-source software from MIT taught to kids in school these days (and also a fun language to explore).

There are two challenges with developing a spatially-explicit micro-founded Agent-Based Model (ABM). First are decisions to move around a pre-defined space, and second to make behvioral decisions that among other things, also involve moving around the canvas. Agents can "own" variables (or asset stocks) such as labor, money, food etc that can be intialized based on some distribution, and these can evolve depending on interactions with the (a) environment and (b) with other agents. Since SHELScape is an economic model, the behavior needs to come from economic literature on agents make decisions. So two parallel developments took place during the development of the model; (a) learn and master NetLogo especially on how agents move around, and store decisions in a complex array of nested lists, and (b) find the relevant socioeconomic literature on how agents deal with shocks. This opened up a rabbit hole of diving deeper into the literature on decision-making under uncertainity, evidence on income and consumption smoothing, permanent income hypothesis, etc. On the programming side there was another challenge; since agents exist at specific locations that form their own micro cosmos of economic interactions, a change of location would alter the behivior as agents get added and subtracted. But changing locations is a complex process which also implies physically moving from one location to another along links of varying lengths (or road networks) that can get destroyed. At that point, pathing routines did not exist in NetLogo. As a result, countless hours went into learning about Djikstra and A-Star algorithms. Even though I abandoned this micro agent-level focus later (for various reasons we will discuss below), I did manage to implement the Djikstra algorithm, which was its own reward. Later versions of NetLogo did incorporate shortest-distance routines with the additional of the network (nw) extension,  but I had already built a flexible path-finding function that could minimize travel time based on distances (link lengths) or hops (fewest node changes), and could be combined with different probability weights (income, distance, community at destination etc.) for running different scenarios.

The first version of the model (v1.0 2008-2012) led to my first publication in 2014 in the Journal of Economic Interaction and Coordination (JEIC) {% cite NaqviRehm2014 %}. The paper looked at 2010 flooding impact in Pakistan and modeled displacement of populations and markets adjustments. In 2012, during the Young Scientist Summer Program (YSSP) at IIASA, led to the development of the second version of SHELscape (v2.0 2012-2021) that was considerably more aggregate and more policy oriented. It was a meso-level upgrade to the first version where the uncessary routines of micro agent decisions, including traveling and movements along paths were taken out. Instead, nodes (or locations) would sending flows of people and goods based that would arrive based on distances and their relative distances. This version also had a stronger focus on better market mechanisms, better implementation of probabilitic decision making, and ring-fencing of spatial extents to make the model computationally faster (other if all locations are being evaluated, then we would have a $$O(N^2)$$ explosion). SHELScape 2.0, led to several publications; World Development in 2017, that explored 2008 post-earthquake in northern Pakistan {% cite Naqvi2017b %}, 2020 paper on bread-basket failures in India using Copulas {% cite Naqvi2020 %}, and the 2021 paper in Nature Scientific Reports, that contextualized the model framework, and introduced *VRank*, a multi-layer indicator for synthesizing the complexity of different market adjustments {% cite Naqvi2021b %}.


## Funding and support

The model evolved over a long time horizon and variations of it have been part of several projects. See individual papers for references and acknowledgements to various grants.