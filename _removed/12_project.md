---
layout: page
title: SHELscape
description: A multi-layer network agent-based framework
img: assets/img/shelscape.jpg
importance: 12
category: frameworks
---

<i>(NOTE: This section is around 70% complete.)</i>

**Duration**: 2009-present

The name SHELscape, or Simulation Hub for Economic Landscapes, was coined for this project as part of a proposal submission in 2012. The proposal did not get funded by the name stayed. The name is inspired from Sugarscape, the well-known agent-based model published in 1994 in Epstein and Axtell's <a href="https://mitpress.mit.edu/books/growing-artificial-societies" target="_blank">Growing Artificial Societies</a> book. Sugarscape showed how simple rules in a simulated society can lead to complex outcomes and emergence. The SHELscape project started as part of my dissertation and has evolved over the years based on countless interactions and conversations with the agent-based community, DRR and DRM people, NGOs, and humanitarian organizations from around the globe. This section provides a broad conceptual overview of the model framework. Underneath this framework are various models that are built for different levels of analysis.


**What is SHELscape?** 

This framework combines <b>multi-layer networks</b> with <b>agent-based models</b> or ABMs. Here the key assumption is that societies, or socioeconomic systems, comprises many location nodes that are inter-connected through various layers. In other words, nodes (which could be anything from a continent, country, province, district, villages, to households) contain decision-making agents that have a various interactions both within their locations and with connected locations. These interactions can be agent-agent or agent-environment and occur across the different layer in different intensities. These layers can be conceived of as ranging from trade networks, migration networks, financial market interactions, to cross-border investments.

<div class="row" style="margin: 2.0em;">
    <div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/MD_networks.png' | relative_url }}" alt="" title="Multi-layer interactions"/>
    </div>
</div>
<div class="caption">
    Various interactions across different network layers for two regions. <i>(Source: Naqvi & Monasterolo 2021)</i>.
</div>


There could be more layers as well, but in terms of economic interactions, the above four define the majority of the interactions. One can independently study each layer in depth, which has been done in literature, but the aim here is to unify these layers in a single inter-connected framework. Furthermore, as the figure below shows, it is important to not have a top-down view, but a sideways view on the different layers: 



<div class="row" style="margin: 2.0em;">
    <div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/figure1.png' | relative_url }}" alt="" title="A multi-layer network structure"/>
    </div>
</div>
<div class="caption">
    A multi-layer network structure showing two layers, a production layer and a household layer that are interconnected at varying degrees of intensity.
</div>


A top-down approach has several limitations. First, it forces us to covert all flows into single units usually monetary values. Different layers might be dealing with different "currencies". For example migration is measured in flows of person numbers. This can be converted into monetary value, based on economic activity, productivity, income levels etc., but the unit of concern for the migration layer are stocks and flows of people. Similarly trade of goods and services, and stock-piling of inventories takes place in units of goods. This is important because physical movement needs physical units for tangible items, like food. Disruptions in these physical flows have market and monetary repercussions. Cross -layer flows are mostly in monetary terms, determined through market (demand-supply, prices) or institutional structures (minimum wages/taxes/tariffs). Thus both physical and monetary stocks and flows need to be accounted for. Second, different layers could have different connection intensities. These intensities matter in hows interactions evolve. For example, two regions might have a very high trade volume (for example, Central Asia and Europe) but their migration flows might be very low due to restrictions on human mobility. In this case, a high-density network layer is interacting with a low-density network layer, and this can also determine how networks evolve. The Figure below shows stylized economic interactions:

<div class="row" style="margin: 2.0em;">
    <div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/figure2.png' | relative_url }}" alt="" title="Behavioral interactions"/>
    </div>
</div>
<div class="caption">
    Stylized behavioral economic interactions within and across nodes. <i>(Source: Naqvi & Monasterolo 2021)</i>.
</div>

In this simplified circular-flow economy setup, households provide labor in exchange for wages from firms, and households use this income to purchase commodities produced by firms. Due to wage and price differences, households can also provide labor in other locations, and firms can sell their goods elsewhere as well. In a frictionless gravity model-like setting, these push and pull factors will equalize the distribution of populations and goods such that prices are equalized across the locations.


