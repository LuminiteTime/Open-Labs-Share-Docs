### Services:
- **API Gateway (Authentication)** -> all other services
- **Users** - users' data (e.g. name, labs solved, labs published, properties, etc)
- **Karma** - users' rating, penalties, awards, balance b/w solved & checked labs, fucking maths formulas
- **Labs** - labs files operations
- **Feedback** - discussions (like in Stepik), reviews, ratings for labs (after completion)
- **Questionary** - check knowledge after reading labs, tests, open questionaries

### Storage:
- s3 (minIO, if it is free) - files storage
- PostgreSQL - users' data, reviews, labs mapping to files in s3, karma points

### Inter-services Communication
- gRPC

### Frontend Communication
- REST
- [[API Endpoints]]

### MVP Architecture

![[ArchitectureLayout.png]]

