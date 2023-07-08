# outlier_classification
Unsupervised classification of execution time outliers of running jobs in a HPC environment.

## Context
High-performance computing (HPC) environments are complex. Both hardware infrastructure and software development have specific needs.

The hardware infrastructure is designed for high performance and availability. But the complexity of it makes it impossible to keep things on track all the time. Therefore, redundancy, monitoring and automation are critical.

Even so, distributed applications running in HPC environments must be very fault tolerant and resilient.

Despite all efforts, it is not uncommon to find jobs that run slower than usual. This slowdown is often due to problems in the hardware infrastructure.

## Objective
The main objective of this project is:
 - given the **execution time** of an unit of work, its **characteristics** and an **history** of execution times, answer if this unit of work run slower than usual.

## Software Requirements
 - The history consists of application's log files which:
     - are **unstructured** and **unlabeled** data;
     - have **more than terabytes** of data.
 - Should be a complete **unsupervised** solution.



