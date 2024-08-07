# Virtual Machine (VM) Exercises

## :information_source: Read this before getting started
- The two exercises should not replicate the exact actions shown in your screencast. The goal of exercises is for learners to apply what was learned in the screencasts to new problems or situations. This is best pedagogical practice for retaining and building skills. For example, this can be done by using another dataset between screencasts and exercises or focusing on a different portion of the dataset.
- Power BI / Tableau specific: We can only run free versions of BI software in our virtual machine exercises. In the case of Power BI, make sure the exercises can run on [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) without any additional paid products. 
- Unsure what the scope of an exercise should be? Here's an [example](https://campus.datacamp.com/courses/introduction-to-power-bi/getting-started-with-power-bi?ex=14) from Introduction to Power BI. The first chapter of most DataCamp courses are free, so take a look at our [BI courses](https://learn.datacamp.com/courses?technologies=Tableau&technologies=Power%20BI) to get a feel for how we assess and guide learners.

## 1st VM Exercise

#### Dataset

- [ ] Add datasets used to the `datasets/` folder

#### Files

- [ ] **Initial**: Add file to the `exercises/`  folder with the name `ex-1-intial.twbx` or `ex-1-intial.pbix` or `ex-1-initial.yxmd`, depending if you are auditioning for a Tableau/Power BI/Alteryx course.
- [ ] **Solution**: Add file to the `exercises/`  folder with the name `ex-1-sol.twbx` or `ex-1-sol.pbix` or `ex-1-sol.yxmd`

#### Learning Objective

*Perform Value Lookup to get product details in orders table*

#### Context

*Let's explore the concept of value lookup. You have two tables: the data table and the dictionary table. The data table includes order details and the Product ID of the products that were ordered. The dictionary table, on the other hand, provides information about product category, subcategory and the name of the product. Your task is to enrich the data table by fetching the product name, category, and subcategory information from the dictionary table using a value lookup operation. This will allow you to analyze the orders table more comprehensively, as it will now contain additional information about products and their categories.*

#### Steps to be executed by the student (max 6)

- Step 1: Connect the orders table to the first port of the Value Lookup node
- Step 2: Connect the Product dictionary table to the second port of the Value Lookup node
- Step 3: Right click on the Value Lookup node and select “Configure” option to open the configuration dialog of the node
- Step 4: In the Lookup column select “Product ID”, similarly in the Key column select “ProductID”
- Step 5: In the Output section, keep the columns Category, Sub-Category, Product Name in the “Includes” list and push the “ProductID” column to the “Excludes” list as we already have the “Product ID” column in the data table
- Step 6: Now press “Ok” and check the output table, it will contain the orders data along with the columns from dictionary table  


#### Exercise question:
*Now that you have completed the value lookup, select the OrderID associated with the Product name - Xerox 1887*
- [ ] CA-2014-100293
- [ ] CA-2014-100090
- [ ] CA-2014-100328
- [ ] CA-2014-100363



## 2nd VM Exercise

#### Dataset

- [ ] Add datasets used to the `datasets/` folder

#### Files

- [ ] **Initial**: Add file to the `exercises/`  folder with the name `ex-2-intial.twbx` or `ex-1-initial.yxmd`, depending if you are auditioning for a Tableau/Power BI/Alteryx course.
- [ ] **Solution**: Add file to the `exercises/`  folder with the name `ex-2-sol.twbx` or `ex-2-sol.pbix` or `ex-1-sol.yxmd`

#### Learning Objective

*Perform Full Outer Join operation to get extensive details on products and orders*

#### Context

*You are given two tables: the Orders table and the Products table. The Orders table includes information such as order ID, product ID, and pin codes, while the Products table provides detailed information about various products. To gain a comprehensive understanding of the orders and the products that were ordered and those that were not, you are asked to perform a full outer join on these tables. This will create a new table that contains information on all orders and all products, allowing you to explore the range of products that were ordered and those that were not*

#### Steps to be executed by the student (max 6)

- Step 1: Connect the Orders table to the first port of the Joiner node and this table will be termed as left table, similarly connect the Products table to the second port of the Joiner node and this table will be termed as right table 
- Step 2: Right click on the Joiner node and select “Configure” option to open the configuration dialog of the node
- Step 3: In the “left table” select the “Product ID” column, similarly in the right table select “Product ID” column as you intend to join these tables on Product ID
- Step 4: In the “Include in Output” section, select all the three options “Matching rows”, “Left unmatched rows” and “Right unmatched rows” and also notice the venn diagram, both the circles are yellow.  
- Step 5: Now select the all the columns from the left table into the “Includes” list and similarly select all the columns from the Products table into the “Includes” list except the “Product ID” column as you already have it in the left table   
- Step 6: Press “Ok” and check the output table it will be an extensive table containing all the columns from both the tables and has detailed information on all orders and products

#### Exercise question:
*This is a question presented to learners to check if the steps above were properly completed. It can be a multiple choice question or a question with a 1-3 word answer. It is often not possible to check if all the steps are completed, in this case; the priority is to check that the learner meets the learning objective.*



