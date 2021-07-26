# ADDING CHARTS USING JS
SOMETIMES, we need to have a canvas in our page. It's recommended to give the chart its own container for responsiveness.      

>
 <div>
  <canvas id="myChart"></canvas>
 </div>
> 
    
Now that we have a canvas we can use, we need to include Chart.js in our page.

    
Now, we can create a chart. We add a script to our page:
>
 const config = {
  type: 'line',
  data,
  options: {}
};
 >
 >
const config = {
  type: 'line',
  data,
  options: {}
 };
>
Finally, render the chart using our configuration:

<script>
  // === include 'setup' then 'config' above ===

  var myChart = new Chart(
    document.getElementById('myChart'),
    config
  );
</script>
 
    
It's that easy to get started using Chart.js! From here you can explore the many options that can help you customise your charts with scales, tooltips, labels, colors, custom actions, and much more.


# Line Chart
A line chart is a way of plotting data points on a line. Often, it is used to show trend data, or the comparison of two data sets.
![Line Chart](https://dyclassroom.com/image/topic/chartjs/v2/line-graph.png) 
# Bar Chart
A bar chart provides a way of showing data values represented as vertical bars. It is sometimes used to show trend data, and the comparison of multiple data sets side by side.
![Bar Chart](https://i.stack.imgur.com/dGJPK.png) 
# Radar Chart
A radar chart is a way of showing multiple data points and the variation between them.

They are often useful for comparing the points of two or more different data sets.
![Radar Chart](https://i.stack.imgur.com/jyNdx.png) 
# Doughnut and Pie Charts
Pie and doughnut charts are probably the most commonly used charts. They are divided into segments, the arc of each segment shows the proportional value of each piece of data.

They are excellent at showing the relational proportions between data.

Pie and doughnut charts are effectively the same class in Chart.js, but have one different default value - their cutout. This equates to what portion of the inner should be cut out. This defaults to 0 for pie charts, and '50%' for doughnuts.

They are also registered under two aliases in the Chart core. Other than their different default value, and different alias, they are exactly the same.
![Doughnut and Pie Charts](https://apexcharts.com/wp-content/uploads/2018/05/simple-donut-chart.svg) 
# Polar Area Chart
Polar area charts are similar to pie charts, but each segment has the same angle - the radius of the segment differs depending on the value.

This type of chart is often useful when we want to show a comparison data similar to a pie chart, but also show a scale of values for context.
![Polar Area Chart](https://apexcharts.com/wp-content/uploads/2020/09/basic-polar-area.png) 
# Bubble Chart
A bubble chart is used to display three dimensions of data at the same time. The location of the bubble is determined by the first two dimensions and the corresponding horizontal and vertical axes. The third dimension is represented by the size of the individual bubbles.
![Bubble Chart](https://apexcharts.com/wp-content/uploads/2018/05/simple-bubble-chart.svg) 
# Scatter Chart
Scatter charts are based on basic line charts with the x axis changed to a linear axis. To use a scatter chart, data must be passed as objects containing X and Y properties. The example below creates a scatter chart with 4 points.
![Scatter Chart](https://apexcharts.com/wp-content/uploads/2018/05/scatter-chart-basic.svg) 

