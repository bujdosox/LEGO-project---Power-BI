## LEGO project
### Sets released between 1970 and 2022
Some interesting investigations about LEGO sets releases from 1970 to 2022

![Lego_dashboard](https://github.com/bujdosox/LEGO_project_PowerBI/assets/173184545/6267df99-a23c-4797-b188-6c29c3592152)

### Goal
-   Looking for trends by temporal distribution of released amount
-   Defining most popular themes in each decade
-   Investigating distribution of mini figures based on themes
-   Investigating distribution of released amount by minimum recommended age
-   Total release and total licensed release in the investigation period
### Outcome
-   Release of new LEGO sets shows overall constant increase in the investigation period
-   Significant jump regardning new releases from middle of 1990's
-   Most popular themes after Miscellaneous (most mini figures belong to these themes as well)

        o   Licensed: 2.509 total releases (1.846 sets with mini figures)
-   Modern Day: 2.357 total releases (1.824 sets with mini figures)
-   Top 3 minimum recommended age (after unclassified)

        o   5 years: 1.574 sets
        o   6 years: 1.604 sets
        o   7 years: 1.179 sets
### Methods and steps
-   Loading single CSV file into Power BI Desktop
-   Checking coloumn quality, coloumn distribution, coloumn profile and data types regarding the whole data set in Power Query editor
-   Transforming data in Power Query editor in order to prepare analysis
-   Creating separate table for measures + create DAX calculations in order to use them anywhere in the report, referenced by other DAX measures and provide more complex calculations 
-   Visualize data in Report view
