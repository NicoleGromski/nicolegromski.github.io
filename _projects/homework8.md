---
name: Weather Visualizations
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: Two plots from the weather dataset!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Weather Dataset



## Bar Chart

This is a visualization from the temperature dataset that is a bar chart using Vega-lite to visualize the mid_temperature based on the the season. The encoding that I ended up using was ordinal for the seasons since it was more categorical and needed to be in order and qualitative for the temperature since they were numerical values. The colors I used were the seasons to show how the count of humidity levels related to each season. A colormap was not necessary since this was just a simple segmented bar chart. I did not complete homework 7 so I do not have anything to compare this graph to. A transformation  was not necessary in this graph either since it did not have any interactivity included in it. 


<vegachart schema-url="{{ site.baseurl }}/assets/json/plot12.json" style="width: 100%"></vegachart> 


## Side-by-Side Interactive Scatterplot

This plot is a side by side interactive scatterplot inspired by the Altair documents. The plot compares the high temperture values in the dataset with visibility and humidity with the points on the graph being color coded by season. There are two graphs one shows the association between high temperature and visibility while the other shows the association between high temperature and humidity levels. The high temperature values are in degrees Farenheit with a float data type. The visibility values are not specificed but are assumed to be some sort of distance measurements such as meters or miles with the float data type as well. The humidity values are g/kg which is grams of water vapor per metre of air with the data type of float. The plot is interactive using a brush interval selector to be able to highlight numerous points on the graph at once and display the relating data on the graph next to it. By doing this, you can see how visibility and humidity play a part in high temperature weather patterns. Without the interactivity it would be more difficult to compare humidity and visibility levels. I used the brush selector because I wanted to be able to have an adjustable window of points to compared multiple data points at once. For the encoding of the graph, I made the mark point since I wanted to make a scatter plot and the colors are encoded to the nominal variable of seasons to see how visibility and pressure are different based on the different seasons. I did not complete Homework 7 so I did not have a graph that compares to this one from that homework 7. If I were to have completed it, the graph I would have had would have not been interactive and possibly just a simple scatter plot such as the high_temperature and humidity one so with this I added a similar plot to interact with so that comparison is easier. 

<vegachart schema-url="{{ site.baseurl }}/assets/json/scatter.json" style="width: 100%"></vegachart> 

## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

```
<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/NicoleGromski/nicolegromski.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/NicoleGromski/nicolegromski.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>

