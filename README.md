# Demand prediction of consumable retail products

## Problem Description

* A large company that manufactures eatables, delivers them through a group of suppliers to retailers of different kinds all over the country. One of the company’s recent sustainable initiatives was to sell eatable products with no preservatives. These consumables have a shelf life of one week.
* The company, to ensure the quality of its products on retailers’ shelves, creates a program to buy back the remaining products on the shelves of the retailers post expiry (one week). This has significantly increased the company’s operation costs and is also affecting its gross margins.
* The company has hired you as a data science consultant and provides you with 5 weeks of data. You are now supposed to predict the demand for various products across for the next two weeks. You are also supposed to produce a report using your machine learning model and the 5th week’s data as a validation set to analyze the potential loss in revenue / gain in operational costs.

## Data Description

* experiment_week : The column identifying the week during which the data was collected
* channel_type : The channel through which the product is being sold, such as ‘Warehouse Retailers’, ‘grocery stores’, etc.
* num_units_sold_in_week: ​Number of units of the particular product sold that week
* sales_revenue_in_week: ​Revenue that the company made by the sale of the products
* num_units_returned: ​The number of units returned by the retailer for the products sold that week. (Sometimes due to the retailers stocking the products for longer and returning products purchased from prior weeks this variable might be higher than the num_units_sold_in_week)
* returned_units_revenue_loss: ​The amount of money that the company paid the retailer for returning the product
* store_identifier: ​Anonymized identifier of the retailer
* product_identifier: ​Product key from the database
* category_of_route: ​Type of route used by the supplier to deliver the
products
* supplier_identifier: Anonymized identifier of the supplier distributing the
product to the retailer. Most stores have a single supplier, sometimes a
store might have two suppliers.
* demand_projection: ​This is the target attribute, that is supposed to generate by subtracting the number of units returned from the number of units sold.

## Task performed

* Data analysis and visualisation on train data.
* Build a machine learning model, which should predict the demand projection for the records in the test data with columns 'experiment_week', 'channel_type', 'store_identifier', 'product_identifier', 'category_of_route' and 'supplier_identifier'.
* Analyze the predictions of the model, using 4 weeks data, to report the loss of revenue for week 5 if the model was deployed.

## Evaluation Metric:
* The evaluation metric used is Root Mean Squared Error (RMSE)
* Achieved RMSE of 10.2 on train data and 11.9 on test data
