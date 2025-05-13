---
layout: post
title:  "NYC Motor Vehicle Crash Analysis"
date:   2025-05-12 10:00:11 +0100
---

Every day in every city, traffic accidents impact on our lives. This project analyzes detailed data from the [NYC Open Data webpage](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95/about_data), covering motor vehicle collisions in New York City from 2013 to 2024.  By studying the datasets’ patterns, we aim to uncover insights that can help reduce accidents and save lives.

A link to the full notebook and dataset can be found [here (zip file)](/assets/FinalProject/Final_notebook.zip)

### NYC Vision Zero

Our analysis supports the [Vision Zero initiative](https://en.wikipedia.org/wiki/Vision_Zero_(New_York_City)#:~:text=Vision%20Zero%20is%20a%20program,York%20City%20streets%20by%202024.), a citywide effort launched in 2014 with the bold goal of eliminating all traffic-related deaths and serious injuries. With limited resources like patrol officers and traffic cameras, it's important to focus efforts where they’re needed most. This analysis helps answer questions such as: Are crashes more likely at certain times of day or in specific neighborhoods? What are the most common causes of severe accidents? By addressing these questions, we aim to provide practical, data-driven recommendations to help city planners, law enforcement, and public safety officials make New York City streets safer for everyone.

## Temporal Analysis: When Do Accidents Occur?

Generally, the data contained nearly 2M rows over 12 years. 24% of the accidents involved injuries, while 0.15% involved dead. When analyzing the accidents by boroughs, Queens was the leading borough, followed by Brooklyn, and Bronx. In this section, we will focus on the temporal analysis of our data.

In the following bar chart, one can observe the development of NYC accidents over the years, and the number of accidents over the hour of the day – which provides the general pattern of daily accidents around the city.


![Accidents by Year and Hour](/assets/FinalProject/accidents_Year_hour_chart.png)

When examining the accidents (y-axis) over the years (x-axis), the number of accidents is steadily growing from 2013 to 2019. Then in 2020 we observed a sharp decrease, and a steady decrease henceforth. While the decrease in 2020 and 2021 can be explained by the Covid-19 pandemic, the decline over the past 3 years is credited for the [record investment in streets safety (link)](https://www.nyc.gov/office-of-the-mayor/news/189-25/mayor-adams-traffic-deaths-reach-historic-low-during-first-quarter-2025-additional#:~:text=In%202024%2C%20there%20were%20252,the%20safest%20year%20since%202019.) like pedestrian and cyclists’ safety, safer intersections, 24/7 speed cameras, and red-light cameras.

Accidents by hour (Y-axis and X-axis respectively) show a clear pattern, with sharp increases between 6–8 AM and a peak around 5 PM, likely due to rush hour traffic and driver fatigue later in the day. But this raises further questions: how are accidents spread across the days and months of the year? Are certain times of year more accident-prone than others?

![Accidents Calendar](/assets/FinalProject/accidents_calendar_heatmap.png)

In the above calendar chart, we can observe the number of accidents per day across all months of the year. The color saturation gradients between the yellow color (high rate of accidents) and the purple color (low rate of accidents). We can observe the months that have fewer accidents (Jan-Apr) than the rest of the year. Additionally, we can observe certain holidays like 4th of July and Christmas have much fewer accidents. A further examination of the accidents led us to create the same calendar chart, focused on injuries:

![Injuries Calendar](/assets/FinalProject/Injuries_calendar_heatmap.png)

We can observe the same pattern of less injuries in the first four months of the year, and more throughout the rest of the year. Another interesting insight is that during holidays, especially the 4th of July, the injuries are at the same level as the rest of the month even though it has half of the number of accidents. Christmas also underlies the same pattern, on a lower scale. These charts enable us to allocate resources into more specific times of the year.

## From Accidents to Sevirity - Causal Analysis: Why Do Accidents Occur?

Continuing the injury calendar chart, one key observation that we found in the temporal analysis can be found in the following line charts:

![# By Hour of the Week](/assets/FinalProject/hour_of_the_week_line_chart.png)

The charts above show the number of crashes, injuries, and fatalities in NYC by hour of the week (from Monday 12 AM to Sunday 11 PM). The x-axis represents each hour of the week, while the y-axis shows the total incidents.  We observe a clear daily pattern in crashes and injuries, with peaks during morning and evening rush hours, around 6–8 AM and 5 PM, reflecting increased traffic volume during rush hours. This regularity suggests that traffic density plays a significant role in the likelihood of accidents and injuries.

However, the fatalities plot reveals a different and more concerning insight: although crashes and injuries drop over the weekend, the number of deaths increases. This suggests weekend collisions tend to be more severe, possibly due to factors like higher speeds or impaired driving. This insight highlights a need for targeted safety measures during weekend hours.

This led us to explore the causes of accidents. We found that driver inattention or distraction is the leading factor. Based on the earlier weekend trend, we also identified several causes that spike on weekends, including alcohol involvement, passenger distraction, ignoring traffic signals, speeding, and improper turns. This raised the next key question: what are the deadliest contributing factors?


![# Dead VS. Rate](/assets/FinalProject/no_of_d_vs_rate.png)

In the above chart we filtered the data to accidents that involve at least one dead. The bars indicate the number of death persons on the left Y-axis per contributing factor in the X-axis. Additionally, we calculated the death rate for each of the top 10 contributing factors. The death rate represents the proportion of deaths per number of accidents that were contributed by a factor. Then we get a different story.

Illness is the deadliest factor among the top 10 factors for accidents followed by unsafe speed, pedestrian\bicyclist error, and disregarded traffic control. We also examined the death rate by vehicle type, and found that in the context of death-rate, two-wheelers, like motor bikes, scooters and bicycles were always in the top. 


## Spatial Analysis: Where are the accidents occur?

In the last section of this analysis, we will introduce an interactive map chart that can be filtered (the filter is on the top tight part of the chart) to three categories: accidents with no injuries and no dead, accidents with injuries only, and any accident that involved at least one dead:

<iframe 
  src="/assets/FinalProject/nyc_accidents_heatmap.html" 
  style="width: 100%; max-width: 900px; height: 600px; border: none; display: block; margin: 0 auto;">
</iframe>

This chart can be used for the sake of city planners, law enforcement, and public safety officials. To utilize this chart, the authorities can find the hotspots of each category of accident and fill the area with the right enforcements’ tools. 

In other words, this chart is mostly meant for further analysis or future decision making regarding resource allocation.

## Summary & Conclusion

This project provides a comprehensive, data-driven exploration of motor vehicle collisions in New York City from 2013 to 2024. By examining the data temporally, causally, and spatially, we've uncovered key insights that can inform policy, enforcement, and public awareness efforts.

**Key findings:**
- A steady rise in accidents until 2019, followed by a decline likely due to both the COVID-19 pandemic and subsequent Vision Zero investments in infrastructure and enforcement.
- Clear daily and weekly accident patterns, with peaks during weekday rush hours and a concerning rise in fatalities during weekend hours.
- Holidays like Christmas and the 4th of July show significantly fewer accidents, but injury rates remain comparable, highlighting a change in accident severity rather than volume.
- The most lethal contributing factors include illness, unsafe speed, pedestrian or cyclist error, and disregarding traffic controls, all pointing to the importance of targeted education and enforcement.
- Two-wheel vehicles (motorcycles, scooters, bicycles) consistently appear among the highest in death rate per accident.
- The interactive spatial analysis empowers decision-makers to visually locate accident hotspots by severity, supporting focused interventions.

## Further Analysis & Recommendations

This study opens the door to even deeper investigation and real-world applications:

1. Apply machine learning to predict high-risk times and locations using historical data, weather, and traffic patterns.
2. Simulate the potential effects of policy interventions, like lowering speed limits or increasing weekend enforcement, using technological control methods such as red-light, speed, and [AI-Based cameras](https://www.bbc.com/news/articles/cged890y27wo) to detect drivers on the phone.
3. Raise the effect of public awareness campaigns on reducing crashes at high-risk times or locations.


