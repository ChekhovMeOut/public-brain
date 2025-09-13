```dataview
TABLE WITHOUT ID file.link as Link, distance as Dist  
FROM #Strava 
WHERE sport_type = "Run"
:> ```