**Where is this framework useful?** 

Let's start with the work I have done with this framework, and that is cascading of economic shocks. Natural disasters and other sudden economic shocks result in complex outcomes. Post-shock transition phases are chaotic. As the figure below shows, the recovery process can result in three types of outcomes: poorer conditions, equal, or better conditions relative to the pre-shock period.


<div class="row" style="margin: 2.0em;">
    <div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/transition.png' | relative_url }}" alt="" title="Economic transition"/>
    </div>
</div>
<div class="caption">
    Post-shock transition pathways. <i>(Source: Naqvi & Monasterolo 2021)</i>.
</div>

It is during these transition processes that policymakers need to respond. Thus response time is limited and usually there are resources constraints. If the region is low-income, then it also has poorer data, thus it is not even clear what the baseline is. In this setup, the framework proposed here can help with policy planning by simulating behavior responses to shocks and tracking post-shock outcomes.


**The logic behind the framework** 

Shocks to one part of the network can cascade to other parts in a multi-layer setup. Because of the nature of the setup, and behavioral responses, this and can result in unintended consequences. For example, a climate shock can cause supply shortages (destruction of capital, disruption of supply chains), or displacement (destruction of houses, life loss, lack of economic opportunities). Usually both of these will happen simultaneously and at different intensities. In the absence of strong social safety nets, this will initiate a post-shock recovery phase mostly led by adaptation of agents within location nodes. This will be driven by some behavior rules. While exact individual rules are probably impossible to determine, average patterns of response can are now fairly well-defined in literature. Within the applied economic literature, especially development economics, there is a plethora of evidence on how households coping strategies are invoked. While a lot more need to be done on this topic, it does provide us with important insights. For example, if households face income shocks, they will run down their savings, borrow money, maybe switch to self-subsistence farming if they have land, or migrate elsewhere for economic opportunities. Similarly profit maximizing firms will not sell in unprofitable markets (usually the shocked ones) resulting in supply chain adjustments and price shocks. If a large section of the households and firms in one part of the network are adjusting, then it can result in short-term market spikes that can result in further feedbacks that can amplify the shock. As a result, the shock impact also cascades to other parts of the network, affecting farther-away regions.


<div class="row" style="margin: 2.0em;">
    <div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/figure4a.png' | relative_url }}" alt="" title="Household's thresholds"/>
    </div>
    <div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/figure4b.png' | relative_url }}" alt="" title="Firm's thresholds"/>
    </div>
</div>
<div class="caption">
The left figure shows the income-consumption line for households The right figure shows the quantity-price line for firms. Households face a minimum consumption threshold and firms face a minimum cost threshold.  
</div>

Agents also face thresholds that can trigger behavioral changes as shown in the figures above. For example, households will not reduce their consumption to zero if their income falls to zero. They need to consume a minimum level $$\bar{c}$$. Hitting this threshold might trigger consumption smoothing strategies, of which one is migration. The second figure shows firm's thresholds. Firms have minimum costs, and if the market price in a destination location falls below this threshold, their will find it unprofitable.

We can simulate this on the model framework to understand how the shocks cascade both spatially and temporally. But let's look at the figure below which shows average income on the y-axis and average food prices on the x-axis:


<div class="row" style="margin: 2.0em;">
    <div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/figure7.png' | relative_url }}" alt="" title="Cyclical vulnerability"/>
    </div>
</div>
<div class="caption">
    Cyclical vulnerability
</div>

The lines are benchmarked to the baseline business-as-usual (BAU) scenario. Before a shock happens, we are at the top left corner with 0% change from the baseline for both indicators. As the shock unfolds, average income falls and food prices rise before stabilizing at a long-run stable point as markets, labor, and supply chains settle down. In this figure we can observe that vulnerability is exacerbated in the short-run which means that some populations might be highly exposed. This highlights two points. First vulnerability is cyclical, even in a perfectly adjusting model where the network structures remain exactly the same. If we add market frictions or change network configuration (for example, by removing nodes), the outcomes are likely to be much worse.

**Model features**

