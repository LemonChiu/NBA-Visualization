# Visualization of NBA 2014

###[Online Demo](http://lemonchiu.github.io/NBA-Visualization/)

![Screenshot Overview](https://raw.githubusercontent.com/LemonChiu/NBA-Visualization/master/screenshot/Overview.jpg)

### Package Description
It includes:

+ index.html: The main html to embed D3 script.
+ css: CSS of the radar chart and the main page.
+ data: JSON and CSV files for the U.S. geographic data, the players and the teams in NBA.
+ js: Javascript files for the D3 library, tip, radar chart, and the main page script to load data and generate visualization.
+ logo: SVG logos of 30 NBA teams.
+ screenshot: Screenshots for important features of the visualization.

### Data Sample
The NBA teams and players' data:

+ Source: [2014-15 Regular Season Traditional Team Stats](http://stats.nba.com/league/team/#!/) and [2014-15 Regular Season Traditional Player Stats](http://stats.nba.com/league/player/#!/).
+ The original data is grabbed from the web page and it is transformed to the CSV files.

The U.S. geographic data:

+ Source: [USA.json](http://www.ourd3js.com/map/worldmap/America/USA.json)
+ The JSON file is then simplified by using [mapshaper](http://mapshaper.org/)

### Methodology and Design
+ The U.S.map is shown with two colors to distinguish the East and the West.
+ Each team is located at its home court and it's represented by a circle which the radius and opacity vary differently due to different winning rate. And both radius and opacity have a linear relationship with the winning rate.
+ Move over a circle, logo and exact winning rate of the represented team will appear.
+ Click on a state to zoom in to get a clearer view.
+ Select a team to generate pie slices as lengths extending outward to the edge. The names of the relevant data are specified in the center. They are "Points", "Assists", "Rebounds", "Blocks", "Steals" and "Turnovers". Both lengths and widths of the pie slices are affected by each player's stats. The length indicates the proportion of the highest value in the current league while the width reveals the proportion in a team.
+ When more than one team is selected, a radar chart which compares the data mentioned above between the selected teams will be displayed. Exact values of all stats have a linear relationship with the team's relevant ranks. Additionally, Click again to reverse.
+ Click the "Show" button in the bottom to exhibit the bar chart of the whole league. Hover over a bar to obtain one data's name of a certain team.
+ The chart has multiples mode and stacked mode. What's more, weight of each item can be assigned and click the "Show" button again to create a new one.

### License
Licensed under The [MIT](https://github.com/LemonChiu/NBA-Visualization/blob/master/LICENSE) License
