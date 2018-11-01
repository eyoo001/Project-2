# Project 2 - Ames Housing Data and Kaggle Challenge


## Data Science Question - 

Can housing prices be predicted based on their features in order to make business decisions for banks regarding houses defaulting on their mortgages? The model should advise the predicted pricing based on weighted values (features that contribute to price more significantly will have a heavier weight than those that do not contribute as much)which can then be used to inform business decisions for the bank/lender to determine whether to pursue the debt or sell off to third party debt collection agencies. 


## The Process

This dataset had 79 columns of features along with over 2000 rows of data. The 79 features consisted of both numerical (integer, float) types as well as categorical data (objects). Some features were input in the dataframe as numerical (e.g. number of rooms, number of baths) and had to be changed into categorical types for better interpretability of the data.

The cleaning process involved dropping unnecessary features (either due to collinearity/correlation to other features, lack of sufficient meaningful data, or other reasons), filling in the null/NaN values for missing data appropriately, and creating dummy columns/one-hot encoding the categorical data. I used a series of histograms and scatterplots against SalesPrices (the y-value), as well as against each other to quickly/briefly identify any patterns. 

The models were created using the SciKitLearn Pipeline feature - the Variance Threshold, StandardScaler, and regression model (Lasso, Ridge, Linear) were applied all in one process in order to streamline efficiency and code. Features were reduced based on their correlation to the SalesPrice column.

I then input the Kaggle test data against my models to produce predicted values. These were submitted online and garnered an RMSE of 42k (via Lasso) to 45k (via Linear)


| feature | weight |
| --- | --- |
| Overall Qual | 15866.938512459916 |
| Gr Liv Area | 15223.831436673501 |
| Full Bath_2 | -11274.976773324026 |
| Kitchen Qual_TA | -10991.701165869368 |
| Overall Qual_9 | 9398.535211256869 |
| Full Bath | 9145.887260997979 |
| Kitchen Qual_Gd | -8891.852202536134 |
| Garage Area | 8209.726500831084 |
| Bsmt Exposure_Gd | 6896.378268622677 |
| Exter Qual_TA | -6056.826910595938 |
| Overall Qual_8 | 5645.053974019009 |
| Bsmt Full Bath | 5093.1305937215775 |
| Fireplaces | 4731.0281469773645 |
| Neighborhood_NridgHt | 4703.53162440803 |
| MS Zoning_RM | -4412.519242871176 |
| Full Bath_1 | -4086.4495518178396 |
| Sale Type_New | 3764.068170030818 |
| Half Bath_1 | 3594.8881393902343 |
| Mas Vnr Area | 3501.1997464945034 |
| Heating QC_TA | -3121.0928653176743 |
| Foundation_PConc | 3052.2478929923477 |
| Exter Qual_Gd | -2705.893827704976 |
| Central Air_Y | 2517.5136559343628 |
| Overall Cond_5 | -2492.915067091541 |
| Garage Type_Attchd | 2452.922657826292 |
| TotRms AbvGrd | 2082.8035163936065 |
| 1st Flr SF | 2060.4389499002555 |
| BsmtFin Type 1_GLQ | 1909.7977941685288 |
| Wood Deck SF | 1748.6736477899353 |
| BsmtFin SF 1 | 1744.5373883081118 |