While the above framework is broad and generic, the model itself is programmed and implemented in NetLogo, a free ABM software developed by the Northwestern University. ABMs have their own unique advantages and disadvantages. They are excellent at dealing with bounded rationality, adaptive behavior, and learning, and they can handle non-linear dynamics very well. They are also very good iterative solvers for a very large complex systems. ABMs also have disadvantages. They are unbounded systems. Which means one can build in as much as possible and explode the parameter space. Thus crafting the model is essential and very context dependent, and the burden of highlighting the qualitative value addition over simpler, analytical models invariably falls on the researcher. 

The SHELscape model framework is modular in nature. Location-level components (production, employment, income, consumption), and inter-location components (migration and trade) are defined independently and interlinked. Each component is determined by rules derived from mostly standard economic literature (see the papers below for equation details). On top this structure, are several modeling innovations built into the model to accommodate the network structures. These are:

1) A-star path-finding routine for traveling along networks: This module takes the network structure and finds optimal routes based on link lengths, weighted links, and hops (minimum switches across links). This module is core for short-listing a target node location set for flow decisions.

1) Search-and-match market algorithms: This module searches market destinations as a combination of distances (negative weight) and relative economic gains (real income gains or real profit gains). The joint probability distribution is defined by a logistic function that can be visualized as follows:


<div class="row" style="margin: 2.0em;">
    <div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/figure5.png' | relative_url }}" alt="" title="Probability distribution"/>
    </div>
</div>
<div class="caption">
    Joint-probability distribution for location selection
</div>

The figure above implies trade-offs between nearer locations with low-economic gains with farther away locations with higher economic gains. The decision to select locations is also not deterministic but rather than probabilistic. This implies that a highly desirable destination has a high "chance" of getting selected and is not automatically assigned a probability of one. This allows distributions to be generated for simulations with exactly the same setup. Just by randomizing the seed and rerunning the same simulation multiple times, we can discover different pathways and equilibriums that can emerge from certain shocks. And we can assign probability propensities to these events.

The SHELscape framework also implies various trade-offs in an ABM setting. This depends on (a) the research question, (b) depth of the set up of each layer, (c) data availability to support the calibration, and (d) the time horizon being studied.


**VRank: A multi-layer risk measure** 

The framework also introduces a new multi-layer risk measure, called <b>Vulnerability Rank</b>, or <b>VRank</b>, to quantify the stress in the system as a result of a natural disaster. This measure follows a stream of recent and relevant advances in multi-dimensional network measures like the <a href="https://www.nature.com/articles/srep00541" target="_blank">DebtRank</a>, which measure of financial distress propagation in financial networks, and <a href="https://en.wikipedia.org/wiki/PageRank" target="_blank">PageRank</a>, the algorithm that determines how Google search results are returned.

By introducing a multi-layer risk measure, the complexity of vulnerability, which arises from various interactions, can be reduced into a single measure. For example, DebtRank considers the portfolio holdings of banks, their debts, and loans and derives a measure of risk of default. Since banks are in a network setting, one bank's risk is not only determined by its own balance sheets but also those of connected banks that own its debt or lend it money. In this setup, even a small benign node failing can cascade across the whole system potentially resulting in a system collapse. While multi-layer networks and systemic risk measures are becoming more important in the banking sector especially in central banks (for example, the European Central Bank (ECB)), the insights from these applications also have an important, yet under-explored, applications to climate shocks and their subsequent cascading impact on socioeconomic systems.

In the model framework presented here, vulnerability, particularly in low-income food-producing regions, is defined in terms of a minimum consumption bundle $$ \bar{c} $$. Agents falling below $$ \bar{c} $$ are labeled as <i>food insecure</i>, and if their consumption needs are not immediately met, it can result in second round negative impacts like poor health, lower productivity, reduced economic output, conflict, and displacement. Minimum consumption bundles are well-defined and usually measured in adult-equivalent caloric in-take per capita, which also determines food-based poverty lines31.

In our model setting, the ability to purchase a minimum consumption bundle $$ \bar{c} $$, is determined by price (supply) and income and savings (demand) including the ability to import the supply from neighboring nodes, and earn income elsewhere. Formally, VRank is defined as:

