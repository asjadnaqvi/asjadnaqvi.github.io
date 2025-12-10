---
layout: page
title: SHELScape ABM
permalink: /shelscape/
description:
nav: false
horizontal: false
related_publications: true
---


Understanding how natural disasters reshape economies requires more than measuring what is lost when a flood destroys crops or a storm disrupts transport routes. Increasingly, research shows that the most severe impacts arise not only from the immediate damage, but from how people and firms respond in the days, weeks, and months that follow. These behavioral adjustments, or how households cope with income losses, how firms reorient trade, how migration patterns shift, can generate ripple effects that extend far beyond the disaster zone.

To capture these dynamics, our research introduces SHELScape, a spatially explicit, multi-layer agent-based model (ABM) designed to simulate how climate- and disaster-related shocks cascade through interconnected socioeconomic systems. SHELScape brings together insights from several strands of literature, including earlier work on food trade networks, disaster-driven migration, and multi-layer network risk measures, and synthesizes them into a unified modeling approach.

# A Multi-Layer View of the Economy

At its core, SHELScape represents the economy as a set of interconnected locations linked through two fundamental layers:

1. A production–trade layer, describing how firms produce goods and respond to price and profit signals by reallocating supplies across space.
2. A household–migration layer, describing how households adjust consumption, labor supply, and migration decisions in response to wage and income changes.

This multi-layer perspective builds directly on earlier theoretical and empirical research showing that shocks rarely remain confined to a single sector or region. For example:

1. Our paper Assessing the cascading impacts of natural disasters in a multi-layer behavioral network framework {% cite Naqvi2021b %} demonstrates how even localized agricultural losses can set off destabilizing cycles of price increases, labor shifts, and migration flows across a broader food system.
2. Complementary work on breadbasket failures and compound climate risks shows how disruptions in one part of a trade network can transmit stress globally, depending on the structure and density of inter-regional linkages.
3. Parallel studies employing geo-simulations and migration models highlight how households respond to risks by smoothing consumption or relocating, creating economic pressures in both sending and receiving regions.

By embedding these mechanisms in a common model, SHELScape allows us to analyze how such channels interact, reinforce one another, or, under certain conditions, amplify initial shocks into widespread socioeconomic stress.

# How Agents Make Decisions

SHELScape simulates the decisions of two types of agents: firms and households, each following behavioral rules grounded in empirical studies of migration, consumption smoothing, and supply-chain adaptation.

Firms choose where to sell their goods based on relative prices, profitability, and the evolving market conditions in neighboring locations.

Households allocate income between essential goods and other consumption, adjust labor supply in response to wages, and relocate if they cannot meet minimum consumption thresholds.

These decisions are not optimized, instead, they reflect bounded rationality, allowing agents to react to imperfect information and local conditions. This design mirrors real-world behavior under uncertainty, especially during crises scenarios where decisions need to make in a highly uncertain environment.

# Tracking How Shocks Cascade

Because SHELScape explicitly models both layers of the system and their feedback loops, it reveals how a shock introduced at a single location propagates across regions and over time. A loss in food production, for example, may simultaneously:

1. raise local prices,
2. reduce real incomes,
3. trigger out-migration,
4. redirect supply chains, and
5. alter wages and prices in distant parts of the network.

These interactions can generate cyclical patterns of vulnerability, a result first documented in our Scientific Reports paper. Instead of a smooth return to equilibrium, economies may experience waves of adjustment marked by spikes in prices, shifting population flows, and periodic stress on vulnerable households.

The model also introduces a novel risk metric—the Vulnerability Rank (VRank), which summarizes a location's exposure to deprivation across multiple layers of the system. VRank accounts for a location's own purchasing power as well as the vulnerability of its neighbors, reflecting the fact that risks in networked systems are interdependent.

# A Growing Research Program

SHELScape is part of a broader research agenda aimed at understanding the complexity of climate-related risks:

1. Earlier work {% cite NaqviRehm2014 %}{% cite Naqvi2017b %} used agent-based geo-simulations to analyze how natural disasters create distributional impacts in low-income economies.
2. Studies on breadbasket failure risks {% cite Naqvi2020 %} combined copulas with multilayer ABMs to assess how correlated climate shocks can destabilize global food systems.


SHELScape extends these efforts by providing a modular and flexible platform that can incorporate new layers, such as infrastructure networks, financial markets, or public-sector response mechanisms.

# Why This Matters

As climate change increases the frequency and severity of natural disasters, understanding indirect and cascading effects becomes critical. Traditional economic models tend to focus on direct damages or long-run equilibria, missing the complex transition dynamics that shape real-world recovery. SHELScape addresses this gap by providing a tool that captures:

1. spatial heterogeneity,
2. behavioral responses under stress,
3. feedback loops across economic layers, and
4. emergent vulnerabilities that cannot be inferred from direct impacts alone.

This richer understanding can inform more targeted resilience strategies, from emergency response and social protection design to infrastructure planning and climate-risk stress testing.