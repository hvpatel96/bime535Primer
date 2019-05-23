---
layout: page
title: "CDS and CPOE"
---
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega@4"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-lite@2.6.0"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-embed@3"></script>
<div id="vis"></div>
<script type="text/javascript">
	var spec = {
	  "config": {"view": {"width": 400, "height": 300}},
	  "data": {"url": "pubs.json", "format": {"type": "json"}},
	  "mark": {"type": "line", "point": true},
	  "encoding": {
	    "href": {"type": "nominal", "field": "url"},
	    "tooltip": {"type": "quantitative", "field": "Number of publications"},
	    "x": {"type": "ordinal", "field": "Year"},
	    "y": {"type": "quantitative", "field": "Number of publications"}
	  },
	  "title": "Pubmed Central results for \"decision support\"",
	  "$schema": "https://vega.github.io/schema/vega-lite/v2.6.0.json"
	}
	var opt = {"renderer": "canvas", "actions": false};  /* Options for the embedding */
	vegaEmbed("#vis", spec, opt);
</script>

## What is Clinical Decision Support?
## What is CPOE and how does it relate to CDS?
## What is the history of CDS?
## What are some current implementations of CDS?
## Many Clinical Decision Support systems are currently in use across the country and the world. 
## What successes and failures have current implementations seen?
## What are the important issues, benefits, and lessons learned?
## What are the challenges related to socio-cultural factors?
