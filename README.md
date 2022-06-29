# Laptop Price Predictor Regressor.
### StreamLit Webapp Screenshots
![Price Predictor](.\images/Price-Predictor-1.png)

![Price Predictor](.\images/Price-Predictor-2.png)

**In this project we are creating a laptop Price predictor with the help of Machine Learning Models.**

**we have used several Models**
* Linear Regresson
* Ridge
* Lasso
* SVMRegressor
* DecesionTreeRegressor
* RandomForestRegressor
* Boosting
    - AdaBoost
    - Gradient Boost
    - Xg Boost

* Ensamble
    - Voting Regressor
    - Stacking Regressor
    

After Applying all the Models we found that the Random Forest has highest R2 Score.

```python
# import for sklearn models.
from sklearn.linear_model import LinearRegression,Ridge,Lasso
from sklearn.neighbors import KNeighborsRegressor
from sklearn.tree import DecisionTreeRegressor
from sklearn.ensemble import RandomForestRegressor,GradientBoostingRegressor,AdaBoostRegressor,ExtraTreesRegressor
from sklearn.svm import SVR
from xgboost import XGBRegressor

```
**After Applying All The Models Export the model and used it in Webapp**

```python

# Export the model
import pickle
pickle.dump(df,open('../model/df.pkl','wb'))
pickle.dump(pipe,open('../model/pipe.pkl','wb'))

# Import the model
pipe = pickle.load(open('../model/pipe.pkl','rb'))
df = pickle.load(open('../model/df.pkl','rb'))
```

**Created a webapp within 20 minutes with streamlit**

```python
# To use the model in the webapp all you have to install is:
pip install streamlit
pip install pickle
pip install numpy
```
