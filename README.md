# Innova Development Environment Docker

> Tested Environment Debian 9 Strench
> This Env contains the Database, Rabbitmq and Sbt for running Dataprocess

## Prerequestes
> Make sure that you have installed the following tools in linux


- Docker Engine (v.latest)
- Docker Compose (v.latest)
- Git (v.latest)

### Installed Features

- RabbitMQ (v.latest)
- SqlServer linux 2017
- Sbt (v.0.13.13)

## Install Procedure
1. bash: cd ~/
2. bash: git clone [dataprocess repo] to ~/dataprocess
3. change the configuration of rabbitmq (hostname: rabbitmq, user: rabbit, password: rabbit) and database connection (hostname: mssql, user: sa: password: Innova2018)
4. bash: mkdir ~/backups
5. base: docker-compose up (it could take 30 minutes for the first time because of dataprocess building)
6. Superviser the logs to make sure there is no problem

## Advices
I advice to use these containers in a VM isolated

## TODO
- Download and restore database
- Support Machine Learning


