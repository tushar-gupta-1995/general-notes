![Alt text](image-91.png)

![Alt text](image-92.png)

![Alt text](image-93.png)

![Alt text](image-94.png)

# Insertion Anamoly :

![Alt text](image-95.png)

- in the above table branch_code, branch_name and brach_age are seperate pieces of info
- assume in above table roll no of student is primary key
- if a new branch is opened, currently with no student, it cannot be inserted into this table
- thus in this table branch gets dependent on student even though in real life its not
- further if we want to remove a student, then branch details also need to be removed, but branch is technically not dependent on student, however due to table design this dependence exists in db. **This is deletion anamoly**
-further if we want to update a hod name for one branch, i will have to do it for each row where that hod exists, if one row is missed, it leads to loss of integrity **This is deletion anamoly**

**Solution:**

![Alt text](image-96.png)


![Alt text](image-97.png)

# functional dependency
if a->b, where b can derived from a, then b is functionally dependent on a.

To prove a=>b
if two or more values in a are same and output different b.
in that case b is indipendent of a.

![Alt text](image-104.png)

![Alt text](image-103.png)
# Trivial Functional Dependency:
if b is subset of a such that a=(p,q,r)
and b = (q)
then a->b will always hold..since its **obvious**

**Example** in option C, RHS is subset of LHS hence trivial.
![Alt text](image-100.png)

# Functional Dependency Closure

![Alt text](image-108.png)

## Mininmal cover

![Alt text](image-114.png)

# Armstrong axioms

![Alt text](image-112.png)

![Alt text](image-123.png)

# types of keys

![Alt text](image-117.png)

# KEY: Any key is a set of attributes(remember attributes=columns)
# Super Key: Set of attributes whose closure covers all attributes (remember attributes=columns)

![Alt text](image-118.png) 

![Alt text](image-121.png)

# candidate key: minimal set of attributes required to represent a row..that is a candidate key cannot be further broken

# primary key

![Alt text](image-122.png)

# Foreign key can ALSO be in the same table as primary key, that is it can refer to the primary key in same table, Example:
- CR is a person amongst the roll numbers
- if i dlete roll number 1 and roll number 1 is the CR, it does not make sense, hence both PK and FK in same table
- Remember FK exists because of the primary key reference...if primary key reference CAN only be removed if FK constraints are removed.

![Alt text](image-125.png)

# Remember one table can have more then 1 foreign key example, in a m:n relation we form a 3rd table with PK of both entities..so it has 2 foreign keys

![Alt text](image-126.png)

# foreign key reference a primary key..foreign key is a subset of primary key they reference//

**Given fk -> pk**
- pk is superset of fk
- pk can be added without constraint
- fk can be removed without constraint
- pk cannot be removed without deleting all fk referencs first
- fk cannot be added without adding a pk which it refers to

![Alt text](image-133.png)


# secondary key 

![Alt text](image-139.png)

# Normalisation

![Alt text](image-148.png)

## First normal form

![Alt text](image-149.png)

![Alt text](image-154.png)

## Second normal form

![Alt text](image-155.png)

### Transitive dependency

if a non prime attribute is functionally dependent on another non prime attribute

![Alt text](image-157.png)

## Third normal form

![Alt text](image-158.png)

![Alt text](image-159.png)

![Alt text](image-162.png)

In summary

- **2nf**: partial dependency, part of prime attribute identifies non prime..when prime is composite
- **3nf**: transitive dependency, non prime attribute identifies another non prime attribute

