# CurveFrcst-Using-ManifoldLrn
ISyE8900 Project Proposal  
Chi Zhang  
Georgia Institute of Technology  

Abstract

In this project, we implement a nonparametric approach for modeling curves in the FICC market using various manifold learning methods.  

Data  

US Treasury Zero Yield Curve; US Treasury Forward Rate Curve;  
US 3m LIBOR/Swap Zero Yield Curve; US 3m LIBOR/Swap Forward Rate Curve;
3m SOFR Zero Yield Curve; 3m SOFR Forward Rate Curve;  
USD OIS Zero Curve; USD OIS Forward Curve;
 
Problem formulation and Application  

Fetching or bootstrapping curves if necessary.  
Dimension deduction:  
Start from baseline classical methods (PCA), then move to advanced methods according to the survey presentation published by Dr. Huo in 2004: semi-classical methods (MDS), manifold searching methods (LLE).  
Time series forecasting for each univariate low dimensional coordinate:  
Start from ARIMA family models, then add Kalman filter or more general state space models to refine and finalize this AR type forecasting engine.  

Files:  

Paper:  
Chen,Deng,Huo.pdf: Electricity Price Curve Modeling and Forecasting by Manifold Learning  
Gurkaynak,Sack,Wright.pdf: The U.S. Treasury Yield Curve: 1961 to the Present  
Huo,Ni,Smith.pdf: A Survey of Manifold-Based Learning Methods  

Dataset:  
WklyOIS.xlsx 
WklyLIBOR.xlsx  
WklySOFR.xlsx  
feds200628.csv  

Source Code:  
