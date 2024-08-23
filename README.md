# api-bakeoff
This is a repository for showing benchmarks and comparison of API backends/tools/fraemworks used to serve API's. This is NOT used to test tools used for CALLING API's (ie Postman). 

Each tool will be judged on the following set of parameters:

- **Hardware** : For fairness of testing, all tests will be done on AWS free-tier. This includes Lambdas as well as EC2 (as they have the same hardware settings currently). If this changes (or internal bandwidth settings change), we will move to a different platform. (EC2 free-tier : t2.micro	1vCPU/1GB Ram) (Lambda Free Tier: 1vCPU, shared RAM)
  - cores : 1
- **Security** : Processing affects how fast th response is returned and that includes any type of security checks. Like armor, it slows you down but makes you safe. Unless you like people mining your database, every API backend has to include a minimum amount of security to be able to make sure the client is safe and secure.
  - JWT token : boolean
  - Session : boolean
  - CORS : boolean
  - RBAC : boolean
  - ABAC  : boolean
- **ResourceType** : Some systems come with built in caching to make their systems faster and easier to setup. Others do not and rely on developers to understand how to setup caching. I give bonus points to those that provide caching solutions with their backend tooling out of the box.
  - RDBMS : boolean
  - NoSQL : boolean
  - Cached : boolean
- **Test Parameters** : We don't mess around when it comes to the test. It is meant as a stress test (not a benchmark). This is meant to really show what happens to the system when we push it on a small system with limited resources. A good backend 
  - Concurrency : 1000
  - Request : 3000
  - Passes : boolean

Test will be an automated JAVA APPLICATION that can be run REMOTELY AND CODE WILL BE SUPPLIED.
