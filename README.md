# PizzaPlace
This is the Power BI PBIX File containing my analysis of the Maven Analytics Pizza Place Data Playground I have also included the Data CSV file.

### Data Source ###
The source for the data is the Pizza Place Sales from the Maven Analytics Data Playground the link to the playground is here.
[Maven Analytics Data Playground](https://www.mavenanalytics.io/data-playground)

### Process Followed ###
1. I used get data and selected folder as a data source. 
2. I then browsed to the folder where the files were stored and selected that folder and clicked OK.
3. Then I selected Trnsform Data from the options that appear in the popup window showing the file names.
4. This opened up the Query Editor windoow and from there I selected the query which is the folder name in my case called "pizza_sales".
5. I then used right click to open a menu and selected reference this created a new query in my case called "pizza_sales (2)".
6. I then selected the first query and used right click and selected reference to create a new query called "pizza_sales (3)".
7. I repeated steps 5 and 6 two more times so there are 5 queries up to "pizza_sales (5)".
  * The reason for doing it this way is so that in the future if you move the report and files to a different folder you only have to update the first query and not have to update each report.
8. I renamed the first query to "pizza_sales (source)" by selecting the query and using right click and selecting rename from the menu.
9. I then renamed the next query (in my case "pizza_sales (2)") to orders.
10. Then I renamed the next query after that (in my case "pizza_sales (3)") to be order_details.
11. Then the next query after that (in my case "pizza_sales (4)") was renamed to be pizzas.
12. The last query (in my case "pizza_sales (5)") was renamed to pizza_types.

#### Now we are ready to start preparing the queries for use.

1. I selected the orders query and selected Keep Rows from the ribbon above.
2. I then selected Keep Top Rows and entered 1 as the number of rows to keep into the popup window as we only need the first row as we are only interested in the orders file.
3. I then clicked on the Content column and selected Remove Columns from the ribbon.
4. Then I selected Remove other columns leaving us just the content column.
5. I then clicked on the double down arrows in the column header to expand the file contents.
6. Then I clicked on OK from the Combine Files window. This expanded the orders.csv file. You will notice a query group has been created called "Tranform File from orders" with a helper queries subgroup. Do not worry about these as they are to help with opening the csv file in power query.
7. Next I clicked on order_details and selected Keep Rows from the ribbon above.
8. From the popup menu that appears I selected Keep Range of Rows and entered 2 as the first row and 1 as the number of rows.
9. I then clicked on the Content column and selected Remove Columns from the ribbon
10. Then I selected Remove other columns leaving us just the content column.
11. I then clicked on the double down arrows in the column header to expand the file contents.
12. Then I clicked on OK from the Combine Files window. This expanded the order_details.csv file. You will notice a query group has been created called "Tranform File from order_details" with a helper queries subgroup. 
13. Next I clicked on pizzas and selected Keep Rows from the ribbon above.
14. From the popup menu that appears I selected Keep Range of Rows and entered 3 as the first row and 1 as the number of rows.
15. I then clicked on the Content column and selected Remove Columns from the ribbon
16. Then I selected Remove other columns leaving us just the content column.
17. I then clicked on the double down arrows in the column header to expand the file contents.
18. Then I clicked on OK from the Combine Files window. This expanded the pizzas.csv file. You will notice a query group has been created called "Tranform File from pizzas" with a helper queries subgroup. 
19. Next I clicked on pizza_types and selected Keep Rows from the ribbon above.
20. From the popup menu that appears I selected Keep Bottom Rows and entered 1 as the  number of rows.
21. I then clicked on the Content column and selected Remove Columns from the ribbon
22. Then I selected Remove other columns leaving us just the content column.
23. I then clicked on the double down arrows in the column header to expand the file contents.
24. Then I clicked on OK from the Combine Files window. This expanded the pizza_types.csv file. You will notice a query group has been created called "Tranform File from pizza_types" with a helper queries subgroup. 
25. As can be seen the column names are not correct we can see the column names in the top row of the query. To fix this we need to select the Use First Row as Headers from the ribbon above is located in the column next to the Group By option in the ribbon bar. I selected this and the first row moved up to be the column headers.

