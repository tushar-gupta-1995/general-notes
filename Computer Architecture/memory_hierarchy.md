CPU -> Register -> Cache => MM (Ram) -> SM(Hard disk)

Each memory is divided into equal sizes, each division is called:
- page in SM
- block/frame/word in MM
- Cache line sometimes called cache block in cache

Each division size should be same across all types of memory.
Therefore number of divisions is less in MM compared to SM, and less in cache compared to MM.

Usually the size of each block is 1 byte and this is called byte addressable memory.



Table for unit of memory
![Table for unit of memory](image.png)

10^3 = 2^10 = kilo
for every 3 power inrease in base 10 or 10 power in base 2
- mega
- giga
- tera
- peta




Size of memory: number of locations(2^size of size of each location) * size of each location(default 1 byte or default assume byte addressible)


# Direct Mapping
Focus on MM and cache.
Divide each block of MM into n words where word is the size of memory location(in byte addressable word size is 1 byte)
Divide each cach line into n words as well
as should be obvious, size of each cache line is size of  each block of MM

since number of cache lines << number of blocks

let size of cache line is n, then take first n blocks and map to each of the n cachelines.
post that, map block number to (block number%n) cache line.

Overall formula also becomes:
CL assigned to block m = (m%n) where n is the number of cache lines

Since each CL holds but one block at a time BUT each block can ever be present in a specific cache line, the obvious CON of this approach is even if a cache line is free, the block will not use it until its mapped to that.

The list of blocks mapped to a CL can be annotated with tags.


Refer the diagrams

![memory distribution amongst cache and MM](image-1.png)
![Alt text](image-2.png)



Lets look at division of data in MM in other way

- MM is divided in blocks
- each block is divided into words

Suppose each block has n words and word has m bits
- Take last log base 2(n) of index of word in binary and it tells the block offset
- remaining(n-log base 2(n)) bits tell the position of block in MM

Now suppose in direct mapping each CL has k bits mapped
- the last log base 2(k) of (n-log base 2(n)) tell the CL of the block
- the remaining (n-log base 2(n)) - log base 2(k) tell the tag of the block

Refer the below image:
![Alt text](image-3.png)

Question:
![Alt text](image-4.png)

# Remember: 
![Alt text](image-6.png)

![Alt text](image-10.png)