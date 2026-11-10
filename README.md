# Hybrid-sea-water-desalination-unit-Grid-search-optimization-
Python optimization code used in a school assignment. I was asked to solve the water problem in a remote island. 

Based on daily data given about the pv power production during 1 year and the speed of air at a wind turbine, the code optimizes a model of energy independent desalination units. The objective function minimizes the Levelized Cost of Water (LCOW) subject to a >=95% annual water demand coverage constraint.

The 4D Grid Search Algorithm, basically tries all the possible scenarios according to the parameters of your problem and collects the ones ( in our case 5 ) that follow
your required outputs. (in our case: the cheapest model in eyro/m^3 and close to 100% demand coverage) 

The core optimization relies on a 4D grid search over the following parameter space:
1. Desalination units (Count: 2-5)
2. Wind Turbines (MW: 0-25)
3. Solar PV capacity (kWp: 0-30,000)
4. Supplementary Tank Capacity (m³)

In the first part, the code runs a statistic analysis in order to confirm that the wind follows weihbull distribution (known in theory). Thats a nice addition to enhance the theoretical background of the assignment. 
In order to do so: Place the wind data file `D1_D100_3Years(2).xlsx` in the same directory as the script. (If the file is missing, the script will catch the `FileNotFoundError` and fall back to hardcoded Weibull distribution parameters).

Also, the pv solar data as well as cost and demand variables are to be changed according to your problems input data.

Libraries used: 
- numpy
- pandas
- scipy
- matplotlib
- openpyxl

Do not let your ego drag you into wrong battles. (i used Ai in some parts)
