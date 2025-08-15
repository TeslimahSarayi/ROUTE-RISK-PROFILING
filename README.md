# ROUTE-RISK-PROFILING-INSIGHTS-AND-STRATEGIC-IMPLICATIONS
This repository contains a Python project developed to segment the 65 travel routes of the UK National Rail according to their likelihood of service disruption  

## PROJECT OVERVIEW 

As part of the broader [Rail Service Analysis Project](https://github.com/TeslimahSarayi/NATIONAL-RAIL-SERVICE-ANALYSIS), this segment applies machine learning to segment the 65 travel routes by operational risk. To help uncover route-level performance insights, the clustering model considers three performance indicators, delay percentage, cancellation percentage and average ticket price.  

This delivers value across multiple business areas:  

**Operations**: Pinpoints high-risk routes with recurring delays and cancellations, enabling focused operational improvements where they are needed most.

**Customer Experience** : Identifies routes with consistent disruptions, helping mitigate passenger dissatisfaction, manage expectations, and prioritise service quality.  

**Strategic Planning**: Supports data-driven resource allocation, from staffing to maintenance, based on the reliability and cost-efficiency of each route cluster. 

**Revenue & Pricing**: Highlights opportunities for price reviews on expensive but reliable routes and margin optimisation on affordable but disruption-prone routes. 

**Scalability**: The clustering model can be refreshed monthly or quarterly to monitor shifting trends, route improvements, or new problem areas.  
## CLUSTERS AND THEIR INTERPRETATION

Unsupervised cluttering (kMeans) were used to segment the routes into 3 and were labelled as : 

**High Risk Routes** : Characterised by high delay rates despite low cancellations. These routes also tend to have above-average ticket prices.  
**Moderate Risk Routes** : Represent the majority. They are relatively affordable and exhibit lower levels of disruption.  
**Reliable But Expensive Routes**: Offer consistent reliability but may present pricing concerns due to significantly higher average fares  

Frequency distribution of clusters and summary of their performance indicators
Cluster |Number Of Routes|  Delay %| Cancellation % | Average ticket price
|:------------:|:-----------------:|:----------:|:-------------:|:---------------:|
High Risk Route |  5 |  88 |  1.80 |  58.12
Moderate Risk Route |   48    |    3.69    |    4.69    |17.08
Reliable But Expensive Route  |   12   |    4.00    |    2.17    |    84.11  

See the notebook for a detailed step-by-step walkthrough of the clustering methodology and route analysis process

## KEY INSIGHTS AND RECOMMENDATIONS
* The following routes are high risk due to their 88%  average delay rates, despite their low cancellation percentages. Targeted operational interventions are recommended:

   1. Edinburgh Waverley⇒London Kings Cross
   2. York⇒Wakefield
   3. Manchester Piccadilly⇒London Euston
   4. Liverpool Lime Street⇒London Euston
   5. London Euston⇒York
* Moderate risk routes make up over 70% of the total network and present an opportunity for margin improvement. With an average fare of £17.08, these routes are candidates for **strategic price optimisation** that will directly enhance profitability
* Reliable but expensive routes have low disruption rates but charge an average fare of £84.11, which may discourage repeat usage. A price review could help reduce potential churn risk.

## CONCLUSION
This route profiling model allows the National Rail to shift from reactive issue resolution to proactive data-driven network strategy. By clustering routes based on reliability and cost, we can prioritise improvements, enhance customer satisfaction, and allocate resources more effectively as the network evolves. 

