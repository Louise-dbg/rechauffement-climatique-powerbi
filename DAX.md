# Code DAX Power BI

1. Code DAX — Table des dates

Calendrier = 
ADDCOLUMNS( 
    CALENDARAUTO(),
    "Year", YEAR([Date]),
    "Month Number", MONTH([Date]),
    "Month", FORMAT([Date], "MMMM")
)

2. Code DAX — Table des latitudes uniques

Latitude_Uniques = DISTINCT('Températures par villes'[Latitude])

3. Code DAX — Table des longitudes uniques

Longitude_Uniques = DISTINCT('Températures par villes'[Longitude])

 4. Code DAX — Table des pays uniques (fusion de deux sources)

Pays_Uniques = 
DISTINCT(
    UNION(
        VALUES('Températures par villes'[Pays]),
        VALUES('Températures par pays'[Pays])
    )
)

 5. Code DAX — Table des villes uniques

Villes_Uniques = DISTINCT('Températures par villes'[Villes])

