# CurveFrcst-Using-ManifoldLrn
ISyE8900 Project Project  
Chi Zhang  
Georgia Institute of Technology  

Abstract

This project proposes a nonparametric approach for the modeling and forecasting of weekly interest rate spread curves by using nonlinear dimension reduction, such as the locally linear embedding (LLE). We mainly focus on two objective spread curves: Swap Spread (LIBOR substract Treasury) and Basis Spread (LIBOR substract SOFR). Benchmarking on its linear dimension reduction counterparty -- principle component analysis (PCA) -- we show the LLE-based framework yields a higher out-of-sample forecast accuracy for specific underlying tenors as well as a better profit and loss (PnL) profile in backtesting various systematic term structure trading strategies.  

Data  
The following cleaned dataset are stored in corresponding .xlsx files. The current experiement is based on the period 2018.10 - 2020.10. New data will be kept adding.  
US Treasury Zero Yield Curve -- Treasury_clean.xlsx;  
US 3m LIBOR/Swap Zero Yield Curve --LIBOR_clean.xlsx;  
3m SOFR Zero Yield Curve -- SOFR_clean.xlsx;    
USD OIS Zero Curve -- OIS_clean.xlsx;    


Programs  
CurveBuild.ipynb:  
(1) Data cleaning  
(2) Curve building  
DmnsRdct_StateFrcst.ipynb:  
(1) Data visualization of low-dim embedding using various dimension reduction methods  
(2) Toy model of Kalman filter implementation (require Kalman_filter.py)  
(3) Randomness test for low-dim embedding  
(4) Implementation of LLE transform and inverse-transform  
(5) Backtesting engine for PCA+ARMA and LLE+ARMA models  

Problem formulation  

(1) dimension reduction  
(2) forecasting in the reduced dimension  
(3) mapping back to the original space.  

Paper:    
[1] Chen J, Deng S J, Huo X. Electricity price curve modeling and forecasting by manifold learning[J]. IEEE Transactions on Power Systems, 2008, 23(3): 877-888.  
[2] Huo X, Ni X S, Smith A K. A survey of manifold-based learning methods[J]. Recent advances in data mining of enterprise data, 2007: 691-745.  
[3] Blaskowitz O J. A forecast evaluation of PCA-based adaptive forecasting schemes for the EURIBOR swap term structure[D]. Christian-Albrechts Universität Kiel, 2009.  
[4] Sack B P, Wright J, Gürkaynak R. The US Treasury yield curve: 1961 to the present[R]. Board of Governors of the Federal Reserve System (US), 2006.  
[5] Kondratyev A. Learning curve dynamics with artificial neural networks[J]. Available at SSRN 3041232, 2018.  
[6] Chen J, Huo X. A hessian regularized nonlinear time series model[J]. Journal of Computational and Graphical Statistics, 2009, 18(3): 694-716.
  
 
