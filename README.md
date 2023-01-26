


   
  



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







![](https://github.com/zdiam/Energy-Production-GDP-Machine-Learning-Model/blob/main/Reference%20Images/Pred%20Block.png)


# Thermal-Expansion-Loop-Bend-Calculator

This Thermal Expansion Calculator will calculate the thermal expansion of a steam system straight pipe run for stresses due to the change in temperature. The calculator uses the ASHRAE standards for loop and z bend sizing but takes it a step further to provide more accurate values, quicker calculations, and with printable outputs to a .csv file. Currently the calculator supports carbon steel piping with an atmopsheric pressure at sea level.


## Walkthrough:

1) Download contents in the build folder.
2) Upon running the program view first popup:
![image](https://user-images.githubusercontent.com/120227829/209484167-1f9b8433-be51-4773-b327-611d59bd0c44.png)
3) Enter:
   - PSIG of the Steam System (*the calculator manually adds the typical sea level atmposheric pressure of 14.696 psi and adjustments to this value must be made to the        Gauge Pressure at the current time*).
   - The straight length of pipe in which the thermal expansion is being calculated (*refer to reference images folder for some excerpts from the ASHRAE 2016                 Fundamentals book*).
   - The Outside Diameter of the pipe (*image to the side carbon steel pipe data*).

**For this example we will use 80 PSIG, 150 feet of straight pipe length, and 6" pipe (*6.625 OD standard*)**

![image](https://user-images.githubusercontent.com/120227829/209484417-332a7d4a-cd3b-4c85-9061-d5e83696aabd.png)

4) Hit 'Run' button.
5) View next popup with output values:
![image](https://user-images.githubusercontent.com/120227829/209484469-1f144c75-60c7-4757-8962-1848d24fff88.png)
6) Press 'Print!' button to export the output values to a .csv file.
   - The values printed correlate the reference images on the right:, and the expansion loop width, height, and total are 
     - The Z-Bend length is the 'L' value for the "Z-Bend Reference Image".
     - The Expansion Loop width and height are the 'W' and 'H' values respectively from the "Expansion Loop Reference Image". The loop length is given for reference but is equal to 2H + W.
   - The output file will automatically save in the same file location as the build. The output files as saved as 'YYYY-MM-DD_*entered PSIG* PSI_*entered length* Length.
   - Our example problem will save as: ![image](https://user-images.githubusercontent.com/120227829/209484576-137229ae-9e47-4eca-a21d-30ff4f4a9bab.png)

7) Press the 'Close' button to end the program.
