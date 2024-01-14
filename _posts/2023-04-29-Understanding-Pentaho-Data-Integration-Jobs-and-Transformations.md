---
title: "Understanding Pentaho Data Integration: Jobs and Transformations"
tags: [Pentaho]
style: border
color: pentaho
comments: false
description: Discover the Key Differences Between Jobs and Transformations in Pentaho Data Integration
---

## Contents <a name="Contents"></a>

- [Contents ](#contents-)
- [Introduction](#introduction)
- [Differences between Jobs and Transformations](#differences-between-jobs-and-transformations)
- [Shared Elements](#shared-elements)
- [Conclusion](#conclusion)
- [References](#references)

## Introduction

Pentaho Data Integration (PDI) is a powerful open-source ETL tool that users can use to extract, transform, and load data from various sources into a target system. In PDI, a typical ETL workflow consists of Jobs and Transformations.

A Transformation represents the data transformation part of an ETL workflow, and performs data manipulation tasks. Like extracting data from various sources, performing calculations, filtering, sorting, joining, and writing data to different destinations. It is designed to be reusable and can be called from a job or another transformation.

On the other hand, a Job represents the orchestration part of an ETL workflow and handles the sequence of tasks to be executed. It can call one or more Transformations or Jobs, execute shell scripts or database operations, check for conditions, define dependencies between tasks, and handle error and recovery scenarios.

In simpler terms, a transformation performs data manipulation tasks, while a job orchestrates the sequence of tasks to be executed in an ETL process.

## Differences between Jobs and Transformations

A key difference between a job and a transformation is that a transformation operates on a single set of data at a time, while a job can execute many transformations, each with its set of data. A job can also perform tasks that are outside the scope of a transformation, such as sending notifications, file management, or writing logs.

Both Jobs and Transformations contain various components to create robust ETL workflows:

- **Job Entries** represent the different tasks or processes that need to be executed as part of the job. Job entries can include Transformations, shell scripts, database operations, file operations, and more. Each job entry performs a specific task and can be configured with various options and parameters.

- **Transformation Steps** represent the actions performed on the data during the ETL process. Each step performs a specific operation on the data (whether it is to read, transform, or write) and can be configured with various options and parameters to achieve the desired results.

## Shared Elements

Both Jobs and Transformations are also composed of:

- **Hops**: These are the lines that connect Job Entries or Transformation Steps and define the flow of execution between them. They can be used to connect different components in a linear or non-linear fashion, allowing for complex workflows.
- **Parameters**: These are variables that users can pass into a Job or Transformation at runtime, allowing for greater flexibility and reusability. They can configure different aspects, such as database connections or file paths, without the need to define them each time.
- **Variables**: These are user-defined variables that can store and manipulate data within the Job or Transformation. Variables can be used to store temporary data, configure options, or perform calculations.
- **Data**:  These are not present in KJB or KTR files, since they are generated or obtained through input Steps at runtime.  They are passed between Entries or Steps through Hops as table rows (Like a relational DB).

Both Parameters and Variables can be recalled in Entries and Steps following this format: `${PARAM_NAME}` or `%%PARAM_NAME%%`.

## Conclusion

Understanding the differences between Jobs and Transformations in Pentaho Data Integration is crucial for building effective and efficient ETL workflows. While both Jobs and Transformations are vital components of a successful ETL process, they have different purposes and are used in different ways. Jobs are used to orchestrate the execution of tasks and can perform tasks outside the scope of Transformations, while Transformations perform data manipulation tasks. By utilizing both Jobs and Transformations effectively, users can extract, transform, and load data from various sources into a target system seamlessly.

## References

- Hitachi Vantara (Mar/2018). *Basic Concepts of PDI: Transformations, Jobs and Hops*. <https://help.hitachivantara.com/Documentation/Pentaho/8.0/Products/Data_Integration/Data_Integration_Perspective/010>
- Hitachi Vantara (Dec/2017). *Parameters*. <https://help.hitachivantara.com/Documentation/Pentaho/8.0/Products/Data_Integration/Data_Integration_Perspective/050/010>
- Hitachi Vantara (Dec/2017). *Variables*. <https://help.hitachivantara.com/Documentation/Pentaho/8.0/Products/Data_Integration/Data_Integration_Perspective/050/020>
