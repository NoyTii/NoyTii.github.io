---
layout: post
title:  "Vehicle Theft in San Francisco (2003 - 2024)"
date:   2025-03-30 10:00:11 +0100
---

This project looks at vehicle theft in San Francisco from 2003 to 2024. The goal is to help the San Francisco Police Department (SFPD) better understand when and where these crimes happen, and to find ways to reduce them even more. We start by looking at theft patterns by the hour of the day, then identify which districts have higher theft rates. Finally, we use a map to highlight specific areas and streets where theft is more common.

A sharp drop in thefts after 2005 [(accessible in this article)](https://www.eastbaytimes.com/2007/02/16/car-thefts-decrease-statewide/) is likely due to the introduction of new technologies like "Bait Cars". This shows how technology can help reduce crime — and with better data, we can aim for even greater improvements.

We will have a look on the vehicle theft crimes by hour of the day per year, as described in the following plots.

## Hourly Crime Rate by Year

The average crime rate is indicated for each year. The blue bars represent hours that exceed the average (for better visibility zoom in 150% in your browser).

![Hourly Vehicle Theft](/assets/assignment2/visual1_hourly_crimes.png)

It looks like the hourly pattern is recurring every year as the number of vehicle theft crimes is increasing throughout the day. The above plot shows us the significant difference in vehicle theft crime by the hours. This allows us to better understand when these crimes are likely to occur. The blue bars represent hours that exceeded the hourly average per year. This is valuable, as SFPD can allocate more officers in those sensitive hours.

Showing the hourly crime is not enough per se. Since more cops demand more resources, which is not part of this analysis, we also need to provide SFPD with the districts that are suffering from vehicle theft crimes, and that is what we are going to investigate further!

## Hourly Crime Patterns Across Districts

With the following interactive chart it is way easier to see what district is best to look at for the SFPD.
SFPD can easily compare the number of crimes per hour accross all disctricts and see clear signs that some central district are in more need of enforcement than others. To observe and compare the data, start by clicking any district in the legend on the left hand side of the chart, it is possible to compare multiple districts:

<iframe
  src="/assets/assignment2/visual2_bokeh_crimes_district.html" 
  style="width: 100%; max-width: 700px; height: 600px; border: none; display: block; margin: 0 auto;">
</iframe>

According to the above plot, it appears that it is still mostly in the evening and night hours that vehicle theft most often happens. Some areas are clearly worse and some areas have very little vehicle theft incidents. The worst five districts are Ingleside, Bayview, Mission, Northern, and Taraval. The first 3 are significantly higher (more than 20%) than the latter, hence those districts should be first priority for SFPD.

We have seen evidence that precautions like cameras, drones, and more are among the new actions that SFPD is going to use in the future. [This article from NBC Bay Area](https://www.nbcbayarea.com/news/local/san-francisco/car-break-ins-san-francisco-2/3667342/) highlights how the city plans to tackle car break-ins with advanced technology.

To facilitate the city and SFPD with treating this problem we can drill further in, and consolidate the data that we have seen by now with an interactive map.


## Vehicle Theft Hotspots: Interactive Time-Based Map

The following interactive map highlights where vehicle thefts happen in San Francisco throughout the day. The animation cycles through each hour, showing how hotspots shift as time changes. Red areas indicate higher concentrations of thefts, helping SFPD target specific regions with precision. On the bottom left hand side of the chart, you can see the hour of the day. The horizontal scroll enables you to rewind or skip forward along the day:

<iframe 
  src="/assets/assignment2/visual3_folium_map.html" 
  style="width: 100%; max-width: 900px; height: 600px; border: none; display: block; margin: 0 auto;">
</iframe>


This plot wraps up our analysis by showing the exact locations of vehicle thefts across San Francisco. Building on the previous breakdowns by hour and by district, this map adds a detailed geographic view that highlights specific streets and areas with higher theft activity.

The colored dots on the map show where vehicle thefts have happened in San Francisco. Each dot represents a reported theft, and the color shows how often thefts happened in that area — red areas have more thefts, while yellow and green areas have fewer.


## Final Thoughts, Conclusion, and Further Analysis

This analysis indicates the importance of time and location. First, by analyizing the crime rate by time in each year, we could have a better grasp on which hours of the day are more sensitive to vehicle theft crimes. We could see that the last 8 hours of the day are prominent, therefore, law enforcement in SF by those hours will be a good idea.

Next, we dived into the location aspect of SF's vehicle theft crimes. We observed the areas that have the most vehicle theft crimes. And since resources are valuable and expenssive, SFPD can now focus more on the most outlawed districts, with the given time of the first section.

Lastly, by combining time-based patterns with spatial heatmap, SFPD can more easily identify not just when, but exactly where vehicle thefts are more likely to happen. This helps support more targeted patrols, or other surveillance such as street cameras or drones, resource planning, and long-term crime prevention efforts.

For further analysis it would be benificial for SFPD to look at the crime level throughout the calender year. Some days might have higher likelihood of vehicle theft that wasn't part of our analysis. This would help with identifying single days/weeks and districts of the city where the crime is abnormally high. They can then implement new governance technologies as spoken of earlier or more cops. With this they can focus their ressources way better and hopefully lower the crime levels even furhter.

