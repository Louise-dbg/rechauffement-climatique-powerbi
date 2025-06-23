# Code Power Query (M) pour conversion des coordonnées géographiques

> Ce code Power Query transforme les coordonnées en texte (ex: "48.8566N", "2.3522E")  
> en valeurs numériques, en appliquant un signe négatif pour les directions Sud (S) et Ouest (W).

---

## 1. Conversion de la latitude en valeur numérique

```m
Table.AddColumn(#"Colonnes renommées3", "Latitude nb", each 
    if Text.End([Latitude], 1) = "S" then 
        -1 * Number.FromText(Text.Start([Latitude], Text.Length([Latitude]) - 1))
    else 
        Number.FromText(Text.Start([Latitude], Text.Length([Latitude]) - 1))
)

## 2. Conversion de la longitude en valeur numérique

Table.AddColumn(#"Type modifié2", "Longitude nb", each 
    if Text.End([Longitude], 1) = "W" then 
        -1 * Number.FromText(Text.Start([Longitude], Text.Length([Longitude]) - 1))
    else 
        Number.FromText(Text.Start([Longitude], Text.Length([Longitude]) - 1))
)
