##Introduction
1)	This is an EViews code for selection of variables according to their pseudo out-of-sample forecasting performances measured by relative root mean squared error (RMSE).
2)	It rests on the work of Banerjee, A. and M. Marcellino (2006). Are there any reliable leading indicators for US inflation and GDP growth? International Journal of Forecasting 22 (1), 137-151.
3)	This code is written by Selen Andic using EViews 8 on 13/6/2014.
4)	Please cite Andic, S. and F. Ogunc. 2015. Variable selection for inflation: a pseudo out-of-sample approach. Central Bank of Turkey Working Paper No:15/06.

Estimation framework
1)	y: stationary dependent variable, x: stationary independent variable, L: lags, e:error term.
2)	General form of the model is a single equation: y=c+b1*L(y)+b2*L(x)+e.
3)	Lags of “y” and “x” variables are determined according to the Schwarz criteria.
4)	Your “x” data set can be as large as you want and can have ragged end.

How the code is run
1)	This code works with quarterly or monthly data.
5)	Make sure start date of your workfile (wf) matches the date of your first "y" observation.
6)	Make sure you do not have any missing values between the first and last observation of your "y" and "x" data.
7)	Paste your data in its stationary form(s) into an E-views wf.
8)	Name the dependent variable as "y". 
9)	For "x" variables, Quick> Empty Group. Paste your "x"  variables without names and close the group without saving. EViews will name your "x" series as "ser*".
10)	Download the .prg file that I have provided in this repository to your computer.
11)	Open the program: File>Open>Programs and choose the program.
12)	Declare your forecasting framework in section 2 of the code.
13)	Run the code quietly for faster results. 

Outputs after the code is run
1)	Performances according to criteria "results1" (RMSE-sum) are presented in "Table Results1".
2)	Performances according to criteria "results2" (outperform ratio etc.) are presented in "Table Results2"
3)	Results of "nbrbest" (for instance 5) variables are presented in "Table Results of Best"
4)	Relative RMSEs (RRMSE) of the best "nbrbest" variables according to "results1"  and "results2", and recursive forecasts of these variables are shown graphically.

Example
1)	I have provided an example workfile. 
2)  It includes “y” and 45 independent variables that will be used in forecasting. 
3)  You can use this workfile and the code to see how the code works and how the results are reported. If you choose to report the performances of 5 best variables,  is defined as scalar nbrbest=5 in the code, your final screen should look like this:
![alt text](https://github.com/selenandic/ms-beevision/blob/master/Example_final%20screen%20after%20the%20code%20is%20run.PNG)
