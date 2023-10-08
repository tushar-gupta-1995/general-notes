# ACID
- Atomic : If a transaction which might contain multiple sql queries with update and insert is not completed it can be rolled back.
- Consistent: Same attribute cannot have different values
- Isolation: Each transaction runs in isolation and completes such that they are concurrent
- Durability: Data is written to file and should persist in case of system failures etc.
- Not redundant: Copies of data should not exist

## ACID EXAMPLES:

- Atomicity: As we can see in the below image, the transaction begins with few inserts, if any insert fails it rollbacks all the previous inserts.

![Atomicity example](image.png)

![Atomicity example-2](image-3.png)

![Isolation example](image-4.png)

![Durability](image-5.png)

### Isolation:
Transaction isolation levels are used in database management systems (DBMS) to control the level of interaction between concurrent transactions. 

The four standard isolation levels are:
- Read Uncommitted: This is the lowest level of isolation where a transaction can see uncommitted changes made by other transactions.   This can result in dirty reads, non-repeatable reads, and phantom reads.

- Read Committed: In this isolation level, a transaction can only see changes made by other committed transactions. This eliminates dirty reads but can still result in non-repeatable reads and phantom reads.

- Repeatable Read: This isolation level guarantees that a transaction will see the same data throughout its duration, even if other transactions commit changes to the data. However, phantom reads are still possible.

- Serializable: This is the highest isolation level where a transaction is executed as if it were the only transaction in the system. All transactions must be executed sequentially, which ensures that there are no dirty reads, non-repeatable reads, or phantom reads.

#### Concurrency

Refer the below image:

![Alt text](image-8.png)

### Consistency: 
If isolation, durability, atomicity holds true then consistency automatically holds true.
But consistency refers to data as a whole being consistent.
so if debit happens from account a and credited to account b, the sum of account a and b should be same before and after:

Example of consistency is below gate question:
![Alt text](image-6.png)

NOTE: here atomicity and consistency may seeem intertwined, but remember atomicity is either execute fully or not, while consistency is focussed on integrity, even though atomicity is critical for ensuring integrity, they are different properties.

### Transaction
a bunch of instructions bound in a bundle such that they behave as a single instruction.

# IMPORTANT: ALL TRANSACTION FOLLOWS THE ACID PROPERTY ABOVE

Any set of instructions(program) which can include read and write operations, that either execute fully or don't such that any failed instruction rollbacks all instructions executed from the set, is called a transaction
In simple words if a program instructions and guarantees to execute fully not not at all, its called a transaction.

#### Operations in transaction
![Alt text](image-1.png)

In essence transaction are a bunch of instructions combined together or bound together to behave like a single instruction.

![Properties of transaction](image-2.png)

#### Transaction States
- Till the time transaction state is executing its active.
- When the instruction is executed but not committed its called `partially commited.` In other words instructions have executed but commit command has not executed or is executing but has not completed.
- till here if any failure happens all changes are rolled back.
- when the results of instructions are completely commited its called `commited`



![Alt text](image-7.png)

# Schema vs Instance:
- Schema: strucure of data
- Instance: snapshot of data at any given time.


