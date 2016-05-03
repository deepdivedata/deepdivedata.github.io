---
title: Beyond GDP – Measuring Well-Being of a Nation
---
![Test](/img/wellbeing.jpg "Test")
[Gross domestic product (GDP)](https://en.wikipedia.org/wiki/Gross_domestic_product) has always been seen as a key measure defining prosperity of a nation; however it is just indicates the economic performance of a nation and doesn’t take into account the well-being of the citizens. Is it justifiable to measure the success just based on economic performance? is money everything? are people really happy about their life and living conditions? Does GDP correlate with well-being. Let’s see what data has to say. There are plenty of well-being related indicators available from various data sources; for example, one can measure the well-being of citizens based on quality of life, education, basic facilities, work-life balance, overall happiness, gender equality, income, etc., I have outlined, below, the different categories that I considered to obtain normalized well-being score.
### Key Categories:

Basic human needs, Civic engagement & Governance, Community, Education, Employment, Health, Life satisfaction & Balance, Safety, Sustainability

For each categories, I researched different metrics and scored the category based on average of different indicators considered for each category. More data oriented details such as collection, data wrangling and transformation are provided later in the section. 
the interactive data visualization and play around a bit to see how well the nation is doing. Unfortunately, it was not possible to gather data for all countries so I considered only the OECD countries for my analysis. Below is the static version of the visualization.

![Test](/img/wellbeing2.png "Test")

### Some Analysis: 

Well-being doesn’t always correlate with GDP and some countries like the United States have huge issue of income inequality meaning the rich people consumes the majority of the wealth of the nation which indeed is not something one would hope for. Interestingly, Mexico had very low GDP but considerable score in well-being.

### Scandinavia – ideal model?

Scandinavian countries performed well in all the key measures. In particular, Norway had very high score in income equality and well-being as well as GDP suggesting it would be interesting to deep dive into the model and why they were able to do well in all aspects and of course unsurprisingly the country has consistently be ranked amongst the top 5 in reports such as “best countries to live in”, world happiness, etc.,

### Data Collection and Transformation:

Indicators for each category were collected from different sources that includes WHO, OECD, Worldbank, Yale, etc., the entire list of indicators used and its source is in this spreadsheet

All the indicators were standardized presented as a score out of 10. This is pretty easy for readability and ensure easy decoding  The quick steps are
1. Obtain the Z score (standardized) for each indicator as follows:

Z = (X – µ) / σ

where X represents the value to be converted, µ – mean of the population (countries in our case) and  σ being the standard deviation of the population
2. Standardized scores are converted into score out of ten using the formula:

Score10 = µ + (σ * Z score) ;  

Where µ = (0– 10 (Zmin / Zmax)) / (1 – (Zmin / Zmax))  and σ = (10 – µ) / Zmax


