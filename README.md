# Master Thesis
Github repository for the master thesis

# Federated Learning for Emergency Management: A Privacy-Preserving City Digital Twin Framework for Pandemic Response

**Author:** Emrecan Yerlikaya

## Introduction

Since 2019, the outbreak of the COVID-19 pandemic has caused more than 7 million confirmed deaths and around 770 million confirmed cases worldwide (Mathieu et al., 2024). Policymakers and governments around the world have implemented various measures to curb the transmission of the virus, ranging from full and partial lockdowns and travel restrictions to vaccination campaigns. However, the effectiveness of these measures often relies on timely and coordinated implementation, a significant challenge during unexpected and novel epidemics where policy makers lack historical data and experience. The rapid spread of the epidemic often outpaces the ability of policymakers to come up with real-time, data-driven policies for an optimal response. Moreover, fragmented policies, privacy concerns, and protective privacy regulations further exacerbate the issue.

To overcome these challenges, the city digital twins (city DTs) offer a promising solution by building a virtual replica of the actual urban systems. In emergency/disaster management, city DTs are found to be especially useful in providing a city information model and situational awareness for city management (Shahat et al., 2021). However, traditional digital twin architectures often depend on centralized data aggregation, which incentivizes local authorities to build isolated city DTs due to privacy concerns and protective regulations. This means that individual DTs cannot learn from each other’s experiences and form isolated data islands. At that stage, federated learning (FL) makes it possible to bridge seperate city DTs and collaboratively learn from decentralized data, without violating privacy regulations. By considering each city DT as a client node in the FL architecture, the individual DTs can benefit from experiences of others.

## Related Works

Several studies have confirmed that city DTs can make important contributions in enhanced situation assessment, decision making, coordination, and resource allocation during rapidly evolving disaster situations. For instance, in one of the studies, Fan et al. proposed a novel city DT framework with deep learning techniques and explained advantages in emergency response management (Fan et al., 2021).

Our research proposal is inspired by the paper from (Pang et al., 2020), who developed a collaborative city digital twin model using federated learning to address the challenges of COVID-19 pandemic response. The authors used daily epidemic data (The COVID tracking project dataset) and state-level policy responses (The Coronavirus State Actions Dataset) in the United States to build city Digital Twins. In the proposed framework, each state was considered as a client node in the federated paradigm with its own local data. The findings suggest that federated city DTs perform much better than the non-federated approach, indicating that individual DTs benefit from collaboration and learn from each other.

## Research Objectives

This research aims to build on the pioneering work by Pang et al. and implement it in the European context. While Pang et al. focused on US states, this study implements a collaborative city DT framework where 30 individual countries in Europe will be considered as client nodes in the federated framework. Europe’s unique geopolitical context provides an interesting setting since it consists of sovereign countries with much more divergent national regulatory frameworks, healthcare infrastructure, and unique political arrangements such as the Schengen agreement.

Moreover, in this study we would like to consider other important variables which might have an important effect on the severity of the epidemic such as weather conditions, vaccination/test rates, share of vulnerable (elderly) people in the population, average number of cases/deaths in neighboring countries, whether the country is in the Schengen Area, population concentration per km2, recovered/active cases and etc. To the best of our knowledge, these important variables were not included in previous studies.

## Methodology

Among others, the two main datasets that will be used in this study are:

*   John Hopkins University - CSSE Covid 19 Daily Reports on daily number of cases, deaths, recoveries, and active cases.
*   European Centre for Disease Prevention and Control Data on country response measures to COVID-19.

In the FL architecture, each client node will use an `LSTM` model to produce forecasts given historical data on the epidemic, corresponding policy responses, weather conditions, etc. Here `LSTM` models are preferred for their ability to model long-term dependencies, and their proven success in forecasting Covid-19 pandemic trajectory in the literature (Yang et al., 2020).

## Expected Contributions

*   Extending FL-based city DTs to Europe's diverse geopolitical context, addressing sovereign nations with varying regulations.
*   Incorporating novel variables (weather, vaccination rates, demographics, etc.) to improve epidemic forecasting accuracy.
*   Demonstrating the effectiveness of federated learning in maintaining privacy while enabling cross-border collaboration as a solution to the isolated data island problem.
*   Providing a framework for real-time, data-driven policy decisions during pandemics, considering both local and regional factors.

## References

*   Fan, C., Zhang, C., Yahja, A., & Mostafavi, A. (2021). Disaster City Digital Twin: A vision for integrating artificial and human intelligence for disaster management. *International journal of information management*, 56, 102049.
*   Mathieu E, Ritchie H, Rodés-Guirao L, Appel C, Giattino C, Hasell J, et al. (2020–2024). "Coronavirus Pandemic (COVID-19)". *Our World in Data*. Retrieved 24 February 2025.
*   Pang, J., Huang, Y., Xie, Z., Li, J., & Cai, Z. (2021). Collaborative city digital twin for the COVID-19 pandemic: A federated learning solution. *Tsinghua science and technology*, 26(5), 759-771.
*   Shahat, E., Hyun, C. T., & Yeom, C. (2021). City digital twin potentials: A review and research agenda. *Sustainability*, 13(6), 3386.
*   Yang, Z., Zeng, Z., Wang, K., Wong, S. S., Liang, W., Zanin, M., & He, J. (2020). Modified SEIR and AI prediction of the epidemics trend of COVID-19 in China under public health interventions. *Journal of thoracic disease*, 12(3), 165.
