# Excess Mortality during the Covid-19 pandemic

This repository contains excess mortality data for the period covering the 2020 Covid-19 pandemic. The data has been collected from national, regional or municipal agencies that collect death registrations and publish official mortality statistics. These original data reshaped into a standard format by FT journalists to allow cross-national comparisons.

The repository contains the excess mortality data for all known jurisdictions which publish all-cause mortality data meeting the following criteria:

* daily, weekly or monthly level of granularity
* includes equivalent historical data for at least one full year before 2020, and preferably at least five years (2015-2019)
* includes data up to at least April 1, 2020

Most countries publish mortality data with a longer periodicity (typically quarterly or even annually), a longer lag time, or both. This sort of data is not suitable for ongoing analysis during an epidemic and is therefore not included here.

## Data definitions

All of the data can be found in the file `data.csv`. For each jurisdiction and each daily, weekly or monthly period, the data contains the following fields:

* `deaths`: historical daily, weekly or monthly numbers of all-cause deaths for as far back as we have been able to obtain this data
* `expected_deaths`: the median value of this data for the equivalent period in years from 2015 to 2019
* `excess_deaths`: difference between `deaths` and `expected deaths` (negative values indiciate fewer deaths than the recent historical average)
* `excess_deaths_pct`: `excess_deaths` as a percentage of `expected_deaths`

## Stories

"Excess mortality" refers to the difference between deaths from all causes during the pandemic and the historic seasonal average. For many of the jurisdictions shown here, this figure is higher than the official Covid-19 fatalities that are published by national governments each day. While not all of these deaths are necessarily attributable to the disease, it does leave a number of unexplained deaths that suggests that the official figures of deaths attributed may significant undercounts of the pandemic's impact.

The data published here were used to inform the following Financial Times stories and graphics:

