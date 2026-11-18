# Relational Database (DB) Design Process

The DB design process described below is **logical**. It focuses
on creating solid schemas, relationships, and structures within
the DB but **does not** say how they should be implemented. This
means, this design process can be done once and implemented in
various relational databases (i.e. PostgreSQL, MySQL, SQL Server, etc.).

Design Process
1. Define mission statement and mission objectives
2. Analyze current database
3. Create the data structures (i.e. fields & field specifications, tables)
4. Determine and establish table relationships
5. Determine and define business rules
6. Determine and define views
7. Review data integrity

Note:

A part of the design process can be determining how to utilize
various indexing strategies. Picking a sound indexing strategy will
vary by the requirements of the systems (i.e. is the DB read-heavy or
write-heavy?). When starting the DB design process, it's recommended
to focus on sound design instead of over-relying on indexing. Indexes should
be peformance optimizations, they do not replace sound DB design.

