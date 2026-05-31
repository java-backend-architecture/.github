# Java Backend Architecture

Reference implementations of backend architecture patterns. Each repository explores one concept in isolation — structure, boundaries, design decisions.

## Focus areas

* Clean Architecture · Hexagonal · DDD
* Application layering and use-case design
* Infrastructure and integration patterns
* API design and communication styles

## Repositories

### Graph Extraction

| Repository | What it demonstrates |
|---|---|
| [persistence-graph-extraction-jdbc](https://github.com/java-backend-architecture/persistence-graph-extraction-jdbc) | Object graph from flat SQL JOIN results — manual deduplication via `computeIfAbsent` |
| [persistence-graph-extraction-jooq](https://github.com/java-backend-architecture/persistence-graph-extraction-jooq) | Object graph using jOOQ `MULTISET` — no projections, no deduplication |
| [persistence-graph-extraction-jpa](https://github.com/java-backend-architecture/persistence-graph-extraction-jpa) | Object graph using JPA + Blaze Persistence Entity Views — optimized queries, no N+1 |

### Pagination

| Repository | What it demonstrates |
|---|---|
| [persistence-flat-pagination-jdbc](https://github.com/java-backend-architecture/persistence-flat-pagination-jdbc) | Offset-based pagination for flat entity queries — `LIMIT / OFFSET` and `COUNT(*)` |
| [persistence-flat-pagination-sorting-jdbc](https://github.com/java-backend-architecture/persistence-flat-pagination-sorting-jdbc) | Pagination with multi-field sorting — dynamic `ORDER BY` with SQL injection protection |
| [persistence-graph-pagination-jdbc](https://github.com/java-backend-architecture/persistence-graph-pagination-jdbc) | Pagination over a multi-level object graph — subquery prevents JOIN row truncation |

## Author

[Dmitrii Russu](https://github.com/Dmitrii-Russu)
