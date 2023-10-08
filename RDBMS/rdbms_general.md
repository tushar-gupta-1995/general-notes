# ACID
- Atomic : If a transaction which might contain multiple sql queries with update and insert is not completed it can be rolled back.
- Consistent: Same attribute cannot have different values
- Isolation: Each transaction runs in isolation and completes such that they are concurrent
- Durability: Data is written to file and should persist in case of system failures etc.
- Not redundant: Copies of data should not exist

## ACID EXAMPLES:

- Atomicity: As we can see in the below image, the transaction begins with few inserts, if any insert fails it rollbacks all the previous inserts.

![Atomicity example](image.png)
### Transaction
a bunch of instructions bound in a bundle such that they behave as a single instruction.

# IMPORTANT: ALL TRANSACTION FOLLOWS THE ACID PROPERTY ABOVE

Any set of instructions(program) which can include read and write operations, that either execute fully or don't such that any failed instruction rollbacks all instructions executed from the set, is called a transaction
In simple words if a program instructions and guarantees to execute fully not not at all, its called a transaction.

#### Operations in transaction
![Alt text](image-1.png)

In essence transaction are a bunch of instructions combined together or bound together to behave like a single instruction.

![Properties of transaction](image-2.png)

# Schema vs Instance:
- Schema: strucure of data
- Instance: snapshot of data at any given time.


