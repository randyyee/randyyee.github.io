---
layout: full-width
title: About
---
<script src="https://www.amcharts.com/lib/3/ammap.js" type="text/javascript"></script>
<script src="https://www.amcharts.com/lib/3/maps/js/worldHigh.js" type="text/javascript"></script>
<script src="https://www.amcharts.com/lib/3/themes/dark.js" type="text/javascript"></script>
<div id="mapdiv" style="width: 1000px; height: 450px;"></div>
<div style="width: 1000px; font-size: 70%; padding: 5px 0; text-align: center; background-color: #535364; margin-top: 1px; color: #B4B4B7;"><a href="https://www.amcharts.com/visited_countries/" style="color: #B4B4B7;">Create your own visited countries map</a> or check out the <a href="https://www.amcharts.com/" style="color: #B4B4B7;">JavaScript Charts</a>.</div>
<script type="text/javascript">
var map = AmCharts.makeChart("mapdiv",{
type: "map",
theme: "dark",
projection: "mercator",
panEventsEnabled : true,
backgroundColor : "#535364",
backgroundAlpha : 1,
zoomControl: {
zoomControlEnabled : true
},
dataProvider : {
map : "worldHigh",
getAreasFromMap : true,
areas :
[
	{
		"id": "BE",
		"showAsSelected": true
	},
	{
		"id": "FR",
		"showAsSelected": true
	},
	{
		"id": "GR",
		"showAsSelected": true
	},
	{
		"id": "GB",
		"showAsSelected": true
	},
	{
		"id": "CA",
		"showAsSelected": true
	},
	{
		"id": "US",
		"showAsSelected": true
	},
	{
		"id": "CN",
		"showAsSelected": true
	},
	{
		"id": "HK",
		"showAsSelected": true
	},
	{
		"id": "JP",
		"showAsSelected": true
	}
]
},
areasSettings : {
autoZoom : true,
color : "#B4B4B7",
colorSolid : "#E88484",
selectedColor : "#E88484",
outlineColor : "#666666",
rollOverColor : "#F59DAD",
rollOverOutlineColor : "#000000"
}
});
</script>


<h1 class="content-listing-header sans">About Randy Yee</h1>
Thanks for visiting my page!

<h1>Short Biography</h1>

2018 - Biomedical Engineering MEng.

2016 - Global Health and Development MSc.

2011 - English Literature BA.
