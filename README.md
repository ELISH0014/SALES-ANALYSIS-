# E COMMERCE  SALES-ANALYSIS

## Table  of content

- [Project overview ](#project-overview)
- [DATA-SOURCE](#data-source)
- [Tools](#tools)
- [Result](#result)
- [Recommendations](#recommendations)
- [Limitations](#limitations)

### Project Overview

This data analysis Project aims to provide insights into the sales performances of an E-COMMERCE company . By analyzing various aspects of the sales data , we seek to identify trends , make data driven recommendations , study their customers and gain a deeper understanding of the companys performance . 

### DATA SOURCE 

Sales Data : The primary dataset used for this analysis is the "Train.csv(440.46 kB)" containing detailed information about each sale made by the company .

### Tools 

- Excel - Data cleaning , Data filtering / sorting , graphical representation
        - [Download here](https://microsoft.com)
- SQl server  - Data analysis [Download here](https:sql.com)


  ### Data cleaning / preparation

In the initial data preparation phase , we performed the following Task:
   - Data loading and inspection
   - Handling missing values
   - Data cleaning / Arrangement


   
### Exploratory Data Analysis 
-  does the Total cost of Product  depend on mode of shipment ?
-  which product category yields greater income  generation higher income ?
-  Is Customer query  being answered?
-  If Product importance is high. having higest rating or being delivered on time ?
-  Does the discount apply based on prior purchase ?

  ### Data Analysis 

  Include some intresting code/features worked with 
  ```sql
 
 SELECT * from table 1
where product form = 'medium';

SELECT ID , Warehouse_block , Mode_of_Shipment , Customer_rating , Weight_in_gms  FROM  train.`sql...`
WHERE Customer_rating ='5'
ORDER BY Weight_in_gms DESC
LIMIT 50;

select Warehouse_block , max(Weight_in_gms) as maximum FROM  train.`sql...`
 group by Warehouse_block
 having max(Weight_in_gms);

 select gender , max(Cost_of_the_Product) as MAXIMUM_EXPENDITURE FROM train.`sql...`
 GROUP BY GENDER 
 HAVING max(Cost_of_the_Product)
 ORDER BY 2 DESC;

 SELECT max(Prior_purchases) 
from train.`sql...`;


select  ID , Prior_purchases , max(Discount_offered) AS MAX_DISCOUNT
FROM train.`sql...`
GROUP BY  ID , Prior_purchases 
HAVING MAX(Discount_offered) 
order BY 3 DESC ;

SELECT distinct (mode_of_shipment) as 'list of tansportation' 
from train.`sql...`;

select * from train.`sql...`
where Customer_care_calls > 3 AND Product_importance = 'high';

select ID , Cost_of_the_Product , customer_care_calls , customer_rating from train.`sql...`
where Customer_care_calls > 3 AND Customer_rating = 5
order by Cost_of_the_Product desc;

```

### Result 

The Analysis results are summarized as follows :
1. The bulk of the companys sale comes from the small category products .
2. product category "low" is the best perfoming product in terms of sales .
3. Discount given is not based on the amount of  prior purchases made .
4. 
   

   ### Recommendations

   - Invest in marketting and production of products in  category 'low'
   - Discount given should be proportional to numbers of previoius purchases .
  
### Limitations 

- There was absence of cost of production
- I had to remove all zero values 


   

  

  

  
 


  
