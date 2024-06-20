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
-   Load single CSV file into Power BI Desktop
-   Check coloumn quality, coloumn distribution and coloumn profile regarding the whole data set in Power Query editor
-   Check data types in Power Query editor
-   Transform data in Power Query editor

        o   Promoted first row as header
        o   Change data type of year, pieces, minfiges, agerange from text to whole number
        o   Replace dot to comma in us_retailPrice coloumn, then change data type from text to currency
        o   Add new conditional coloumn named „decade” based on year of release
-   Create a separate table for measures in Table view + create new measures

        o   Count sets = DISTINCTCOUNT(lego_sets[set_id])
        o   Count sets mini figures = CALCULATE([Count sets], lego_sets[minifigs] <> 0)
-   Visualize data in Report view

        o   Coloumn chart: Release trend by temporal distribution
        o   Matrix: Released quantity by themes (highlighting the quantity by data bar color)
        o   Slicer with decades
        o   Donut chart: Mini figure distribution by theme (top 5)
        o   Multi row-card: Total releases and Total releases with mini figures
        o   Matrix: Released quantity by minimum recommended age range
        o       Slicer with decades
        o       Donut chart: Mini figure distribution by theme (top 5)
        o       Multi row-card: Total releases and Total releases with mini figures
        o       Matrix: Released quantity by minimum recommended age range
        o       Checking interactions
        o       Summarize outcomes on a separate page
        o       Create a fix panel with buttons: change between pages + clear all filters
