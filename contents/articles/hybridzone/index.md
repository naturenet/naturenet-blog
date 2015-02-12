---
title: Notes on re-creating data visualizations of the hybrid zone of the black-capped chickadee and the carolina chickadee
author: Sloane O'Neill
date: 2015-02-05
template: article.jade
---


ISSUES

The only problem with some of the visualizations is that some of the data doesn’t accurately depict the moving border of the hybrid zone/migration zone/pattern because there are outliers that can skew the image visualized through Tableau. I do not see this as being just a problem with the eBird data but perhaps a problem with citizen science data mining in general: how accurately we can convey information via data visualization depends on how well the data is structured and I think that the way the eBird data (and other data from various citizen science platforms) is structured is not compatible with visualization systems. The goal then when designing citizen science platforms to collect data will be to create a platform which organizes/structures the data in a way such that it is understandable to the average persin and easy to use in conjunction with a specific visualization software (chosen by the website for example). 

-------------------------------------------------------------------------------------------------------------------------

Specific issues with tableau: 

Need to figure out to convey ‘observation clusters’ to depict a more accurate representation of the data 
Perhaps when we import the data into excel something becomes corrupted and fills certain slots in with an X – because it is ridiculous that they would have data and a location and time/place etc. and not include how many (if any) observed it there – will need to look into this. 
-------------------------------------------------------------------------------------------------------------------------

Here is an image of the black-capped chickadee zone between 1990 and 2004 in the northern US based off of individual observations logged through eBird:
-------------------------------------------------------------------------------------------------------------------------

![black-capped chickadee zone as catalogued by eBird: 1990-2004](black-capped-90-04.PNG)


Here is the same black-capped species from 1950-1990:

![black-capped](black-capped-50-90.PNG "Black-capped Chickadee zones: 1950-2004")

Here is the Carolina chickadee zone as observed between the years 1950 and 1990:

![carolina](carolina-chicka-50-90.PNG)

Here is our pre-liminary data visualization for the hybrid zone between these two chickadee types; it is based off of all fo the observations -- the data we have contains observations from 1950 to 2004.


![hybrid](chicka-hybrid-zone.PNG)