Convergence in economic output between European countries
==========================================================
Laurie Peeters, Sandra van der Schaaf, Dian van Rooi 
-----------------------------------------------------
January 31st, 2017

This paper aims to empirically compare convergence of different regions in the European Community between 1980 and 1984 and 1985 and 1989. 
Our research is loosely based on the paper of \href{http://web.b.ebscohost.com/ehost/pdfviewer/pdfviewer?sid=2b519a94-f685-4d04-8e5f-5fdb94e89ef5\%40sessionmgr101&vid=1&hid=116}{Neven and Gouyette (1995)}. 
This study, as well as ours, uses data on GDP per capita derived from the world development indicators of the \href{https://www.kaggle.com/worldbank/world-development-indicators}{World Bank}.
However, our north region will be compiled from data of The Netherlands, Germany and Finland and the south region will consist of Italy, Greece and Spain.
Also, a different model will be used to analyze the dataset.
Finally, our data analysis will be carried out in Python to report the findings in a transparent way and make it easier to verify and/or reproduce them by others.

1. Question
==========

Has there been convergence between northern and southern countries in Europe between 1985 and 1989?

1.1 Motivation
-----------

Over the last few years, outcomes of traditional growth models have been more and more challenged by new research.
Mainly the prediction of these neoclassical models that output of different regions will converge over time towards a steady state has led to an increasing amount of criticism (\href{http://web.b.ebscohost.com/ehost/pdfviewer/pdfviewer?sid=2b519a94-f685-4d04-8e5f-5fdb94e89ef5\%40sessionmgr101&vid=1&hid=116}{Neven \& Gouyette, 1995}).
For instance, when taking into account some non-convexity in production or externalities arising from the accumulation of human capital, regional outputs per capita can in fact diverge.
Also agglomeration economies may result in centripetal forces and uneven growth patterns.
Therefore, the question arises whether traditional neoclassical models are still useful when predicting convergence and making policy related decisions.

Whether or not convergence is actually happening is of great importance for policy debates on EU's \href{http://ec.europa.eu/regional_policy/en/policy/what/investment-policy/}{Regional Policy}.
In case it turns out that there is indeed convergence, this means that neoclassical models are able to provide a decent overview of regional evolution.
According to \href{http://web.b.ebscohost.com/ehost/pdfviewer/pdfviewer?sid=2b519a94-f685-4d04-8e5f-5fdb94e89ef5\%40sessionmgr101&vid=1&hid=116}{Neven \& Gouyette (1995)}, this makes it harder for \href{http://ec.europa.eu/regional_policy/en/policy/what/investment-policy/}{Regional Policy} to justify its importance for economic efficiency.

1.2 Method
-------
We used data from the dataset 'World Development Indicators' by the \href{https://www.kaggle.com/worldbank/world-development-indicators}{World Bank}. 
This dataset contains more than thousand annual indicators for economic development for many countries in the world. 
For this research we used GDP per capita (current US\$).  
We will compare the northern and southern European countries by means of estimating the coefficient of the correlation between GDP per capita (current US\$) over the period of 1980 - 1984 and the period 1985 - 1989. 

{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 204,
   "metadata": {
    "collapsed": false
   },
   "outputs": [],
   "source": [
    "%matplotlib inline\n",
    "import numpy as np\n",
    "import pandas as pd\n",
    "import matplotlib.pyplot as plt\n",
    "import math\n",
    "import scipy as scipy\n",
    "import statsmodels.formula.api as smf\n",
    "import re\n",
    "plt.style.use('ggplot')"
   ]
  },

1.3 Answer
-----------

When we exclude Finland from our northern region, we can observe convergence between the northern (the Netherlands and Germany) and southern region (Italy, Greece and Spain) between 1985 and 1989. This convergence was not present during the period of 1980 - 1984.

1.4 Main assumptions
---------------------

When using an OLS regression, the following assumption are implied:
\begin{examples}
\item Linear relationship
\item Multivariate normality
\item No or little multicollinearity
\item No auto-correlation
\item Homoscedasticity
\end{examples}

1.5 Importing libraries
--------------------
To be able to run the model the following python packages were used:

2. Model
=========

We use our own method to see whether there is a shift in correlation between the years of 1985 - 1989 in terms of GDP per capita (current US\$). For the estimation we use the following estimation equation:

\begin{equation}
Y = \alpha + \beta (Y_{it}) + u_{it}
\end{equation}





3. Analysis
============

As mentioned above, Python was used to analyze the data. 

4. Results
========

GRAPH 

We can see in the graph that starting from 1985 GDP per capita is increasing for every country.
It can also be seen that Germany and the Netherlands are stagnating while Italy and Spain keep increasing.
Finland and Greece seem to be an exception in their region.
GDP per capita is still increasing in Finland in 1989 and appears to be constantly stagnating in Greece.

TABLES OF OLS REGRESSIONS

5. Conclusion
==============
The results show that there is indeed convergence between northern and southern countries in Europe between 1985 and 1989, however, only if Finland is excluded from the dataset. 
This could mean that the neoclassical models are perfectly able to make predictions and \href{http://ec.europa.eu/regional_policy/en/policy/what/investment-policy/}{Regional Policy} 

6. Discussion
=============

In 1987 the European Commission made equality one of their top priorities in its policies and started interfering more (\href{http://web.b.ebscohost.com/ehost/pdfviewer/pdfviewer?sid=2b519a94-f685-4d04-8e5f-5fdb94e89ef5\%40sessionmgr101&vid=1&hid=116}{Neven \& Gouyette, 1995}).
Unfortunately, our dataset is too short to be able to draw any conclusions on the consequences of these measures.
It will be interesting to study this in the future.
In case this research would observe a different pattern of convergence and would be able to relate this to the measures taken by the Commission, this would give an indication of the effectiveness of regional policy.

7. References
===============


\	\	\ Barro, Robert J., and X. Sala-I-Martin (1990). "Economic Growth and Convergence across the United States." Working Paper 3419. Cambridge, Mass.: National Bureau of Economic Research (August). 

European Commission. (2013). Retrieved from \url{http://ec.europa.eu/regional_policy/en/policy/what/investment-policy/}
   
Neven, D., and C. Gouyette (1995). Regional convergence in the European Community. \textit{Journal of Common Market Studies}, 33(1), 47. 

World Bank. (2016). World Development Indicators. Retrieved from \url{https://www.kaggle.com/worldbank/world-development-indicators/version/1}
