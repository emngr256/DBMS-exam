Online Food Delivery

This project demonstrates a Polyglot Persistence approach for a food delivery service, integrating a relational database (PostgreSQL) with a document-oriented database (MongoDB). The system ensures real-time synchronization between both databases using a Java-based application.



🚀 Key Features

Dual-Database Sync: Synchronized CRUD operations across SQL and NoSQL.



Data Integrity: Implemented foreign keys with ON DELETE CASCADE and UNIQUE constraints in PostgreSQL.



Performance Optimization: B-Tree indexing on frequently searched columns (e.g., Restaurant Names).



Normalized \& Embedded Models: Demonstrates 3rd Normal Form in SQL and Embedded Document patterns in NoSQL.



📂 Project Structure

src/: Java source code (Connection logic, Models, and CRUD operations).



source.sql: Full PostgreSQL database dump (including 10 tables, data, and indexes).



pom.xml: Maven configuration with dependencies for PostgreSQL and MongoDB drivers.



🛠️ Tech Stack

Languages: Java



RDBMS: PostgreSQL (Source of Truth)



NoSQL: MongoDB (User Profiles)



Drivers: JDBC, MongoDB Java Sync Driver



📊 Performance Benchmarks (Indexing)

Using EXPLAIN ANALYZE on the Restaurants table:



Without Index: 0.609 ms (Sequential Scan)



With B-Tree Index: 0.044 ms (Index Scan)



Improvement: \~13.8x faster retrieval.



⚙️ How to Run

Execute source.sql in your pgAdmin Query Tool to set up the PostgreSQL schema.



Ensure a local MongoDB instance (or Atlas) is running.



Update connection strings in the Java source code.



Run the application via IntelliJ IDEA or any Java IDE.

