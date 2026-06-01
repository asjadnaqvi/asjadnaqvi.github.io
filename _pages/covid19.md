---
layout: page
title: COVID-19 tracker
permalink: /covid19/
description:
nav: false
display_categories: 
horizontal: false
---

This page summarizes the **COVID-19 European Regional Tracker** {% cite Naqvi2021 %}, a project developed to collect, clean, harmonize, and map sub-national COVID-19 case data across Europe.

During the first year of the pandemic, the core challenge for researchers, policymakers, and the public was not the absence of data, but the lack of comparable regional data across countries. Most European countries published COVID-19 case numbers, but they did so through different dashboards, administrative units, file formats, update schedules, and reporting standards. The tracker was built to turn these fragmented national reporting systems into a coherent regional dataset.

## What the Tracker Does

The paper introduces a harmonized dataset that follows the regional evolution of COVID-19 cases across **26 European countries** from the start of the pandemic through **November 2020**. Its main contribution is to organize daily regional case data into a common structure so that the spread of the pandemic can be compared across European regions rather than only across countries.

Where possible, the data are harmonized to the **NUTS 3 level**, the lowest comparable statistical geography used by Eurostat. For countries where NUTS 3 data were not available, the tracker uses the closest available spatial level. In the first release, **Poland and Greece** are included at the NUTS 2 level because of data limitations.

The dataset includes:

- cumulative COVID-19 cases,
- daily new cases,
- population,
- daily new cases per 10,000 population,
- regional identifiers based on the European NUTS classification,
- date-level observations for each region.

## Why Regional Data Matter

National COVID-19 statistics were useful for high-level monitoring, but they often concealed substantial regional variation. The pandemic did not spread evenly across countries. Early European outbreaks were concentrated in specific places, such as northern Italy and the Austrian ski resort of Ischgl, before spreading across the continent.

A regional dataset makes it possible to study:

- how infections diffused spatially over time,
- whether border closures and mobility restrictions affected regional spread,
- how urban, rural, and cross-border regions differed,
- where second-wave outbreaks were concentrated,
- how regional case intensity changed after adjusting for population.

The paper shows that the second wave in autumn 2020 was not simply a repetition of the first. Regional dispersion in daily cases per capita became much larger, indicating a more spatially widespread and uneven outbreak pattern.

## Data Challenges

The main difficulty is that European countries do not report regional COVID-19 data in a uniform way. Some countries publish clean downloadable files, while others rely on dashboards, PDFs, image-based maps, ArcGIS portals, or GitHub repositories maintained by public agencies or independent researchers.

The paper documents these differences country by country. For example:

- Austria provides district-level data below NUTS 3,
- Germany has high-quality regional data from the Robert Koch Institute,
- Italy provides well-documented data through an official GitHub repository,
- Greece releases regional information mainly through PDFs,
- Estonia reports case ranges for privacy reasons, requiring midpoint approximations,
- Switzerland relies partly on independently compiled cantonal data,
- the United Kingdom is treated as separate country systems because England, Scotland, Wales, and Northern Ireland use different reporting infrastructures.

This heterogeneity is precisely what makes the tracker useful. It converts fragmented national data systems into a comparable European regional dataset.

## Methodological Approach

The tracker maps country-specific reporting units to the European **NUTS 2016 regional classification**. This makes regional COVID-19 data comparable across countries, even when the original data are reported using national administrative units.

The workflow includes:

1. collecting raw data from official or official-derived sources,
2. cleaning and standardizing country-level files,
3. mapping national regions to NUTS regions,
4. merging country files into one European master dataset,
5. calculating daily cases and population-normalized case rates,
6. producing maps and visualizations of the regional spread of COVID-19.

The paper is also explicit about the underlying limitations. Regional boundaries sometimes change, some countries do not provide exact NUTS-level data, and several sources contain reporting lags or retrospective corrections. These issues are documented rather than hidden, making the tracker useful not only as a dataset but also as a guide to the quality and comparability of European regional COVID-19 data.

## Open Data and Replication

A major strength of the project is that it is fully reproducible. The raw files, cleaned files, Stata code, GIS files, processed master dataset, and maps are made available online.

The main repository for the project is [COVID-19 European Regional Tracker](https://github.com/asjadnaqvi/COVID19-European-Regional-Tracker).

The repository contains the complete workflow, including country-specific scripts and master files. The project was also released through Zenodo under a Creative Commons Attribution 4.0 International license, making it easier for others to reuse, audit, and extend the data.

## What the Tracker Contributes

The COVID-19 European Regional Tracker contributes in three main ways.

First, it provides a **harmonized regional dataset** at a much finer spatial scale than standard country-level COVID-19 databases.

Second, it documents the **data infrastructure behind pandemic monitoring** in Europe, showing which countries had accessible, machine-readable, and regionally detailed data, and which relied on less transparent or harder-to-process formats.

Third, it supports **spatial and policy analysis** by making it easier to compare regional outbreaks, identify hotspots, and examine the relationship between COVID-19 spread, population, borders, and containment measures.

## Conclusion

The COVID-19 pandemic generated an extraordinary amount of public data, but much of it remained fragmented across national systems. The COVID-19 European Regional Tracker was designed to make this information comparable across European regions.

By harmonizing daily regional case data for 26 countries, the tracker provides a foundation for studying the spatial dynamics of the pandemic in Europe. More broadly, it highlights a general lesson for crisis monitoring: data availability alone is not enough. Data must also be accessible, comparable, documented, and reproducible.

The project shows how open data, transparent code, and regional harmonization can improve our understanding of how crises unfold across space.
