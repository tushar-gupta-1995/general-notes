# pipelining

![Alt text](image-81.png)


![Alt text](image-82.png)

# instruction fetch:  get the instruction from memory

# instruction decode
## instruction opcode: the operation required by instruction
## instruction operand: the operands on which the operation (determined by opcode) needs to be performed

# instruction execute: perform the operation decoded above

# instruction store: store the details of operation in memory


![Alt text](image-83.png)

![Alt text](image-84.png)

![Alt text](image-85.png)

![Alt text](image-86.png)

Usually in a normal cpu, details of current instruction are stored in CPU register and then cpu in its clock does one of the following:
(**NOTE:** each of the below takes 1 clock cycle)
- fetch
- decode
- execute
- store

in pipeline 
- there is seperate circuit for each of 4 phases in same processor, thus when decode is happening fetch can happen in parallel.


# Sample pipelining question:


![Alt text](image-89.png)

## solution

![Alt text](image-90.png)

### formulae for pipelining

![Alt text](image-91.png)

![Alt text](image-92.png)

![Alt text](image-93.png)

### CPI (clock per instruction) in pipelining
 - first instruction takes m clock cycles where m is number of stage per instruction (usually 4 as above)
 - from second onwards take 1 clock cycle
 - in long run CPI for pipelining should be 1 (with exception of first instruction)


# Understanding clock

If a cpu is 1 Ghz, then it completes 10^9 clock cycle in a second, so to complete 1 clock cycle, it will take, 10 ^-9 seconds = 1 ns.
if n processes take different times, to complete all process in same clock cycle, we just need to ensure that slowest process completes in 1 cs, and that will determine the min cpu frequency needed to complete a task.

- so might have to slow time taken to complete 1 clock cycle and thus cpu frequency if required to complete all processes in 1 clock cycle based on slowest process

**example:** 
![Alt text](image-99.png)

**Gate Question to show the slowest stage determines speed:**
![Alt text](image-102.png)

**Also understand pipelined processor uses buffers, so that the staged circuit can directly pick up from output of previous stage, hence the time taken for a single instruction on pipelined processor is greater or equal to non pipelined BUT over time pipelined processor can have much better speed then non pipelined processor, the speed up having a theoretical limit of number of stages for which seperate circuit exist**

# Hazards:

![Alt text](image-113.png)


**if particular stages share memory, they cannot execute in parallel**
![Alt text](image-114.png)

![Alt text](image-115.png)

## Control Hazards

![Alt text](image-116.png)


![Alt text](image-117.png)

**Example of control hazard:** since in a pipelined processor instruction are executing parallely, suppose instruction 3 is executing, and its a if condition, instruction 4 and 5 are in fetch and decode stage parallely, once instruction 3 executed, next instructions are instruction 7 and 8 and Instruction 4 and 5 are never supposed to be executed, thus decoding and fetching 4 and 5 was a waste.
Refer above image as well.

so if an instruction's execution decides which instruction to run next and thus there is non determinism in deciding next instruction to decode, fetch impacting parallelism, then its called **control hazard**

![Alt text](image-118.png)

example in above: 80% take 1 Clock cycle
20% take 3 stalls + 1 clock cycle=4
0.8+0.2(0.4) = 1.6


![Alt text](image-119.png)


# Prediction of next statements

- usually in loops statement execute multiple times
- therefore if we identify a loop, we can load the instructions for loop in pipeline
- it is probable that they will be the next statements to execute
- if the loop terminates, we will incur a stall, but its an acceptable stall if loop executes multiple times

![Alt text](image-124.png)

![Alt text](image-126.png)

# Data hazards

![Alt text](image-127.png)

![Alt text](image-128.png)