# Interface

![Alt text](image-53.png)

![Alt text](image-54.png)

![Alt text](image-55.png)

![Alt text](image-56.png)

# Memory mapped I/O

Same bus for cpu and I/o devices.

Below image 8085, example of memory mapped I/o:

![Alt text](image-57.png)


# I/O processor

A seperate processor for I/O devices, responsibility taken from cPU, example below:

![Alt text](image-58.png)

# Data transfer mode:

![Alt text](image-59.png)

# Synchronous vs Ascynchronous transfer

- Synchronous transfer data sender and receiver both are on the same clock example Main memory

- Asynchronous transfer data sender and receiver both are on  different clock example I/O devices.

Async: send a strobe to notify data request and ack to acknowledge data recieved, handshake.

![Alt text](image-60.png)


