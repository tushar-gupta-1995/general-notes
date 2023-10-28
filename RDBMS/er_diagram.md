# Important Note WHEN creating set for cardinality
**the one with many in er diagram line, pick many from set, th one with a "1", pick one from set**



![Alt text](image-60.png)

![Alt text](image-61.png)

![Alt text](image-62.png)


# tuple
row of the table

# domain/attribute
column in the table

# Database Schema
A database schema is a structure that represents the logical storage of the data in a database. It represents the organization of data and provides information about the relationships between the tables in a given database. In this topic, we will understand more about database schema and its types. Before understanding database schema, lets first understand what a Database is.

## example:

![Alt text](image-63.png)

# types of attributes

![Alt text](image-64.png)

## Multivalued: double ellipse: to tackle this create seperate table
## simple vs composite (composite broken into further parts, example name broken into first and last name), to tackle this create seperate column

![Alt text](image-65.png)

![Alt text](image-66.png)

![Alt text](image-67.png)

# Relationships: represented by diamond

![Alt text](image-68.png)


## Name:  Unique name of the relationship

## Degree: number of entities participating in relation, eg, unary binary, ternary, n-ary

![Alt text](image-69.png)



## Structural constraints(cardinality, participation)

### Cardinalty

#### 1:1 relation
Either we do not participate, or participate exactly once.
1:1 shown by arrow pointing towards entity from relationship symbol.
or by writing 1 on the line from relation symbol to entity.

![Alt text](image-70.png)


#### 1:n relation

![Alt text](image-71.png)

![Alt text](image-75.png)


#### m:n relation

![Alt text](image-72.png)


![Alt text](image-73.png)


# Strong and weak entity set

![Alt text](image-78.png)

- weak entity set remains in total participation with the strong entity set
- weak entity represented by double rectangle
- weak relation represented by double diamond
- total participation represented by double line
- weak entity might be in relation with multiple strong entity set..however it has foreign key relation with only one, called its owneer entity set

![Alt text](image-79.png)


![Alt text](image-80.png)

# Number of tables for different cardinality of binary

- for a 1:1 relation, **no 3rd table to represent relation required**, just add a new column on the weak enrity key table for primary column of strong entiry, this becomes foreign key..(note since 1:1 the foreign key will not repeat more then once..it might not exist..but if it does it will be at max once.)
- for a 1:n relation, **no 3rd table to represent relation required**.

![Alt text](image-98.png)

- Similarly for n:1: 

![Alt text](image-99.png)

- So its reverse for 1:n types, the side in ER showing 1, participates n times and side showingn participate 1 time
- for a m:n relation, create a seperate table with primary key of both entity a and entity nb

![Alt text](image-81.png)

![Alt text](image-82.png)
- for ternary and >=2 ary just create seperate tables

![Alt text](image-83.png)

![Alt text](image-85.png)