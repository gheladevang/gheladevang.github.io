---
name: Homework 10
tools: [Python, HTML, vega-lite, Altair]
image: assets/pngs/cars.png
description: Assignment 10, using Altair, Python, and Vega-lite
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Homework 10

## Plot 1: Number of Buildings per Congressional District

<br />
For my first visualization, I plotted the number of buildings present in each congressional district as a stacked bar chart. I encoded the congress district variable as a quantitative variable, and for the number of buildings, I used a count aggregation on 'Congress Dist' and encoded that as a quantitative variable as well. I colored the bars based on the status of the buildings within the districts, status being a nominal variable. I didn't change the color scheme as I felt the one it outputted was good enough. I felt that transformations were not necessary for the data as it seemed that there were no issues that might interfere with plotting it. I will note that I used the same data and chart I used for Homework 9, but plotting it using Altair, but the syntax was significantly easier for me to understand and write with as I'm more familiar with Python.
<br /><br />

<vegachart schema-url="{{ site.baseurl }}/assets/json/bar_buildings.json" style="width: 100%"></vegachart>

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/gheladevang/gheladevang.github.io/blob/main/python_notebooks/ghela-devang-assignment10.ipynb" text="The Analysis" %}
</div>


## Plot 2: Total Building Square Footage per Agency

<br />
For the second plot I made, I plotted the total square footage of the buildings under each agency within the dataset. I encoded the agency name variable as a ordinal variable as it is all just strings of names that could be ordered by alphabetical order. For the total square footage, I used a sum aggregation on 'Square Footage' and encoded it as a quantitative variable. For this plot, I stuck to the default blue color for the bars as I did not have a variable from the set to color the bars by. Once again, there were no other transformations I made on the data besides the aggregation I mentioned before. As I also mentioned before, I used the same chart I made in Homework 9, but using Altair made it easier to code.
<br /><br />

<vegachart schema-url="{{ site.baseurl }}/assets/json/bar_buildings2.json" style="width: 100%"></vegachart>

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/gheladevang/gheladevang.github.io/blob/main/python_notebooks/ghela-devang-assignment10.ipynb" text="The Analysis" %}
</div>

<br /><br />
### Interactivity

Something I noticed on my second plot was that there were bars that were too small to see what Total Square Footage they had, and other bars were too hard to estimate what that value was for them. To aid with this, I added a tooltip that shows the Agency Name and the Total Square Footage of buildings owned by the agency on the bar the user hovers over.