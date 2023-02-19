<h1 align=center>AGRODE</h1>

AGRODE aims to utilise various data analysis and visualisation techniques for explaining whether the current geographical, political, and logical scenarios 
would benefit North Germany from the use of Agrivoltaics or not. The states that come under the umbrella term of North Germany are **Bremen**, **Hamburg**, 
**Niedersachsen**, **Mecklenberg-Vorpommern**, and **Schleswig-Holstein**.

## What is Agrivoltaics?

It simply means that we use the same piece of land for farming and solar panel installations. Various researches have shown that by doing this, we can improve 
the land productivity by nearly twofolds. However, there is a slight caveat of crop selection that can be paired with solar panels. Only shade tolerant crops
like wheat, lettuce, potatoes, etc. can be used for agrivoltaics.

![agro](https://metsolar.eu/blog/wp-content/uploads/2018/04/3-1.jpg)

## Dataset Used

* [Marktdatenstammregister](https://www.marktstammdatenregister.de/MaStR) - used for obtaining data about PV intallations by applying various filters
* [Taxation Rates](https://www.dihk.de/de/themen-und-positionen/wirtschaftspolitik/steuer-und-finanzpolitik/hebesaetze-56878) - used for obtaining tax data for 
PV installations in different districts

## Bried Description

* SECTION 1 - Data Cleaning
> The data was loaded into pandas dataframes. The column names were translated from German to English for better understanding using Google's translator
API. Numerical columns were saved as object data type so I had to convert them into float data type. Before converting the column data type, rows with NaN
values had to be dropped. Then I had to replace commas (,) with full stops (.) because pandas cannot convert strings with comma to float data type. Lastly,
I had to convert some column names and values manually using map functions.
 
* SECTION 2 - Solar Data Analysis
> This section deals with an in-depth analysis of solar data extracted from our main dataset. It consistes of three main parts - solar power loss in North
Germany, distribution of solar panel orientations, and solar power loss due to panel orientation. Solar power loss is calculated as the state-wise difference between gross solar power and net solar power normalised by the gross solar power multiplied by a factor of 100. Solar panel orientations is 
calculated as the sum of value counts of different orientations. Lastly, the solar power loss due to panel orientations is calculated by aggregating gross
and net output by different orientations.

* SECTION 3 - Energy Source Analysis
> This section utilises some bar graphs to show the different sources of energy that fuel North Germany. It also shows the distribution of solar panel 
orientations throughout different states. And also shows us how solar energy compared to the other sources of energy in North Germany.

* SECTION 4 - Geospatial Analysis
> I have used geopandas and contexily here to generate geospatial plots of North Germany in various scenarios. We can see the distribution of freeland solar installations in different states at night, by geographical terrain, and plant size of installation.

* SECTION 5 - Tax Data Analysis
> The tax analysis shows us the ditribution of tax rates in different states through a violin plot. A more detailed analysis on tax data's relationship with PhotoVoltaic installations was carried out by one of my team mates.

## Summary

* all Northern states have higher number of solar plant installations than any other energy source

* Coal is the main source of energy for Bremen and Hamburg while Wind drives our three bigger states

* Mecklenburg-Vorpommern has some of the biggest solar plants in North Germany

* Wind Energy has a much higher potential for North Germany as compared to Solar Energy 

* more installation are found in areas with lesser rate for Property Tax B

* despite having lower tax rates Mecklenburg-Vorpommern focuses more on Wind energy

* future planned installation of PV are mostly on rooftops to avoid conflict with farmers

* EEG subsidy for PV installation has not been adapted by North Germany

* soil quality in North is good for crops like potato that can be used for agrivoltaics

* a viable option for North Germany can be Hybrid plants - install solar panels on wind farms
