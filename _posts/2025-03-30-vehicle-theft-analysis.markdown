---
layout: post
title:  "Vehicle Theft in San Francisco (2003 - 2024)"
date:   2025-03-30 10:00:11 +0100
---

This project looks at vehicle theft in San Francisco from 2003 to 2024. The goal is to help the San Francisco Police Department better understand when and where these crimes happen, and to find ways to reduce them even more. We start by looking at theft patterns by the hour of the day, then identify which districts have higher theft rates. Finally, we use a map to highlight specific areas and streets where theft is more common.

A sharp drop in thefts after 2005 is likely due to the introduction of engine immobilizer systems in newer cars. This shows how technology can help reduce crime — and with better data, we can aim for even greater improvements.

We will have a look on the vehicle theft crimes by hour of the day per year, as described in the following plots.

## Hourly Crime Rate by Year

The average crime rate is indicated for each year. The blue bars represent hours that exceed the average.

![Hourly Vehicle Theft](/assets/assignment2/visual1_hourly_crimes.png)

It looks like the hourly pattern is recurring every year as the number of vehicle theft crimes is increasing throughout the day. The above plot shows us the significant difference in vehicle theft crime by the hours. This allows us to better understand when these crimes are likely to occur. The blue bars represent hours that exceeded the hourly average per year. This is valuable, as SFPD can allocate more officers in those sensitive hours.

Showing the hourly crime is not enough per se. Since more cops demand more resources, which is not part of this analysis, we also need to provide SFPD with the districts that are suffering from vehicle theft crimes, and that is what we are going to investigate further!

## Hourly Crime Patterns Across Categories

<iframe
  src="/assets/assignment2/visual2_bokeh_crimes.html" 
  style="width: 100%; max-width: 700px; height: 600px; border: none; display: block; margin: 0 auto;">
</iframe>

This interactive chart allows you to explore crime patterns across different categories by hour. Use the legend to toggle each crime type and uncover when activity peaks across San Francisco.

## Vehicle Theft Hotspots: Interactive Time-Based Map

<iframe 
  src="/assets/assignment2/visual3_folium_map.html" 
  style="width: 100%; max-width: 900px; height: 600px; border: none; display: block; margin: 0 auto;">
</iframe>


This interactive map highlights where vehicle thefts happen in San Francisco throughout the day. The animation cycles through each hour, showing how hotspots shift as time changes. Red areas indicate higher concentrations of thefts, helping SFPD target specific regions with precision.

This plot wraps up our analysis by showing the exact locations of vehicle thefts across San Francisco. Building on the previous breakdowns by hour and by district, this map adds a detailed geographic view that highlights specific streets and areas with higher theft activity.

The colored dots on the map show where vehicle thefts have happened in San Francisco. Each dot represents a reported theft, and the color shows how often thefts happened in that area — red areas have more thefts, while yellow and green areas have fewer.

By combining time-based patterns with this spatial heatmap, the San Francisco Police Department can more easily identify not just when, but exactly where vehicle thefts are more likely to happen. This helps support more targeted patrols, or other surveillance such as street cameras or drones, resource planning, and long-term crime prevention efforts.

