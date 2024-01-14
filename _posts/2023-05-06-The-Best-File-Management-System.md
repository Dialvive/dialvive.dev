---
title: "What is the Best File Management System?"
tags: [Opinion]
style: border
color: primary
comments: false
description: "Whether you are thinking on a new application you want to develop, or upgrading a legacy system to modern code with best practices, this is a post that will certainly be of help to answer this important design question"
---

## Introduction

I've always said that less is more. And in today's rant, I'd like to elaborate on why having an application serving (or even working with) files using a File Manager System, is such a bad idea.

I do believe that we are living in the future, and we have an enormous array of applications (dependencies, frameworks, you name it) at our disposal that help us not re-invent the wheel each time we want to develop a new feature, or even modernizing legacy systems. I mean, why bother reinventing the wheel when we have access to Michelin or Pirelli wheels already at our disposal? Even if we don't want to pay for top-notch wheels with guarranty and support, in the Software Engineering world we always have Open-Source options.

There are frameworks that help us to use a File Management System in a secure way. But it is up to every developer (and architect) to have special focus on security when working with those. A simple wrong assumption or bad development practice can led your application to expose the File System you are using, along with your probably confidential and sensitive data, and your dignity and reputation as well.

Serving files through applications is really useful in some cases, they may allow an application to import or export data in a friendly and structured way without using an API for less tech savvy final users (specially in a B2C setting). And just passing files from one place to another may seem like the fastest and easiest solution for this purpose, but at what cost? It will not take much time for you to realize that the security hardening of such system will take a lot of effort, time, and money.

### Concerns with File-based Application Storage

- **Lack of Data Integrity and Consistency**: File systems do not provide built-in mechanisms for ensuring data consistency, enforcing referential integrity, or handling concurrency. Ensuring data integrity and consistency becomes the responsibility of the application or developers. Don't you want some ACID (Atomicity, Consistency, Integrity, Durability)?

- **Limited Search and Query Capabilities**: File systems lack advanced querying and search functionalities compared to databases. Performing complex searches, filtering, or sorting operations on files becomes challenging without implementing challenging and complex custom solutions (That will probably abuse sketchy batch or bash scripts).

- **Access Control and Security Challenges**: File systems often have limited access control capabilities compared to databases. It can be challenging to enforce fine-grained permissions or track user actions on files. Additionally, securing files against unauthorized access or tampering requires additional measures beyond file system-level controls.

- **Vulnerabilities and Security Risks**: Common Weakness Enumerations (CWE) such as 22 to 59, 61 to 67, 69, 72, 73, 98, 219, 378, 379, 426, 427, 428, 434, 552, 538, 541, and 775, highlight the potential dangers associated with file-based storage. By avoiding files altogether, we can mitigate these risks and enhance the overall security posture of our application by design.

- **Added Maintenance Overhead**: Most file management systems, especially Windows or Linux operating systems, require an additional layer of maintenance. This includes regular updates, patches, security configurations, and monitoring to ensure the stability and security of the operating system. And really, if we are building a new application, are we really setting up a full featured Linux or Windows server for our application these days? Probably serving a minimal Docker image will suffice.

### Advantages of Using a Document-based Database

A document-based database, such as MongoDB or CouchDB, offers an alternative approach to file management. Storing data as documents provides several advantages. It allows for flexible schema design, efficient querying and indexing, seamless scalability, and built-in replication for high availability:

- **Structured Data Management**: Databases provide a structured approach to data storage, allowing for efficient querying, indexing, and searching. This is especially beneficial when dealing with large amounts of data or complex data relationships.

- **Improved Data Consistency**: Databases enforce data consistency by supporting transactional operations. This ensures that data remains accurate and reliable, even in concurrent access scenarios or during system failures.

- **Access Control and Security**: Databases offer built-in access control mechanisms, allowing administrators to define user roles and permissions. This ensures that only authorized individuals can access, modify, or delete data. Additionally, databases provide security features like encryption and auditing to protect sensitive information.

- **Scalability and Performance**: Databases, including MongoDB, are designed to handle scalability and performance requirements. They can efficiently manage large datasets, distribute data across multiple nodes, and handle high volumes of read and write operations.

- **Flexibility in Data Modeling**: MongoDB, being a NoSQL database, offers flexibility in data modeling. It allows for dynamic schema design, accommodating evolving data structures and facilitating agile development. This can be advantageous when dealing with unstructured or semi-structured data.

- **Implementing Data Versioning Systems**: Versioning files stored in a document-based database is often easier and more manageable than in a file system. With the right database configuration and structure, it becomes straightforward to track and manage different versions of data. This simplifies collaboration, auditing, and rollback scenarios, ensuring data integrity and reducing complexity.

- **Migrating Data**: One of the significant advantages of moving away from file-based storage is the ease of data migration. Whether it's for disaster recovery purposes, system upgrades, or troubleshooting, migrating data stored in a document-based database is typically simpler than dealing with file systems. The structured nature of the database allows for seamless transfer, transformation, and consolidation of data across different environments.

## Conclusion

Relying on an application to serve or manage files through a file management system poses significant security risks and drawbacks. While there may be some cases where serving files through an application seems convenient, the disadvantages outweigh the benefits.

By avoiding the use of file management systems and embracing document-based databases, we can mitigate security risks, enhance data integrity, and streamline data management processes. It's a step towards a more secure and efficient application architecture.

Sometimes the best file management system is simply not having files altogether.
