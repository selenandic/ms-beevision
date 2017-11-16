1)	This is an EViews code for selection of variables according to their pseudo out-of-sample forecasting performances measured by RMSE.

2)	It rests on the work of Banerjee, A. and M. Marcellino (2006). Are there any reliable leading indicators for US inflation and GDP growth? International Journal of Forecasting 22 (1), 137-151.

3)	How the code is run;
•	This code works with quarterly or monthly data.
•	Make sure start date of your wf matches the date of your first "y" observation.
•	Make sure you do not have any missing values between the first and last observation of your y and x data.
•	Paste your data in its stationary form(s) into a E-views wf.
•	Name the dependent variable as "y". 
•	For "x" variables, Quick> Empty Group. paste your "x"  variables without names and close the group without saving. Eviews will name your" x" series as "ser*".
•	Declare your forecasting framework, section 2.
•	Run the code quietly for faster results. 

4)	Estimation framework:
•	y: stationary dependent variable, x: stationary independent variable, L: lags, e:error term.
•	General form of the model: y=c+b1*L(y)+b2*L(x)+e.
•	Lags of y and x variables are determined according to the Schwarz criteria.

5)	Outputs after the code is run;
•	Performances according to criteria "results1" (RMSE-sum) are presented in "Table Results1".
•	Performances according to criteria "results2" (outperform ratio etc.) are presented in "Table Results2"
•	Results of "nbrbest" (for instance 5) variables are presented in "Table Results of Best"
•	RRMSEs of the best "nbrbest" variables according to "results1"  and "results2", and recursive forecasts of these variables are shown graphically.

6)	This code is written by Selen Andic on 13/6/2014.

7)	Please cite Andic, S. and F. Ogunc. 2015. Variable selection for inflation:a pseudo out-of-sample approach. Central Bank of Turkey Working Paper No:15/06.