* Ongoing: [Coronavirus tracked: the latest figures as countries fight to contain the pandemic](https://www.ft.com/content/a26fbf7e-48f8-11ea-aeb3-955839e06441)
* April 22, 2020: [UK coronavirus deaths more than double official figure, according to FT study](https://www.ft.com/content/67e6a4ee-3d05-43bc-ba03-e239799fa6ab)
* April 26, 2020: [Global coronavirus death toll could be 60% higher than reported](https://www.ft.com/content/6bd88b7d-3386-4543-b2e9-0d5c6fac846c)
* April 28: [Low Covid-19 death toll raises hopes Africa may be spared worst](https://www.ft.com/content/e9cf5ed0-a590-4bd6-8c00-b41d0c4ae6e0)
* May 5, 2020: [Turkey's virus deaths may be 25 per cent higher than official figure](https://www.ft.com/content/80bb222c-b6eb-40ea-8014-563cbe9e0117)
* May 11, 2020: [Russia's Covid death toll could be 70 per cent higher than official figure](https://www.ft.com/content/77cd2cba-b0e2-4022-a265-e0a9a7930bda)
* May 19, 2020: [UK deaths since virus struck almost 55,000 above average, says ONS](https://www.ft.com/content/f6a11fcd-0445-4643-9d3c-24d5fc0611da)
* May 28, 2020: [UK suffers highest death rate from coronavirus](https://www.ft.com/content/6b4c784e-c259-4ca4-9a82-648ffde71bf0)

## Sources

The data re-published here has been gathered and standardised from the following [official sources](sources.md):

| id | region           | category   | country        | iso | agency                                                                                                                                                                                                                                  |
|----:|------------------|------------|----------------|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1  |                  |            |                |     | [Financial Times calculation](http://www.ft.com/)                                                                                                                                                                                                 |
| 2  |                  |            | Austria        | AUT | [Statistics Austria](http://www.statistik.at/web_de/statistiken/menschen_und_gesellschaft/bevoelkerung/gestorbene/index.html)                                                                                                                     |
| 3  |                  |            | Belgium        | BEL | [Sciensanto](https://covid-19.sciensano.be/fr/covid-19-situation-epidemiologique)                                                                                                                                                                 |
| 4  | Manaus           |            | Brazil         | BRA | [Civil Registry of Brazil](https://transparencia.registrocivil.org.br/registros)                                                                                                                                                                  |
| 5  |                  |            | Chile          | CHL | [Civil Registry of Chile](https://github.com/MinCiencia/Datos-COVID19/tree/master/output/producto32)                                                                                                                                              |
| 6  |                  |            | Denmark        | DNK | [Statistics Denmark](https://m.statbank.dk/TableInfo/DODC2)                                                                                                                                                                                       |
| 7  | Guayas           |            | Ecuador        | ECU | [Civil Registry of Ecuador](https://www.registrocivil.gob.ec/cifras/)                                                                                                                                                                             |
| 9  |                  | current    | France         | FRA | [National Institute of Statistics and Economic Studies](https://insee.fr/fr/information/4470857)                                                                                                                                                  |
| 9  |                  |            | Germany        | DEU | [Federal Statistics Office](https://www.destatis.de/DE/Themen/Gesellschaft-Umwelt/Bevoelkerung/Sterbefaelle-Lebenserwartung/sterbefallzahlen.html)                                                                                                |
| 10 |                  |            | Iceland        | ISL | [Statistics Iceland](https://hagstofa.is/utgafur/tilraunatolfraedi/danir-tt/)                                                                                                                                                                     |
| 11 | Jakarta          |            | Indonesia      | IDN | [Jakarta Provincial Park and Forest Service](https://pertamananpemakaman.jakarta.go.id/v813/t1p1/csv-data25.csv/YXNzZXRzL2RhdGEvY3N2LXBlbWFrYW1hbi8-)                                                                                             |
| 12 |                  |            | Israel         | ISR | [Minstry of Health](https://www.health.gov.il/UnitsOffice/HD/PH/epidemiology/Pages/epidemiology_report.aspx?WPID=WPQ7&PN=6)                                                                                                                       |
| 13 |                  |            | Italy          | ITA | [National Institute of Statistics](https://www.istat.it/en/archivio/240106)                                                                                                                                                                       |
| 14 |                  |            | Netherlands    | NLD | [Statistics Netherlands](https://opendata.cbs.nl/statline/#/CBS/nl/dataset/70895ned/table?ts=1585918931535)                                                                                                                                       |
| 15 |                  |            | Norway         | NOR | [Statistics Norway](https://www.ssb.no/statbank/table/07995/)                                                                                                                                                                                     |
| 16 |                  |            | Peru           | PER | [Ministry of Health](https://cloud.minsa.gob.pe/s/BGCKJBWKELW8nDi/download?path=%2F&files=Carga_Tableau_12052020.xlsx&downloadStartSecret=ieif5k3ymp)                                                                                             |
| 17 |                  |            | Portugal       | PRT | [Directorate-General for Health](https://evm.min-saude.pt/)                                                                                                                                                                                       |
| 18 | Moscow           |            | Russia         | RUS | [Moscow city government](https://data.mos.ru/opendata/7704111479-dinamika-registratsii-aktov-grajdanskogo-sostoyaniya?pageNumber=1&versionNumber=3&releaseNumber=42)                                                                              |
| 19 |                  |            | South Africa   | ZAF | [Medical Research Council](https://www.samrc.ac.za/reports/report-weekly-deaths-south-africa)                                                                                                                                                     |
| 20 |                  |            | Spain          | ESP | [Institute of Health Carlos III](https://momo.isciii.es/public/momo/dashboard/momo_dashboard.html#datos)                                                                                                                                          |
| 22 |                  |            | Sweden         | SWE | [Statistics Sweden](https://www.scb.se/contentassets/edc2b33f85ad415d8e7909002253ed84/2020-04-09---preliminar-statistik-over-doda-inkl-eng.xlsx)                                                                                                  |
| 22 |                  |            | Switzerland    | CHE | [Federal Statistics Office](https://www.bfs.admin.ch/bfs/en/home/statistics/health/state-health/mortality-causes-death.html)                                                                                                                      |
| 23 | Istanbul         |            | Turkey         | TUR | [Istanbul Metropolitan Municipality](https://www.turkiye.gov.tr/istanbul-buyuksehir-belediyesi-vefat-sorgulama)                                                                                                                                   |
| 24 | England & Wales  |            | United Kingdom | GBR | [Office for National Statistics](https://www.ons.gov.uk/peoplepopulationandcommunity/birthsdeathsandmarriages/deaths/datasets/weeklyprovisionalfiguresondeathsregisteredinenglandandwales)                                                        |
| 25 | Scotland         |            | United Kingdom | GBR | [National Records of Scotland](https://www.nrscotland.gov.uk/statistics-and-data/statistics/statistics-by-theme/vital-events/general-publications/weekly-and-monthly-data-on-births-and-deaths/deaths-involving-coronavirus-covid-19-in-scotland) |
| 26 | Northern Ireland |            | United Kingdom | GBR | [Northern Ireland Statistics and Research Agency](https://www.nisra.gov.uk/publications/weekly-deaths)                                                                                                                                            |
| 37 |                  |            | United States  | USA | [National Center for Health Statistics](https://gis.cdc.gov/grasp/fluview/mortality.html)                                                                                                                                                         |

## License and attribution

This software is published by the Financial Times under the [MIT license](https://opensource.org/licenses/MIT). 

The data in the `data` directory of this repository is available under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

If you use this data, you must attribute it to "Financial Times" as well as the relevant originating agency or agencies listed above. If it is published online, we would appreciate a link to our [Coronavirus tracker page](https://www.ft.com/content/a26fbf7e-48f8-11ea-aeb3-955839e06441), where this material first appeared.

Please let us know if you are using this data by contacting us at [coronavirus-data@ft.com](mailto:cornoavirus-data@ft.com). We may be interested in reporting on your work.

Please note that MIT licence includes only the software, and the Creative Commons licence includes only the data included in this repository. Neither cover any FT content made available using the software or data, which is copyright © The Financial Times Limited, all rights reserved. For more information about re-publishing FT content, please contact our [syndication department](https://enterprise.ft.com/en-gb/services/republishing/).

## Contributors

Work on this project is led by [John Burn-Murdoch](https://www.ft.com/stream/e191658e-c66a-45bc-9bad-343bdc4210b3) of the [FT Visual & Data Journalism team](https://www.ft.com/visual-and-data-journalism).

Additional contributors include [Chris Giles](https://www.ft.com/chris-giles), [Valentina Romei](https://www.ft.com/valentina-romei), [Henry Foy](https://www.ft.com/henry-foy) [David Pilling](https://www.ft.com/david-pilling), [Laura Pitel](https://www.ft.com/laura-pitel), [Martin Stabe](https://www.ft.com/martin-stabe) and [Aleksandra Wisniewska](https://www.ft.com/aleksandra-wisniewska).

To contact the team, please email [coronavirus-data@ft.com](mailto:cornoavirus-data@ft.com).

## How you can help

If you are aware of a jurisdiction not already listed here which publishes all-cause mortality data that meets the criteria set out above, please send us a link to the source of that data at [coronavirus-data@ft.com](mailto:cornoavirus-data@ft.com).

Alternatively, please submit a pull request to this repository adding the relevant information to the file `[sources.md](/sources.md)`.