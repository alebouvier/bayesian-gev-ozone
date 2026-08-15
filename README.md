# Bayesian Modeling of Extreme Ozone Concentrations

This project focuses on the statistical modeling of maximum ozone concentrations in Lombardy using meteorological covariates.

## Overview

Air pollution is a major environmental and public health in which ozone plays a particularly important role due to its harmful effects on human health, vegetation, and ecosystems.

The main scientific objective of this project is to understand how meteorological conditions influence extreme ozone concentrations and to develop a bayesian statistical model capable of capturing this relationship in a reliable and interpretable way.

## Method

This project focuses on modeling weekly maximum ozone levels observed at different monitoring stations.

It relies on extreme value theory within a Bayesian framework through the use of the Generated Extreme Value (GEV) distribution. More precisely, we adopt a  quantile-based reparametrization of this distribution and penalized complexity priors.

The GEV distribution depends on 3 parameters: the location, the spread and the tail.

3 differents models were fitted using the INLA framework:
  - a temporal model
  - a heteroskedastic model
  - a hybrid model

A comparison between INLA and STAN implementation have also been conducted.

## Data

We worked with the Arpa Lombardia dataset to obtain weekly ozone maximums for 51 monitoring stations throughout Lombardy from 2018 to 2024.

The following weekly meteorogical covariates were collected from Open-Meteo for each monitoring station:
  - Maximum temperature at 2m
  - Minimum temperature at 2m
  - Total weekly precipitation
  - Maximum wind speed at 10m

## Results

### Temporal model

In this model, the location parameter shows a linear component for the meteorogical covariates and the year and cyclic second-order random walk for the monthly seasonal component. The spread and tail parameters are covariates free



## Credits

Academic project conducted for the Bayesian Statistics course 2025/2026 at Politecnico di Milano.

Authors:
  - Luca Binaghi
  - Alexandre Bouvier
  - Benoît Caron
  - Maxime Dabout
  - Adam Lerondel-Touzé
  - Elias Ramili

Supervisers:
  - Simone Colombara
  - Giulio Beltramin
