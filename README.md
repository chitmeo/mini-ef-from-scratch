# Project Goal

This project is not about building another ORM.

The goal is to understand how Entity Framework Core works internally by implementing a minimal version step by step.

By the end of this project, you should understand:

1. Expression Trees
2. LINQ Providers
3. IQueryable
4. IQueryProvider
5. Expression Visitors
6. SQL Translation
7. Query Pipelines
8. Dynamic LINQ
9. ORM Architecture

# Learning Objectives

After completing this repository, you will be able to:

1. Read any Expression Tree
2. Build Expression Trees programmatically
3. Write custom Expression Visitors
4. Understand how LINQ works internally
5. Understand why IQueryable exists
6. Build a custom LINQ Provider
7. Translate LINQ into SQL
8. Understand Entity Framework Core architecture
9. Read EF Core source code with confidence

# Repository Structure
```
mini-ef-from-scratch
│
├── README.md
│
├── docs/
│   ├── 00-roadmap.md
│   ├── 01-expression-trees.md
│   ├── 02-query-provider.md
│   ├── 03-expression-visitor.md
│   ├── ...
│
├── src/
│   ├── MiniEf.Core/
│   ├── MiniEf.Sql/
│   ├── MiniEf.Console/
│
├── tests/
│   └── MiniEf.Tests/
│
└── .github/
    ├── ISSUE_TEMPLATE/
    └── workflows/
```

