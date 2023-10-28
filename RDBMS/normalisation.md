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

