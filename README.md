# Cricket Analytics: Unveiling Insights from the 2022 T20 World Cup Data

[Dashboard Link](https://app.powerbi.com/view?r=eyJrIjoiNjhlOWNlNjUtNThiMi00MDVjLTg5YmMtNDY3MTI1NzAzYWRiIiwidCI6IjAzMWEzYmJjLWNmN2MtNGUyYi05NmVjLTg2NzU1NTU0MGExYyJ9)

## Problem Statement
As part of the Analytics Vidhya Hackathon Practice Event, I tackled the intriguing task of analyzing data from the 2022 Cricket T20 World Cup. The dataset was scraped from the official Cricbuzz website. My job consisted of several tasks, including preprocessing diverse datasets, conducting exploratory data analysis (EDA), constructing a comprehensive and interactive Power BI dashboard, and ultimately deriving the optimal 11-player team based on various performance parameters.

The players for the ideal team are categorized into five distinct roles: Openers/Power Hitters, Anchors/Middle Order, Finishers, Allrounders/Lower Order, and Pacers/Fast Bowlers. 

## Data Description
The project involved the extraction and preprocessing of cricket data from the official Cricbuzz website using JavaScript codes. The resulting datasets were stored in JSON files (which were provided in case of any difficulty writing JavaScript codes), providing a foundation for further analysis. I had to convert these JSON files into Pandas Data Frames, preprocess the data, and transform them into CSV files for enhanced usability. The distinct CSV files and their contents include:

* t20_wc_match_results.csv: Contains details about match outcomes, participating teams, match dates, and unique match IDs.
* t20_wc_batting_summary.csv: Encompasses individual batsmen's performances in each match, including information on dismissals by specific bowlers.
* t20_wc_bowling_summary.csv: Provides insights into the performance of each bowler in every match, detailing batsmen dismissed and relevant match information.
* dim_players.csv: Features comprehensive player profiles, complete with photos, batting/bowling styles, and concise descriptions.

To enhance analysis in Power BI, I added a common column for seamless dataset integration. This laid the groundwork for creating an informative dashboard.

## Performance Metrics - DAX Measures and Calculated Columns
We were provided with specific criteria for each cricket role, such as power hitters needing a good strike rate and boundary percentage, and pacers requiring excellent economy and bowling strike rates. For a balanced selection of allrounders, a combination of both factors was considered. The constraints for each role can be found [here](https://github.com/praneeth377/Cricket_T20WC_Best_11-Data_Analysis/blob/master/Paramaeter%20Scoping.pdf). 

To adhere to these constraints, I implemented DAX measures for each parameter. The detailed list of DAX measures and calculated columns can be found [here](https://github.com/praneeth377/Cricket_T20WC_Best_11-Data_Analysis/blob/master/DAX%20Measures%20and%20Calculated%20columns.xlsx).

Once the measures were correctly implemented, I proceeded to create an interactive dashboard.

## Interactive Dashboard
I designed five tabs, each dedicated to a specific cricket role. In these tabs, detailed crosstabs display player and team information along with key performance metrics such as batting average, strike rate, boundaries, boundary percentage, bowling average, economy, wickets, dot ball percentage, and maidens. Each tab adheres to specific constraints applied as filters. Following the tables, area charts illustrate the performance parameters of each player throughout the tournament. Additionally, scatter plots depict relationships between strike rates and batting averages for batters, and economy versus bowling strike rates for bowlers.

In the pursuit of the ultimate goal, selecting the best 11, a dashboard is linked to all the tabs mentioned earlier. A filter is incorporated on the side of the dashboard, allowing us to handpick the best 11. My personal strategy involved selecting the top two from each of the four tabs and the top three bowlers based on relevant parameters. Below this tab, you'll find the cumulative performance overview of this particular best 11.

Additionally, I decided to experiment with custom tooltips, creating three variations for batsmen, all-rounders, and bowlers. These tooltips are attached to their respective tabs and provide a rapid overview of each player's performance throughout the tournament. 

Explore the non-interactive PDF version of the dashboard [here](https://github.com/praneeth377/Cricket_T20WC_Best_11-Data_Analysis/blob/master/Dashboard.pdf) and the interactive version [here](https://app.powerbi.com/view?r=eyJrIjoiNjhlOWNlNjUtNThiMi00MDVjLTg5YmMtNDY3MTI1NzAzYWRiIiwidCI6IjAzMWEzYmJjLWNmN2MtNGUyYi05NmVjLTg2NzU1NTU0MGExYyJ9). Feel free to interact with the data. All changes made to the CSV files through Power Query are available [here](https://github.com/praneeth377/Cricket_T20WC_Best_11-Data_Analysis/blob/master/Best%2011%20Dashboard.pbix).

## Learnings and Conclusion
This project has been a tremendous learning experience for me. It involved the entire data analysis pipeline, from preprocessing using Python pandas to making refinements through Power Query. Establishing relationships among tables in Power BI and creating visually appealing dashboards added to my skill set. I delved into a variety of plot customizations, interactive button creations, and the development of custom tooltips. The exploration of DAX formulas and custom columns further enriched my understanding.

This project enhanced my skills in data preprocessing, Power BI, and advanced visualization. The experience with DAX formulas and custom columns has strengthened my analytical capabilities, providing a valuable foundation for my future professional endeavors.
