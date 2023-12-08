# Assignment-2

### Overall objective

This assignment is intended to assess your knowledge of NoSQL database programming.

### Instructions (read carefully)

* The assignment comprises **two questions**, each worth 50% of the mark.
* You **must** write **one Python code (notebook) for each question**. Please, **DO NOT** submit one single file as your solutions will be assessed by different markers.
* Make sure **your code files show the results for each cell**, especially those commands retrieving data from the database. You can export a PDF or HTML of your notebook and upload it along with your Python notebook.
* Remember that this is a **2-step submission process**: once you have all your files on GitHub, copy the link to your GitHub repository and submit it through Moodle ([Coursework submissions](https://moodle.lse.ac.uk/mod/assign/view.php?id=1132257) section). Avoid, as much as possible, any identifiable information (other than your candidate number) on your submitted work.

### Question 1: MongoDB

In this question, you will use the **Northwind** example database as a **collection of documents** to answer some questions.

1. Set up a MongoDB Atlas cluster.
2. Create a Python notebook with `PyMongo` installed, and connect it to your Atlas cluster.
3. Download the Northwind database (CSV files) from the [data](./data) folder. There are 6 files mapping categories, customers, employees, orders, products, and suppliers.
4. Have a look at the **Northwind Entity-Relationship model** ([fig](./fig) folder) to get a sense of existing entities, primary/foreign keys, and relationships. Notice that `Orders` and `Order_Details` were merged into one single file (`orders.csv`).
5. Answer the questions below (write Python code for that). See example [SQL (relational) code](./code) for questions 1B-1D. 

1A) Create a new database (`db`) called `Northwind` and load each CSV file into a new collection (for instance, `customers.csv` into `db["customers"]`. **Important:** when loading the CSV data into a collection, check for relationships (foreign keys) between two entities (for instance, `products` and `suppliers`). **You should create all relationships manually**, by figuring out how to make one document (from one collection) refer to a document in another collection. **Tip:** use the object IDs.

1B) List all product names and unit prices supplied by each company (supplier). Also, list the supplier's name.

1C) List the category of the 10 top-seller products.

1D) For all customers, list all the products they bought.

### Question 2: Neo4j

In this question, you will **transpose an E-R model into a graph database**.

1. Set up a Neo4j AuraDB cluster.
2. Create a Python notebook with a Neo4 driver installed, and connect it to your AuraDB cluster.
3. Refer to **the E-R model you developed for assignment 1 (Baseball or Private Airport)** and identify all entities, attributes, and relationships. Then, **design a Property Graph model** mapping these elements into nodes (and labels), properties, and relationships. **Important:** remember that Neo4j requires the property graph to be created all at once (all nodes and relationships), so you can benefit from variables when specifying your Cypher queries. A **practical tip** is i) look to your E-R model and check which pairs/sets of entities must be created together (i.e., they have direct relationships); ii) write Cypher statements to create part of your graph and check for consistency (all nodes and labels, properties, and relationships); iii) progressively expand your graph by adding new nodes and relationships. An **alternative approach** is to create sub-graphs (parts of your E-R) and then `MATCH/MERGE` sub-graphs into a single graph.
4. Answer the questions below (write Python code for that):

2A) Create your graph database, based on your Property Graph model translated from your E-R model. Feel free to adapt your E-R model as needed. [This ebook](https://neo4j.com/whitepapers/definitive-guide-graph-databases-rdbms-developer/) is a good reference. Populate your graph with the data you used in Assignment 1. This can be i) hardcoded (manually creating all nodes, properties, and relationships) OR ii) loaded from CSV files used in/exported from your first assignment. Show the final graph: i) on your Python code, using *yFiles* (see Seminar 9), or ii) a screenshot taken from your AuraDB instance and uploaded along with your code. 

If **BASEBALL**:

2B) List (or show the graph of) all teams, and their corresponding managers, coaches, and players.

2C) List all games, ordered by descending number of hits. If you decide to show the graph (instead of a list), check whether yFiles allows you to visualise nodes in descending order (hierarchical visualisation) of a particular property (`hit`, in this case). Do not worry in case this visualisation is not possible.

2D) List the player (name and corresponding BA) with the most hits - this can be a sum of all single, double, triple and home run hits. In case the player is also a pitcher, list his corresponding ERA.

If **AIRPORT**:

2B) List (or show the graph of) all aeroplanes and their owners, and whether each owner is a person or a corporation.

2C) List all maintenance services, ordered by ascending maintenance time (number of hours). If you decide to show the graph (instead of a list), check whether yFiles allows you to visualise nodes in descending order (hierarchical visualisation) of a particular property (maintenance time, in this case). Do not worry in case this visualisation is not possible.

2D) List (or show the graph of) the employees and all the planes they can do maintenance work.

### Important dates

* Assignment released: 24/11/2023, 5:00 pm.
* Solution deadline: 11/12/2023, 5:00 pm (**both GitHub and Moodle**)
* Feedback and provisional marks (tentative): 05/01/2024, 5:00 pm.
* See Moodle for late submission penalties.

### Note on Generative AI tools

* Refer to [Moodle](https://moodle.lse.ac.uk/course/view.php?id=7681) for the Generative AI guidance document and course-specific policy. Make sure to comply with all items in the document.

### Marking criteria

* This assignment is worth 20% of the final grade.
* **IMPORTANT**: according to the School policy, you **must** submit an answer to this assignment; otherwise, you will be graded 0 (zero).
* Refer to [Moodle](https://moodle.lse.ac.uk/course/view.php?id=7681) for the General Assessment Criteria for Undergraduate Degrees document.

| Problem breakdown  | Max marks |
| ------------- | ------------- |
| 1A - Correct database creation (entities, attributes, PK/FK mapped into collections) and data loading | 20 |
| 1B - Correct query and display of results, code documentation/organisation | 10 |
| 1C - Correct query and display of results, code documentation/organisation | 10 |
| 1D - Correct query and display of results, code documentation/organisation | 10 |
| 2A - Correct database creation (entities, attributes, PK/FK mapped into graph), Property Graph model displayed, correct data loading | 20 |
| 2B - Correct query and display of results, code documentation/organisation | 10 |
| 2C - Correct query and display of results, code documentation/organisation | 10 |
| 2D - Correct query and display of results, code documentation/organisation | 10 |
| TOTAL | 100 |

### Feedback and provisional marks

* To be provided after your submission.
