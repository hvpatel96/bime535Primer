---
layout: page
title: "CDS and CPOE"
---
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega@4"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-lite@2.6.0"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-embed@3"></script>
<div id="vis"></div>
<script type="text/javascript">var spec = {
  "config": {"view": {"width": 400, "height": 300}},
  "data": {"name": "data-9f4489a26ceddb61f839d22e711059f9"},
  "mark": {"type": "line", "point": true},
  "encoding": {
    "href": {"type": "nominal", "field": "url"},
    "tooltip": {"type": "quantitative", "field": "Number of publications"},
    "x": {"type": "nominal", "field": "Year"},
    "y": {"type": "quantitative", "field": "Number of publications"}
  },
  "title": "Pubmed Central results for \"decision support\"",
  "$schema": "https://vega.github.io/schema/vega-lite/v2.6.0.json",
  "datasets": {
    "data-9f4489a26ceddb61f839d22e711059f9": [
      {
        "Year": 1990,
        "Number of publications": 80,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+1990%5Bdp%5D"
      },
      {
        "Year": 1991,
        "Number of publications": 77,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+1991%5Bdp%5D"
      },
      {
        "Year": 1992,
        "Number of publications": 76,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+1992%5Bdp%5D"
      },
      {
        "Year": 1993,
        "Number of publications": 87,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+1993%5Bdp%5D"
      },
      {
        "Year": 1994,
        "Number of publications": 128,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+1994%5Bdp%5D"
      },
      {
        "Year": 1995,
        "Number of publications": 187,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+1995%5Bdp%5D"
      },
      {
        "Year": 1996,
        "Number of publications": 141,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+1996%5Bdp%5D"
      },
      {
        "Year": 1997,
        "Number of publications": 250,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+1997%5Bdp%5D"
      },
      {
        "Year": 1998,
        "Number of publications": 234,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+1998%5Bdp%5D"
      },
      {
        "Year": 1999,
        "Number of publications": 219,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+1999%5Bdp%5D"
      },
      {
        "Year": 2000,
        "Number of publications": 228,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2000%5Bdp%5D"
      },
      {
        "Year": 2001,
        "Number of publications": 280,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2001%5Bdp%5D"
      },
      {
        "Year": 2002,
        "Number of publications": 318,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2002%5Bdp%5D"
      },
      {
        "Year": 2003,
        "Number of publications": 300,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2003%5Bdp%5D"
      },
      {
        "Year": 2004,
        "Number of publications": 248,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2004%5Bdp%5D"
      },
      {
        "Year": 2005,
        "Number of publications": 404,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2005%5Bdp%5D"
      },
      {
        "Year": 2006,
        "Number of publications": 466,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2006%5Bdp%5D"
      },
      {
        "Year": 2007,
        "Number of publications": 533,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2007%5Bdp%5D"
      },
      {
        "Year": 2008,
        "Number of publications": 780,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2008%5Bdp%5D"
      },
      {
        "Year": 2009,
        "Number of publications": 884,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2009%5Bdp%5D"
      },
      {
        "Year": 2010,
        "Number of publications": 1124,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2010%5Bdp%5D"
      },
      {
        "Year": 2011,
        "Number of publications": 1555,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2011%5Bdp%5D"
      },
      {
        "Year": 2012,
        "Number of publications": 1859,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2012%5Bdp%5D"
      },
      {
        "Year": 2013,
        "Number of publications": 2358,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2013%5Bdp%5D"
      },
      {
        "Year": 2014,
        "Number of publications": 2690,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2014%5Bdp%5D"
      },
      {
        "Year": 2015,
        "Number of publications": 3092,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2015%5Bdp%5D"
      },
      {
        "Year": 2016,
        "Number of publications": 3143,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2016%5Bdp%5D"
      },
      {
        "Year": 2017,
        "Number of publications": 3595,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2017%5Bdp%5D"
      },
      {
        "Year": 2018,
        "Number of publications": 3333,
        "url": "https://www.ncbi.nlm.nih.gov/pmc/?term=%22decision+support%22+2018%5Bdp%5D"
      }
    ]
  }
};
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
