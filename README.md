# Master Thesis
Github repository for the master thesis

# Federated Learning for Emergency Management: A Privacy-Preserving City Digital Twin Framework for Pandemic Response

**Author:** Emrecan Yerlikaya

**1st Examiner:** Prof. Dr. Steffan Lessmann

**1st Examiner:** Prof. Dr. Daniel Klapper

An Overview of the FL Framework:

![FL Framework](Figures/FL_arc.png)

## Table of Contents

- [Summary](#Summary)
- [Working with the Repo](#Repo)
- [Results](#Results)
- [Project structure](#structure)

## Summary

The Coronavirus pandemic (COVID-19) has become one of the most devastating health crises in modern times, causing significant loss of life, economic slowdown, and disruptions worldwide. Authorities around the globe have failed to develop data-driven and coordinated policy response measures, further exacerbating the spread of the virus. Several studies in the literature have used Federated Learning (FL) and City Digital Twin (city DT)s to address these challenges. However these mostly focused on different regions within a country and lacked cross-country context which is especially important for a rapidly spreading global pandemic. In this thesis we address this challenge by proposing a privacy-preserving framework for emergency management based on FL and city DT using data from 30 EU/EEA countries. The framework enables multiple countries to collaboratively train a shared epidemic forecasting model without centralizing sensitive health data. Utilizing a Long Short-Term Memory (LSTM)-based time-series model, we conducted a series of simulations to assess the framework’s performance against isolated local model training and a hypothetical centralized model. Moreover we also utilize vaccination and testing data which holds important information regarding pandemic dynamics. Our results suggest that while FL struggles from high data heterogeneity and client drift, the performance improves significantly when the countries are grouped into more homogenous clusters. We also demonstrate the trade-off between model performance and privacy preservation by comparing the performance result of the hypothetical centralized model with that of FL.

## Working with the Repo

Several studies have confirmed that city DTs can make important contributions in enhanced situation assessment, decision making, coordination, and resource allocation during rapidly evolving disaster situations. For instance, in one of the studies, Fan et al. proposed a novel city DT framework with deep learning techniques and explained advantages in emergency response management (Fan et al., 2021).

Our research proposal is inspired by the paper from (Pang et al., 2020), who developed a collaborative city digital twin model using federated learning to address the challenges of COVID-19 pandemic response. The authors used daily epidemic data (The COVID tracking project dataset) and state-level policy responses (The Coronavirus State Actions Dataset) in the United States to build city Digital Twins. In the proposed framework, each state was considered as a client node in the federated paradigm with its own local data. The findings suggest that federated city DTs perform much better than the non-federated approach, indicating that individual DTs benefit from collaboration and learn from each other.

## Results

This research aims to build on the pioneering work by Pang et al. and implement it in the European context. While Pang et al. focused on US states, this study implements a collaborative city DT framework where 30 individual countries in Europe will be considered as client nodes in the federated framework. Europe’s unique geopolitical context provides an interesting setting since it consists of sovereign countries with much more divergent national regulatory frameworks, healthcare infrastructure, and unique political arrangements such as the Schengen agreement.

Moreover, in this study we would like to consider other important variables which might have an important effect on the severity of the epidemic such as weather conditions, vaccination/test rates, share of vulnerable (elderly) people in the population, average number of cases/deaths in neighboring countries, whether the country is in the Schengen Area, population concentration per km2, recovered/active cases and etc. To the best of our knowledge, these important variables were not included in previous studies.

## Project Structure

Among others, the two main datasets that will be used in this study are:

*   John Hopkins University - CSSE Covid 19 Daily Reports on daily number of cases, deaths, recoveries, and active cases.
*   European Centre for Disease Prevention and Control Data on country response measures to COVID-19.

In the FL architecture, each client node will use an `LSTM` model to produce forecasts given historical data on the epidemic, corresponding policy responses, weather conditions, etc. Here `LSTM` models are preferred for their ability to model long-term dependencies, and their proven success in forecasting Covid-19 pandemic trajectory in the literature (Yang et al., 2020).
