# CurveFrcst-Using-ManifoldLrn
ISyE8900 Project  
Chi Zhang  
Georgia Institute of Technology  

Abstract

This project proposes a nonparametric approach for the modeling and forecasting of weekly interest rate spread curves by using nonlinear dimension reduction, such as the locally linear embedding (LLE). We mainly focus on two objective spread curves: Swap Spread (LIBOR substract Treasury) and Basis Spread (LIBOR substract SOFR). Benchmarking on its linear dimension reduction counterparty -- principle component analysis (PCA) -- we show the LLE-based framework yields a higher out-of-sample forecast accuracy for specific underlying tenors as well as a better profit and loss (PnL) profile in backtesting various systematic term structure trading strategies.  

Data  

The following dataset are stored in corresponding .xlsx files. The current experiement is based on the period 2018.10 - 2020.10. New data will be kept adding.  
Original:  
Parameters of Treasury Term Structure Models -- feds200628_till210319.xlsx;  
US 3m LIBOR/Swap Zero+Forward Yield Curve -- WklyLIBOR.xlsx;  
3m SOFR Zero+Forward Yield Curve -- WklySOFR.xlsx;    
USD OIS Zero+Forward Curve -- WklyOIS.xlsx;  
fed funds rate time series -- FFR_daily;  
1yr breakeven inflation rate time series -- inflation_daily;  
Cleaned:  
US Treasury Zero Yield Curve -- Treasury_clean.xlsx;  
US 3m LIBOR/Swap Zero Yield Curve --LIBOR_clean.xlsx;  
3m SOFR Zero Yield Curve -- SOFR_clean.xlsx;    
USD OIS Zero Curve -- OIS_clean.xlsx;    

Programs  

CurveBuild.ipynb:  
(1) Data cleaning and re-sampling  
(2) Curve building  
DmnsRdct_StateFrcst.ipynb:  
(1) Data visualization of low-dim embedding using various dimension reduction methods  
(2) Toy model of Kalman filter implementation (require Kalman_filter.py)  
(3) Randomness test for univariate low-dim embedding  
(4) Implementation of LLE transform and inverse-transform  
(5) Backtesting engine for systematic trading strategies using PCA+ARMA and LLE+ARMA models  
NumerExperim.ipynb:  
(1) Calculate credit risk premium 3m LIBOR- 3m SOFR, liquidity risk premium EFFR – inflation  
(2) Regress swap spd on the two risk factors for each tenor    
(3) Simulate the residual as O-U process for each tenor    
(4) Recover the simlulated swap spd curve    
(5) Run multi-stage forecasting framework for swap spd curve from script 2    


Problem formulation  

(1) Dimension reduction  
(2) Forecasting in the reduced dimension    
(3) Mapping back to the original space  
(4) Performance evaluation    

Paper:  
[1] Chen J, Deng S J, Huo X. Electricity price curve modeling and forecasting by manifold learning. IEEE
Transactions on Power Systems, 2008, 23(3): 877-888.
[2] Huo X, Ni X S, Smith A K. A survey of manifold-based learning methods. Recent advances in data mining
of enterprise data, 2007: 691-745.
[3] Chen J, Huo X. A hessian regularized nonlinear time series model. Journal of Computational and Graphical Statistics, 2009, 18(3): 694-716.
[4] Kondratyev A. Learning curve dynamics with artificial neural networks. Available at SSRN 3041232,
2018.
[5] Zhang Z, Zha H. Principal manifolds and nonlinear dimensionality reduction via tangent space alignment.
SIAM journal on scientific computing, 2004, 26(1): 313-338.
[6] Li S, Lin H, Zang Z, et al. Invertible Manifold Learning for Dimension Reduction. arXiv preprint
arXiv:2010.04012, 2020.
[7] Blaskowitz O J. A forecast evaluation of PCA-based adaptive forecasting schemes for the EURIBOR swap
term structure. Christian-Albrechts Universit¨at Kiel, 2009.
[8] Sack B P, Wright J, G¨urkaynak R. The US Treasury yield curve: 1961 to the present. Board of Governors
of the Federal Reserve System (US), 2006.
[9] Diebold F X, Li C. Forecasting the term structure of government bond yields. Journal of econometrics,
2006, 130(2): 337-364.Authors’ names blinded for peer review
16 Article submitted to Management Science; manuscript no. MS-0001-1922.65
[10] Ang A, Piazzesi M. A no-arbitrage vector autoregression of term structure dynamics with macroeconomic
and latent variables. Journal of Monetary economics, 2003, 50(4): 745-787.
[11] Cooper I, Priestley R. Time-varying risk premiums and the output gap. The Review of Financial Studies,
2009, 22(7): 2801-2833.
[12] Ludvigson S C, Ng S. Macro factors in bond risk premia. The Review of Financial Studies, 2009, 22(12):
5027-5067.
[13] Sorensen E H, Bollier T F. Pricing swap default risk. Financial Analysts Journal, 1994, 50(3): 23-33.
[14] Grinblatt M. An analytic solution for interest rate swap spreads. International Review of Finance, 2001,
2(3): 113-149.
[15] Litterman R, Scheinkman J. Common factors affecting bond returns. Journal of fixed income, 1991,
1(1): 54-61.
  
 
