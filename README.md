# xgboostExtension
xgboost Extension for Easy Ranking &amp; Leaf Index Feature

Related xgboost issue: [Add Python Interface: XGBRanker and XGBFeature#2859](https://github.com/dmlc/xgboost/issues/2859)

As we know, Xgboost offers interfaces to support Ranking and get TreeNode Feature.
However, the example is not clear enough and many people leave their questions on StackOverflow about how to rank and get lead index as features.

Now xgboostExtension is designed to make it easy with sklearn-style interfaces.


For Python Package:

    XGBRanker  : Give rank scores for each sample in assigned groups. 
                 The scores are valid for ranking only in their own groups. 

    XGBFeature : Give the index of leaf in trees for each sample. 
                 XGBFeature is very useful during the CTR procedure of GBDT+LR. In addition, it's better to take the index of leaf as features but not the predicted value of leaf. Firstly, the predicted values of leaves are as discrete as their index. Secondly, the predicted values of leaves like [0.686, 0.343, 0.279, ... ] are less discriminant than their index like [10, 7, 12, ...]. So we take the index as features. 


The version of XGBoostExtension always follow the version of compatible xgboost.
