# Model bias dashboard


<div>

  <div id="dashboard-bias"></div>
  <p>test</p>

</div>


<script>

require.config({
    paths: {
        "d3": "https://d3js.org/d3.v6.min",
        "Plotly": "https://cdn.plot.ly/plotly-3.0.1.min"
    }
});

function createNutsMap(parent) {
    Plotly.newPlot(parent, [{
	    x: [1, 2, 3, 4, 5],
	    y: [1, 2, 4, 8, 16]
    }], {
	    margin: { t: 0 } 
    });
}

document.addEventListener("DOMContentLoaded", function () {
    const dashboard = document.getElementById("dashboard-bias");

    require(["Plotly"], (Plotly) => {
        const map = createNutsMap(dashboard);
    });

});

</script>
