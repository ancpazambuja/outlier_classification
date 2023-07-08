# outlier_classification
Unsupervised classification of execution time outliers of running jobs in a HPC environment.

## Context
High-performance computing (HPC) environments are complex. Both hardware infrastructure and software development have specific needs.

The hardware infrastructure is designed for high performance and availability. But the complexity of it makes it impossible to keep things on track all the time. Therefore, redundancy, monitoring and automation are critical.

Even so, distributed applications running in HPC environments must be very fault tolerant and resilient.

Despite all efforts, it is not uncommon to find jobs that run slower than usual. This slowdown is often due to problems in the hardware infrastructure.

## Objective
The main objective of this project is:
 - given the **execution time** of an unit of work, its **characteristics** and **history** of execution times of all kind of tasks, answer if this unit of work ran slower than usual.

## Important Restrictions
 - The history consists of application's log files which:
     - are **unstructured** and **unlabeled** data;
     - have **more than terabytes** of data.
 - Should be a complete **unsupervised** solution.

## User Story

### **Title**:
Execution Time Outlier Classification

### **Persona**:
Job Monitor, person or team responsible for ensuring the perfect use of computer clusters.

### **Description**:
As a **Job Monitor**, I want to **be alerted if a unit of work in a job finishes slower than expected**, so **I can check why it's slow and fix it**.

### Machine Learning Functionality**:
The ML module works in 2 steps:
 - training: should be completely unsupervised. The algorithm should learn from data how to identify anomalous execution times.
 - inference: given a work unit which has just finished its execution, classify it as outlier or not.

### **Acceptance Criteria**:
Given **a tuple of attributes representing a work unit**, when **the execution time is slower than usual**, then **classify it as an outlier**.
In the other way, given **a tuple of attributes representing a work unit**, when **the execution time is as usual**, then **do nothing**.

### **Machine Learning Criteria**:

**The machine learning model must be more accurate than the automation module in use today** - based in statistical analysis.

## Methodology

This work is composed by a series of 3 python notebooks:
 - *exploratory_analysis.ipynb;*
 - *pre_processing.ipynb; and*
 - *outlier_classification.ipynb.*

See the files for a self-explanatory reading of them.



## Code Organization
 There are 2 directories:
  - notebook: which contains the 3 notebooks;
  - data: which contains a very small structured data.
