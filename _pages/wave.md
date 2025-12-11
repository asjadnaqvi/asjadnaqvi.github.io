---
layout: page
title: The WAVE Model: Integrating Elasticities, Welfare and Value Added 
permalink: /wave/
description:
nav: false
display_categories: 
horizontal: false
related_publications: true
---



# Why We Need a New Model  

Assessing how global economic shocks spread across countries and sectors requires tools that capture both behavioural responses and structural interdependencies. Trade models estimate welfare changes using substitution elasticities, but these are often externally calibrated and rely on restrictive assumptions about homothetic and linear preferences. They tell us how trade flows might reallocate but not how these shifts propagate through domestic and international production networks.

MRIO and IO models, by contrast, excel at describing supply-chain propagation, but assume fixed technical coefficients and no behavioural substitution. They show how production responds mechanically to shocks, but not how consumers and firms alter demand when prices change.

Together, these limitations motivate the development of the **Welfare and Value Added Elasticities (WAVE)** model, which integrates flexible demand estimation with structural production linkages to deliver a coherent and empirically grounded welfare analysis.



# What the WAVE Model Does  


The WAVE model combines a Quadratic Almost Ideal Demand System (QUAIDS), estimated using reshaped MRIO expenditure and price data in {% cite naqvi2025a %} with the *Asian Development Bank's Multi-Regional Input–Output (ADB MRIO)* framework used in {% cite naqvi2025b %}. This integration allows WAVE to estimate behavioural demand responses to shocks and trace them through global value chains to quantify changes in Value Added (VA), a welfare-relevant metric aligned with GDP.

## QUAIDS demand structure  
In Naqvi 2025a, the budget share for region $r$ in the expenditure of country–sector $(c,s)$ is expressed as:

$$
w_{(c,s),r} = \alpha_r + \sum_{r'} \gamma_{rr'} \ln p_{r'} + \beta_r \ln \left(\frac{X_{(c,s)}}{a(p)} \right) + \lambda_r \left[\ln \left(\frac{X_{(c,s)}}{a(p)}\right)\right]^2 .
$$

From this system, own- and cross-price elasticities and income elasticities are derived, forming the behavioural core of the WAVE model.

## Translating tariffs into demand changes  
A tariff $\tau_r$ applied to imports from region $r$ raises its price to:

$$
p'_r = p_r (1 + \tau_r),
$$

and the proportional change in demand across all supplying regions becomes:

$$
Q = E\, \Delta p + \eta\, \Delta m,
$$

where $E$ is the matrix of uncompensated price elasticities and \( \eta \) the income elasticity vector. {% cite naqvi2025b %} sets $\Delta m = 0$ under constant-expenditure simulations.

## Mapping demand shifts into global production  
Demand adjustments feed back into the MRIO system, modifying intermediate and final demand:

$$
x_1 = (I - A_0)^{-1} y_1,
$$

where $A_0$ is the baseline technology matrix and $y_1$ the post-shock final-demand vector.

Value added then adjusts proportionally through:

$$
v_1 = \alpha_0 \odot x_1,
$$

with $\alpha_0$ denoting value-added coefficients and $\odot$ element-wise multiplication.

These equations connect behavioural shifts to structural propagation, creating an integrated welfare evaluation tool.



# What makes WAVE different  

WAVE differs fundamentally from traditional trade or IO models in several ways. First, it relies on empirically estimated elasticities derived directly from MRIO data rather than stylised parameters. This approach captures regional substitution patterns and non-linear income effects more realistically, especially via the QUAIDS specification of {% cite naqvi2025a %}.

Second, by embedding these elasticities within the MRIO system, WAVE models the entire pass-through of shocks, from consumer substitution to global supply-chain propagation, offering a richer picture than either approach can provide alone.

Third, the framework evaluates impacts in value added, not output, ensuring a direct welfare interpretation and producing results aligned with national accounts.

Together, these features make WAVE a transparent, empirically grounded, and versatile analytical framework.


# What WAVE can be used for  

Although initially applied to tariff shocks, the WAVE framework has much broader potential. It can evaluate:

- **Trade policies** such as tariffs, quotas, reshoring, and supply-chain diversification.
- **Climate and energy shocks**, including carbon border adjustments and fossil-fuel price changes.
- **Disaster and resilience scenarios**, where supply constraints interact with behavioural adjustments.
- **Macroeconomic transitions**, including global demand shifts and structural realignments.

WAVE's combination of behavioural responses and structural interdependence allows analysts to quantify which sectors and countries are most vulnerable, how shocks propagate, and where resilience can be strengthened.


# What we learn from the 2025 USA Tariffs

{% cite naqvi2025b %} applies the WAVE model to the U.S. tariffs introduced in September 2025. The analysis shows that global value added falls by roughly 0.52 percent, with indirect effects about twice as large as direct ones. Direct losses occur mainly in traded manufacturing—such as textiles, chemicals, and machinery—while the majority of global losses come from indirect contractions in services, including transport, telecommunications, finance, and public administration.

Small open economies like Ireland and Austria experience disproportionately large spillovers, and countries such as India, Pakistan, Nepal, and Vietnam face deep systemic losses due to their supply-chain integration. Notably, the United States itself loses around 3.2 percent of value added, as domestic price increases propagate through domestic production networks and reduce service-sector output. China, by contrast, experiences milder aggregate effects due to its large domestic market and strong intra-regional linkages.

These results highlight that global economic shocks must be understood as network phenomena, not bilateral interactions.




# The way forward  

The WAVE model introduced in {% cite naqvi2025a %} and {% cite naqvi2025b %} provides a foundation for a broad research agenda. Incorporating investment dynamics would enable long-term growth analysis. Adding employment coefficients would support labour-market modelling. Linking environmental satellite accounts would allow analysts to examine emissions, resource use, and sustainability transitions.

As global disruptions become more frequent and complex, WAVE offers a scalable, empirically grounded platform for understanding how shocks propagate, who is most affected, and where resilience can be strengthened within global value chains.

Its combination of behavioural elasticities and production-network modelling places WAVE at the frontier of quantitative policy analysis in an interconnected world.


