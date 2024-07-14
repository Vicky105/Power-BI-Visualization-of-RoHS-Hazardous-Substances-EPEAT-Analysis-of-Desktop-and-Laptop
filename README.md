# Power-BI-Visualization-of-RoHS-and-EPEAT-Analysis-of-Desktop-and-Laptop
![Dashboard Image](https://github.com/Vicky105/Power-BI-Visualization-of-RoHS-Hazardous-Substances-EPEAT-Analysis-of-Desktop-and-Laptop/blob/2f49e40a8c42fcd380ca50925d5b30b7b595eb10/Navigation%20Page.png)
<br>
![Dashboard Image](https://github.com/Vicky105/Power-BI-Visualization-of-RoHS-Hazardous-Substances-EPEAT-Analysis-of-Desktop-and-Laptop/blob/2f49e40a8c42fcd380ca50925d5b30b7b595eb10/EPEAT-Analysis.png)
![Dashboard Image](https://github.com/Vicky105/Power-BI-Visualization-of-RoHS-Hazardous-Substances-EPEAT-Analysis-of-Desktop-and-Laptop/blob/2f49e40a8c42fcd380ca50925d5b30b7b595eb10/Desktop%20vs%20Laptop.png)

## Table of Contents
* [Introduction](#introduction)
* [Data Sources](#data-sources)
* [Data Dictionary](#data-dictionary)
* [Major KPI's](#major-kpis)
* [Key Findings](#key-findings)
* [Tools Used](#tools-used)
* [Conclusion](#conclusion)

## Introduction
This project analyzes the EPEAT scores, EPEAT Tier of European countries and four major manufacturers of desktops and laptops (HP, Dell, Acer, and ASUS). Additionally, the project compares the EPEAT scores of desktops and laptops to determine which is more hazardous to the environment with respect to Directive 2002/95/EC.<br>
EPEAT TIER:<Br>
BRONZE - Products that meet all required criteria and achieve less than 50% of the optional points <br>
SILVER - Products that meet all required criteria and achieve 50 - 74% of the optional points <br>
GOLD - Products that meet all required criteria and achieve 75 - 100% of the optional points <br>

## Data Sources
* Hazardous substances data according to Directive 2002/95/EC - BOM_RoHS View
* EPEAT data can be accessed from this link [EPEAT DATASET](https://www.epeat.net/search-computers-and-displays) - EPEAT_EUROPE

## Data Dictionary

### BOM_RoHS View

| Column Name | Description | Data Type |
|-------------|-------------|-----------|
| component_id | Unique identifier for the component | INT |
| component_name | Name of the component | VARCHAR(100) |
| in_desktop | Indicates if the component is used in desktops | BIT |
| in_laptop | Indicates if the component is used in laptops | BIT |
| substance_name | Name of the RoHS restricted substance | VARCHAR(100) |
| rohs_limit | EU RoHS limit for the substance | DECIMAL(5,4) |
| hazard_classification | Classification of the hazard | VARCHAR(100) |
| potential_alternatives | Potential alternatives for the substance | TEXT |

### EPEAT_EUROPE Table

| Column Name | Description | Data Type |
|-------------|-------------|-----------|
| id | Unique identifier for the product | INT |
| manufacturer | Name of the manufacturer | VARCHAR(50) |
| product_name | Name of the product | VARCHAR(100) |
| product_type | Type of product (e.g., laptop, desktop) | VARCHAR(50) |
| EPEAT_Score_out_of_49 | EPEAT score out of 49 points | INT |
| EPEAT_TIER | EPEAT tier (Bronze, Silver, Gold) | VARCHAR(10) |
| registered_on | Date of registration | DATE |

## Major KPI's
* Primary KPI's - Products Count in Each Country vs Average EPEAT Score
* Primary KPI's - Average EPEAT score of Manufacturers by Desktop and Laptop
* Secondary KPI's - No of hazardous Substance in Laptops and Desktops
* No of products Registered by each manufacturer between 2020 to 2024
* Manufacturers and Countries vs No of Golden Tiers
* Hazardous substance and thier alternatives
* Top 3 Electrical Component by Count of Hazardous Substance Present in it.

## Key Findings
* Components used in Desktop having more hazardous elements than Laptops
* The manufacturers and countries with the highest average EPEAT scores are based only on laptops, not desktops. This illustrates that desktops have a lower average score due to the presence of more hazardous substances.
* HP has registered the most products and has the highest number of Gold tier products, resulting in the highest average EPEAT score
* Ireland is Having Highest Average EPEAT Score
  
## Tools Used
* Excel for initial data cleaning
* SQL for data cleaning and EDA(Exploration)
* Power BI for visualization
* [Cyberpunk Generator](https://deepai.org/machine-learning-model/cyberpunk-generator) for Background image

## Conclusion
This project provides valuable insights into the environmental impact of desktops and laptops based on their EPEAT scores and the presence of hazardous substances. The analysis shows that desktops tend to have more hazardous substances compared to laptops, affecting their overall EPEAT scores. HP stands out with the highest number of registered products and the highest average EPEAT score. This study emphasizes the importance of EPEAT analysis for products by each manufacturer and highlights the need to improve the sustainability of their products.
