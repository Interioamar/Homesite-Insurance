### **Homesite Insurance Quote Conversion Prediction**

**Introduction**

![MVU-MSDSCI-2020-Q1-Skyscraper-Predictive-Analytics-in-Insurance-Types-Tools-and-the-Future-header-v1-1000x523](https://user-images.githubusercontent.com/107593984/174439218-57d93183-2c8b-4e37-9727-9e5d4c20c4f5.jpg)

Homesite is a US based online Insurance company which oﬀers insurance coverage for Home, Renters, Auto, Small business etc. It is the one of the ﬁrst companies to enable customers to purchase home insurance directly online, during a single visit. Homesite tackles in ﬁnding faster and smarter methods of improving how people buy insurance is the main jam. Website : <https://go.homesite.com/>

**Problem Statement**

1.  We need to predict which insurance quotes will actually result in the sale of a policy. In layman terms, whether a customer whom we are going to reach out will accept or reject the quote from the tele-marketer.
2.  The prediction will help the Homesite company to improve on the Insurance quote and will help to identify the right customer who will buy the policy so that more preference will be given to the predicted customers on the follow ups.

**Business Constraints**

1.  Incorrect prediction of interested customer will be loss to the company for the given quote. So higher penalty is given for False Negative identification/prediction of customer
2.  Model can take a few seconds to evaluate the result. As here more importance is given to correct prediction than the prediction execution

**About Data**

<https://www.kaggle.com/competitions/homesite-quote-conversion/data>

This dataset represents the activity of a large number of customers who are interested in buying policies from Homesite. The provided features are anonymized and provide a rich representation of the prospective customer and policy

-   train.csv — the training set, contains QuoteConversion_Flag
-   test.csv — Input dataset to predict the conversion of customer

Conversion refers to the identified customer bought the quoted policy by Homesite company

General information about the dataset:

1.  Total Number of input columns =298
2.  Target column : “QuoteConversion_Flag” (having binary values)
3.  Numerical columns: 271 features including target column
4.  Categorical columns: 27 columns
5.  Date column : 1 (Original_Quote_Date)

Total number of data points in train.csv ﬁle are : 260753

Total number of data points in test.csv ﬁle are : 173836

**Features description:**

1.  QuoteNumber: It is a customer identiﬁcation Number and is unique to each customer
2.  Original_Quote_Date : It is the date when the customer receives the quote for policy which he/she looking to buy
3.  QuoteConversion_Flag: This is the target ﬁeld which tells about whether a customer bought the policy which is quoted.
4.  Other ﬁelds are : Fieldxx, CoverageFieldxx, SalesFieldxx, PersonalFieldxx, PropertyFieldxx, GeographicFieldxx. Where these column gives information about Personal, Property & Geographic Field of the customer

**Performance Metric**

This is a Binary classiﬁcation problem. The metric for evaluation in Kaggle is **Area under the ROC curve**.

For the converted customers, Target label for **QuoteConversion_Flag** column is assigned as 1 and 0 for non-converted customers

Other Metrics: Confusion Matrix,F1 score can be used since the dataset is imbalanced where 81% of the quotes are not converted in the train dataset