$$
    VRank_{it} = \left( \frac{p_{it} \bar{c}}{w_{it} L_{it}} \beta \frac{\sum_{j \neq i}{p_{jt}\bar{c}}}{\sum_{j \neq i}{w_{jt} L_{jt}}}  \right)^{1/2} \nonumber
$$

where  $$i $$ = own location, $$j $$ = neighbors, $$ p $$ = price, $$ \bar{c} $$ = cost of minimum consumption bundle, $$ w $$ = wages, $$ L $$ = labor supply. A higher value of $$VRank_{it}$$ implies higher vulnerability.

The VRank formula, captures two key elements. First, it shows the dependence of a node from another one in terms of food supply. For instance, a node which does not produce any food commodity would be considered vulnerable in isolation, but if it is connected with several food producing locations that could supply it with food, it would show a much lower VRank index. In addition, this node would be in a better position than a completely isolated food-producing node. Second, VRank captures the displacement and migration channels of vulnerability. A node that produces enough food for its own consumption might experience a sudden population influx from highly vulnerable neighboring nodes, thus becoming vulnerable to the shock. Therefore, the VRank allows us to quantify multiple sources of vulnerability, and also resilience, in a single quantitative index.
 

<div class="row" style="margin: 2.0em;">
    <div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/figure8a.png' | relative_url }}" alt="" title="Food-to-Labor price ratio"/>
    </div>
    <div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/figure8b.png' | relative_url }}" alt="" title="Average food consumption"/>
    </div>
	<div class="col">
        <img class="img-fluid" img align="bottom" src="{{ '/assets/img/figure9.png' | relative_url }}" alt="" title="VRank"/>
    </div>
</div>
<div class="caption">
The left figure shows the food-to-labor price ration, the middle figure shows the average food consumption, while the right figure shows the VRank. The y-axis is the node density measure by number of nodes connected with a node, and the x-axis shows the distance to the shocked region.
</div>
 
The figure above shows how the shock spreads over time in the simulated regions. The y-axis is the node density and the x-axis shows the distance to the shocked region. Here we can observe that higher density nodes pass the shock earlier but also see higher volatility. More isolated remote nodes are also impacted by the shock. In summary, while the disaster recovery focuses on the directly affected regions, connected neighbors might also need policy response and might even be key to a more refined recovery process.
 
 
**The larger picture**

coming soon! 
 


**Selected papers and reports**

Naqvi, A., and Monasterolo, I. (2021). Assessing the cascading impacts of natural disasters in a multi-layer behavioral network framework. Nature Sci Rep 11, 20146. DOI: 
https://doi.org/10.1038/s41598-021-99343-4

Naqvi, A., Gaupp, F. & Hochrainer-Stigler, S. The risk and consequences of multiple breadbasket failures: an integrated copula and multilayer agent-based modeling approach. OR Spectrum 42, 727–754 (2020). DOI: https://doi.org/10.1007/s00291-020-00574-0

Naqvi, A. (2017). Deep Impact: Geo-Simulations as a Policy Toolkit for Natural Disasters. World Development
Volume 99, November 2017, p. 395-418. DOI: https://doi.org/10.1016/j.worlddev.2017.05.015

Naqvi, A., Rehm, M. (2014). A multi-agent model of a low income economy: simulating the distributional effects of natural disasters. Journal of Economic Interaction and Coordination 9, p. 275–309. DOI: https://doi.org/10.1007/s11403-014-0137-1

Naqvi, A., Rehm, M. (2014). Simulating natural disasters - A complex systems framework. 2014 IEEE Conference on Computational Intelligence for Financial Engineering & Economics (CIFEr), London, England. DOI: https://doi.org/10.1109/CIFEr.2014.6924103.

Naqvi, A., Sobiech, C. (2010). Simulating Humanitarian Crisis and Socio-Economic Vulnerability: Applications of Agent Based Models. Published in collection "Tipping Points in Humanitarian Crisis:
From Hot Spots to Hot Systems" (http://collections.unu.edu/eserv/UNU:1880/pdf7511.pdf). United Nations University – Institute for Environment and Human Security (UNU-EHS) SOURCE 13.

