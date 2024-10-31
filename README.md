# SonarQube Setup with Docker Compose

This guide provides instructions to set up SonarQube in a Docker environment using Docker Compose. SonarQube is a popular tool for continuous code quality and security checks. This setup uses a PostgreSQL database for storing data.

## Prerequisites
- Docker and Docker Compose installed on your machine.
- An external PostgreSQL database accessible at `db_address` (replace with your actual database address).

## Create Volumes
- docker volume create --name=sonarqube_data
- docker volume create --name=sonarqube_logs
- docker volume create --name=sonarqube_extensions
- docker volume create --name=postgres_data

## Docker Compose Configuration

The `docker-compose.yml` file will run SonarQube with external volumes to persist data, logs, and extensions.

## Run Container
- docker-compose up -d

## Check Container logs
- docker logs sonarqube

## Go to SONARQUBE UI
- serveripaddress:9001

- Username: admin
- Password : admin