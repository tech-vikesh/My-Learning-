Task 1: What is Docker?
Question 1> What is a Container and Why Do We Need It?
Answer> A container is a lightweight package that contains an application along with all its dependencies, libraries, and configuration files.

* We need containers because:
:They ensure applications run the same way on every system.
:They eliminate the "It works on my machine" problem.
:They are lightweight and start quickly.
:They make application deployment easier.
:They improve resource utilization compared to virtual machines.

#Containers vs Virtual Machines
= Container > Shares the host OS kernel, Lightweight, Starts in seconds, Uses fewer resources, Suitable for microservices and DevOps
= Virtual Machines > Has its own guest OS, Heavyweight, Takes minutes to start, Uses more resources, Suitable for running multiple operating systems

Real Difference
A Virtual Machine virtualizes the hardware and runs a complete operating system.
A Container virtualizes the operating system and shares the host OS kernel, making it faster and more efficient

Docker Architecture
Docker consists of the following components:
1. Docker Client
The Docker Client is the command-line tool used by users.
Example: docker run nginx
