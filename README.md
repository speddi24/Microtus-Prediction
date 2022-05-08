# Microtus-Prediction
Microtus Data- Classification of Multiplex and Subterranean Species of Microtus Specimen.

*Microtus* data from *Flury* package consists of data of two different species of Microtus, M.multiplex and M.subterraneus which are difficult to distinguish morphologically. The Microtus data consists of eight morphometric variables measured using Nikon measure-scope and dial calipers. The data set has records of 288 specimens out of which 89 were analyzed and their species was identified. Remaining 199 specimen were grouped as unknown and are to be distinguished into respective species based on the morphometric variables. The 9 variables include Group(a factor with levels multiplex, subterraneus, unknown), MlLeft( width of upper left molar 1-0.001mm),M2Left (width of upper left molar 2-0.0001mm),M3Left(width of upper left molar 3-0.001mm),Foramen(Length of incisive foramen-0.001mm),Pbone(Length of palatal bone-0.001mm),Length(condylo incisive length or skull length-0.01mm),Height(skull height ablove bullae-0.01mm),Rostrum(skull width across rostrum-0.01mm).Generalized linear model will be fit and used to identify these unknown species.

Refer the.RMD file for Exploratory Data Analysis and Feature Selection.

  Microtus data with records of Microtus specimen is used for the analysis. Data set with 89 specimen grouped into multiplex and subterranean is used as Training set and remaining Specimen of unknown origin is used as test data. Exploratory data analysis show that there are no missing values, and a non linear correlation between the Group variable and other variables. Feature selection is done using different methods like subset selection using *regsubsets()* function, Step selection using Forward, Backward and Stepwise directions, Quadratic models using polynomial terms, linear models with all variables and only intercept.The Forward selection, backward selection and Quadratic model with 3 variables have lower AIC values of 28,27,7 and 26.1 and were further analyzed. The p values of Backward model were not significant at 95% confidence interval except for the M1Left feature and was rejected. Analysis of Variance of the remaining two models are marginally significant. However, the 10 fold cross validation of these models showed a lower error rate of 4.49% for model obtained from Forward selection compared to the Quadratic model that had 8.99% error rate.The simple linear model obtained from Forward selection process is used to predict the test data.121 specimen were classified as multiplex species and 78 specimen were classified as subterranean species.
  
