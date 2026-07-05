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
│   ├── 01-expression-trees.md
│   ├── 02-query-provider.md
│   ├── 03-expression-visitor.md
│   ├── ...
│
├── src/
│   ├── ChitMeo.MiniEf.Core/
│   ├── ChitMeo.MiniEf.Sql/
│   ├── ChitMeo.MiniEf.Console/
│
├── tests/
│   └── ChitMeo.MiniEf.Tests/
│
└── .github/
    ├── ISSUE_TEMPLATE/
    └── workflows/
```

# The final API should look like this
```csharp
var sql = db.Users
    .Where(x => x.Age > 18)
    .Where(x => x.Name.StartsWith("A"))
    .OrderBy(x => x.Name)
    .Select(x => new
    {
        x.Id,
        x.Name
    })
    .ToSql();
```
Expected output:
```sql
SELECT Id, Name
FROM Users
WHERE Age > 18
AND Name LIKE 'A%'
ORDER BY Name
```
# Definition of Done (for Every Issue)

Every issue must satisfy the following checklist.

## Objective

Describe exactly one concept to learn.

## Prerequisites

List the required knowledge.

## Input

Provide the input code or data.

## Expected Output

Provide the exact expected result.

## Requirements
Use only the .NET Base Class Library (BCL)
Do not use third-party libraries
Keep the implementation clean and readable
Write meaningful comments where appropriate
## Checklist
- [ ] Implementation completed
- [ ] Unit tests added
- [ ] Console demo added
- [ ] Documentation updated
- [ ] Code reviewed
- [ ] All tests pass

## Bonus Challenge

Optional advanced exercise for deeper understanding.
