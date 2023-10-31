# DWM_Practical
Don't copy  , just take inspiration


Aggregate Fact Tables:
Aggregate fact tables are a special kind of fact tables in a data warehouse which contains new metrics which are been derived from one or more aggregate functions (COUNT, AVERAGE, MIN, MAX, etc.) or from some specialized functions whose outputs are totally derived from a grouping of base data.
Aggregates are basically summarization of the fact related data which are been used as a purpose to improve the performance.
These new metrics, called as “aggregate facts” or “summary statistics” are been stored and maintained in database of the data warehouse in special fact table at the grain of the aggregation.
In similar way, the corresponding dimensions are been rolled up and compressed to match the new grain of the fact.
These specialized tables are been used as an substitutions whenever possible for returning user queries. The reason is the speed. 
Querying a neat aggregate table is much faster and uses less of the disk I/O than the base, atomic fact table, especially when the dimensions are large as well.
If you want to amaze your users then start adding the aggregates. 
Even you can use this technique in your operational systems as well, giving boost to the foundational reports.






OLAP Operations in DBMS

OLAP stands for Online Analytical Processing Server. It is a software technology that allows users to analyze information from multiple database systems at the same time. It is based on multidimensional data model and allows the user to query on multi-dimensional data (eg. Delhi -> 2018 -> Sales data). OLAP databases are divided into one or more cubes and these cubes are known as Hyper-cubes.

OLAP operations:
There are five basic analytical operations that can be performed on an OLAP cube:

Drill down: In drill-down operation, the less detailed data is converted into highly detailed data. It can be done by:
Moving down in the concept hierarchy
Adding a new dimension
In the cube given in overview section, the drill down operation is performed by moving down in the concept hierarchy of Time dimension (Quarter -> Month).

Roll up: It is just opposite of the drill-down operation. It performs aggregation on the OLAP cube. It can be done by:
Climbing up in the concept hierarchy
Reducing the dimensions
In the cube given in the overview section, the roll-up operation is performed by climbing up in the concept hierarchy of Location dimension (City -> Country).

Dice: It selects a sub-cube from the OLAP cube by selecting two or more dimensions. In the cube given in the overview section, a sub-cube is selected by selecting following dimensions with criteria:
Location = “Delhi” or “Kolkata”
Time = “Q1” or “Q2”
Item = “Car” or “Bus”
Slice: It selects a single dimension from the OLAP cube which results in a new sub-cube creation. In the cube given in the overview section, Slice is performed on the dimension Time = “Q1”.
Pivot: It is also known as rotation operation as it rotates the current view to get a new view of the representation. In the sub-cube obtained after the slice operation, performing pivot operation gives a new view of it.




https://www.geeksforgeeks.org/difference-between-fact-table-and-dimension-table/amp/
https://www.geeksforgeeks.org/olap-operations-in-dbms/amp/
