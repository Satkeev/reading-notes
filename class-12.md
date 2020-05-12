### Creating a Chart

>It's easy to get started with Chart.js. All that's required is the script included in your page  
along with a single <canvas> node to render the chart.   
In this example, we create a bar chart for a single dataset and render that in our page. You can   
see all the ways to use Chart.js in the usage documentation.  

><canvas id="myChart" width="400" height="400"></canvas>  
<script>  
var ctx = document.getElementById('myChart').getContext('2d');  
var myChart = new Chart(ctx, {  
    type: 'bar',  
    data: {  
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],  
        datasets: [{  
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],  
            backgroundColor: [  
                'rgba(255, 99, 132, 0.2)',  
                'rgba(54, 162, 235, 0.2)',  
                'rgba(255, 206, 86, 0.2)',  
                'rgba(75, 192, 192, 0.2)',  
                'rgba(153, 102, 255, 0.2)',  
                'rgba(255, 159, 64, 0.2)'  
            ],  
            borderColor: [  
                'rgba(255, 99, 132, 1)',  
                'rgba(54, 162, 235, 1)',  
                'rgba(255, 206, 86, 1)',  
                'rgba(75, 192, 192, 1)',  
                'rgba(153, 102, 255, 1)',    
                'rgba(255, 159, 64, 1)'  
            ],  
            borderWidth: 1  
        }]  
    },  
    options: {  
        scales: {  
            yAxes: [{  
                ticks: {  
                    beginAtZero: true  
                }  
            }]  
        }  
    }  
});  
</script>  

The ><canvas> element    
<canvas id="tutorial" width="150" height="150"></canvas>  
At first sight a <canvas> looks like the <img> element, with the only clear difference being that    
it doesn't have the src and alt attributes. Indeed, the <canvas> element has only two attributes,   
  width and height. These are both optional and can also be set using DOM properties. When no width   
  and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high.   
  The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout   
  size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.  
Note: If your renderings seem distorted, try specifying your width and height attributes explicitly in the  
<canvas> attributes, and not using CSS.  
The id attribute isn't specific to the <canvas> element but is one of the global HTML attributes which can   
be applied to any HTML element (like class for instance). It is always a good idea to supply an id because  
this makes it much easier to identify it in a script.
The <canvas> element can be styled just like any normal image (margin, border, background…). These rules,   
however, don't affect the actual drawing on the canvas. We'll see how this is done in a dedicated chapter   
of this tutorial. When no styling rules are applied to the canvas it will initially be fully transparent.  
Fallback content  
