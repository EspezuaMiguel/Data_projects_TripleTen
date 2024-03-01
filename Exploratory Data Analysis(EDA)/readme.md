## **Project description**

For this project, you’ll work with data from Instacart.

Instacart is a grocery delivery platform where customers can place a grocery order and have it delivered to them, similar to how Uber Eats and Door Dash work. This particular dataset was[ publicly released](https://tech.instacart.com/3-million-instacart-orders-open-sourced-d40d29ead6f2) by Instacart in 2017 for a[ Kaggle competition](https://www.kaggle.com/c/instacart-market-basket-analysis/overview). Although the original dataset is no longer available on the Instacart website, we’ve created CSV files that contain a modified version of that data. Download these files and use them for your project.

The dataset we've provided for you has been modified from the original. We've reduced the size of the dataset so that your calculations run faster and we’ve introduced missing and duplicate values. We were also careful to preserve the distributions of the original data when we made our changes.

Your mission is to clean up the data and prepare a report that gives insight into the shopping habits of Instacart customers. After answering each question, write a brief explanation of your results in a markdown cell of your Jupyter notebook.

This project will require you to make plots that communicate your results. Make sure that any plots you create have a title, labeled axes, and a legend if necessary; and include `plt.show()` at the end of each cell with a plot.

## Conclusion

In this project, we worked with data from Instacart, a grocery delivery platform. The dataset provided for analysis had been modified from the original, with reduced size and introduced missing and duplicate values. Despite these modifications, the distributions of the original data were preserved.

### Data Observations:

- **instacart_orders.csv**: This file includes six columns, with the 'days_since_prior_order' column indicating missing values.

- **products.csv**: The 'product_name' column has missing information.

- **aisles.csv**: Two columns were found with no missing data.

- **departments.csv**: It was observed that there are 21 departments.

- **Order_products.csv**: The 'add_to_cart_order' column shows missing values.

### Project Goal Achievement:

The project goal was successfully completed using Pandas to create dataframes from the provided dataset, despite the non-standard format of some CSV files. The `info()` method was utilized to check the status of the loaded files, including column names, number of rows, and data types.

Preprocessing steps were carried out to address duplicates, missing data, and data editing where necessary. Data analysis was performed, and distribution charts were created using bar and histogram plots. These analyses provided insights into customer behavior, such as the most frequent time and day for orders and popular product selections.

The Pandas library proved instrumental in managing the dataset effectively, while matplotlib facilitated the creation of informative plots to visualize the data.

## Recommendations

1. **Data Standardization**: Standardize the CSV file formats to facilitate easier data loading and preprocessing in future analyses.

2. **Data Quality Improvement**: Address missing information in the 'product_name' column of the products dataset to ensure completeness and accuracy.

3. **Further Analysis**: Explore additional factors that may influence customer shopping habits, such as seasonal trends, promotional campaigns, and geographic variations, to gain deeper insights into customer behavior.

4. **Enhanced Visualization**: Experiment with different visualization techniques to present data findings more effectively and intuitively, enhancing the interpretability of insights derived from the analysis.

By implementing these recommendations, Instacart can continue to leverage data-driven insights to optimize its operations and enhance the shopping experience for its customers.



## **Data dictionary**

There are five tables in the dataset, and you’ll need to use all of them to do your data preprocessing and EDA. Below is a data dictionary that lists the columns in each table and describes that data that hold.



* `instacart_orders.csv`: each row corresponds to one order on the Instacart app
    * `'order_id'`: ID number that uniquely identifies each order
    * `'user_id'`: ID number that uniquely identifies each customer account
    * `'order_number'`: the number of times this customer has placed an order
    * `'order_dow'`: day of the week that the order placed (which day is 0 is uncertain)
    * `'order_hour_of_day'`: hour of the day that the order was placed
    * `'days_since_prior_order'`: number of days since this customer placed their previous order
* `products.csv`: each row corresponds to a unique product that customers can buy
    * `'product_id'`: ID number that uniquely identifies each product
    * `'product_name'`: name of the product
    * `'aisle_id'`: ID number that uniquely identifies each grocery aisle category
    * `'department_id'`: ID number that uniquely identifies each grocery department category
* `order_products.csv`: each row corresponds to one item placed in an order
    * `'order_id'`: ID number that uniquely identifies each order
    * `'product_id'`: ID number that uniquely identifies each product
    * `'add_to_cart_order'`: the sequential order in which each item was placed in the cart
    * `'reordered'`: 0 if the customer has never ordered this product before, 1 if they have
* `aisles.csv`
    * `'aisle_id'`: ID number that uniquely identifies each grocery aisle category
    * `'aisle'`: name of the aisle
* `departments.csv`
    * `'department_id'`: ID number that uniquely identifies each grocery department category
    * `'department'`: name of the department
