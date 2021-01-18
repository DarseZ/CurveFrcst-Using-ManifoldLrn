# CurveFrcst-Using-ManifoldLrn
ISyE8900 Project Proposal
Chi Zhang
Georgia Institute of Technology

Abstract
In this project, we implement a nonparametric approach for modeling curves in the FICC market using various manifold learning methods.

Data
US Treasury Zero Yield Curve;
US Treasury Forward Rate Curve;
US 3m LIBOR/Swap Zero Yield Curve;
US 3m LIBOR/Swap Forward Rate Curve;
3m SOFR Zero Yield Curve;
3m SOFR Forward Rate Curve


Problem formulation and Application
Fetching or bootstrapping curves if necessary.

Dimension deduction:
Start from baseline classical methods (PCA), then move to advanced methods according to the survey presentation published by Dr. Huo in 2004: semi-classical methods (MDS), manifold searching methods (LLE).
Time series forecasting for each univariate low dimensional coordinate:
Start from ARIMA family models, then add Kalman filter or more general state space models to refine and finalize this AR type forecasting engine.
