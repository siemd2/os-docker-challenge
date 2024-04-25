# Docker Challenges Project README

## Overview

This repository contains a series of Docker challenges designed to enhance understanding and practical skills in containerization, in line with the Operating Systems and Cloud Computing course content. The challenges are focused on real-world applications and are valuable for both academic learning and professional development.

## Project Structure

The project is structured into directories corresponding to each challenge, with configurations for Docker scenarios:

- `challenge3/`: A Docker Compose setup for a full-stack application with a web server, Node.js app, and database.
- `challenge4/`: Extends `challenge3/` by adding configurations for scaling the Node.js service.

Contents of each directory include:

- `Dockerfile`: Instructions for Docker image creation.
- `docker-compose.yml`: YAML file that defines services, networks, and volumes.
- `variables.env`: Environment variables for the services.

## Setup and Execution

### Prerequisites

- Git
- A public GitHub account
- Docker installed on your machine

### Getting Started

1. Clone or fork this repository.
2. Navigate to the desired challenge directory.

### Challenge 3: Full Stack Application

To run the full-stack application:

1. Ensure you are in the `challenge3/` directory.
2. Configure `.env` with the required environment variables.
3. Use Docker Compose to build and start the services:

    ```sh
    docker-compose up --build
    ```

4. Access the app via `http://localhost:8080/api/books` and `http://localhost:8080/api/books/1`.

### Challenge 4: Scaling Up an Application

For application scaling:

1. Switch to the `challenge4/` directory.
2. Scale `node-service` using Docker Compose:

    ```sh
    depends_on:
      - db
    # ports:
    #   - "3000:3000"
    scale: 3
    ```

3. Test the load balancing by requesting `http://localhost:8080/api/stats`.

## Learning Outcomes

- knowledge of Docker and its ecosystem.
- Experience with full-stack application deployment and service scaling.
- Insight into the use of environment variables for configuration.


## Author

Siem Debesay

