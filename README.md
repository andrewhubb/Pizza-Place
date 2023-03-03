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
3. I then clicked on the content column and selected Remove Columns from the ribbon.
4. Then I selected Remove other columns leaving us just the content column.
5. I then clicked on the double down arrows in the column header to expand the file contents.
6. Then I clicked on OK from the Combine Files window.
