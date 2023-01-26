


   
  



# Energy Production GDP Machine Learn Model

This machine learning model was a continuation of 'World-Energy-Production vs GDP Machine Learning Tester' (https://github.com/zdiam/World-Energy-Production-vs-GDP-Machine-Learning-Tester) project, in which World Total GDP (USD) was compared against World Total Energy Production for the Years 1980-2021. The result was a fairly linear plot:

![](https://github.com/zdiam/World-Energy-Production-vs-GDP-Machine-Learning-Tester/blob/main/Reference%20Images/Initial%20Plot%20w%20Pred%20Line.png)

The next thought, which continued in this project, was to break down the data into countries and see if there is a real trend between GDP and Energy Production or if another factor was determing the relationship on the macro scale of the World. 

If there was a trend, a machine learing regression model could be used to predict the future energy production based on future GDP predictions from Organisation for Economic Co-operation and Development (OECD).

Energy Production per country for the years 1980-2021 was already obtained for an animated map showing the change: World-Wide-Energy-Usage-R-Viz (https://github.com/zdiam/World-Wide-Energy-Usage-R-Viz). GDP data was pulled from https://data.worldbank.org/indicator/NY.GDP.MKTP.CD?end=2021&start=1960, and then manupilated to merge with the Energy Production data. 

Rather than troubleshoot different country labeling, inconsisent data was dropped via a left merge (GDP to Energy Production) providing ~6000 data rows for analysis.

The final plot of the dataset is:

![](https://github.com/zdiam/Energy-Production-GDP-Machine-Learning-Model/blob/main/Reference%20Images/Default%20Plot.png)

Which is a different view than the original World Wide plot. Although this data was not linear, for the sake of learning and exploring used 5 different machine learning models to try to find a solid prediction model. 

The models and their associated scores are:

### Decision Tree:

![](https://github.com/zdiam/Energy-Production-GDP-Machine-Learning-Model/blob/main/Reference%20Images/Decision%20Tree.png)


### Random Forest: 

![](https://github.com/zdiam/Energy-Production-GDP-Machine-Learning-Model/blob/main/Reference%20Images/Random%20Forest.png)


### Linear Regression:

![](https://github.com/zdiam/Energy-Production-GDP-Machine-Learning-Model/blob/main/Reference%20Images/Linear%20Regression.png)

### Isotonic Regression:

![](https://github.com/zdiam/Energy-Production-GDP-Machine-Learning-Model/blob/main/Reference%20Images/Isotonic%20Regression.png)

### KNeighbors:

![](https://github.com/zdiam/Energy-Production-GDP-Machine-Learning-Model/blob/main/Reference%20Images/KNeighbors.png)

With KNeighbors (with neighbors set to 10 as any more gave diminishing returns) being the highest score.

The KNeighbors model was then paired against the the prediction GDP from OECD for 4 countries.

The result:

![](https://github.com/zdiam/Energy-Production-GDP-Machine-Learning-Model/blob/main/Reference%20Images/Pred%20Block.png)


## Analysis

While the World Wide data painted a very clear picture, splitting into countries made it clear that there wasn't a real correlation. What does this mean? Likely, it means that there is a different factor or multiple different factors that contribute to Energy Production, and GDP is related indirectly. In plotting the Country distrubtion we see two major breakaways in China and the USA, but China is producing more energy without growing to the USA's GDP. Monetary presence is required to break away, but more money does not mean more energy production, which is exactly what the World Wide plot was describing.

Ultimately, GDP is not a strong enough correlation to Energy Production to produce a reliable machine learning model. Breaking down the data was essential to help show this conclusion. While the model isn't usable realistically, it was an excellent learning opportunity and I can walk away from the project with a stronger understanding of data wrangling, machine learning, and data analysis.
