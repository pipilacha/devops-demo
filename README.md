### This repo functions as a centrilazed hub for the microservices that make the voting app work
This a multiple repo version of [LFS261-example-voting-app](https://github.com/pipilacha/LFS261-example-voting-app) which is a mono-repository project.

CI is handled by jenkins running in a Docker container. Every repo has it's own Jenkinsfile that it is used to run the Pipeline for the project.

Architecture
-----
Microservices:
- [vote-app](https://github.com/pipilacha/vote-app)

![Architecture diagram](https://github.com/pipilacha/LFS261-example-voting-app/blob/master/architecture.png)

* A Python webapp which lets you vote between two options
* A Redis queue which collects new votes
* A .NET worker which consumes votes and stores them in…
* A Postgres database backed by a Docker volume
* A Node.js webapp which shows the results of the voting in real time
