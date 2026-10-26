# Service Discovery

A Spring Boot microservices project demonstrating **Service Discovery** — a mechanism that allows microservices to register themselves with a central registry and discover other services dynamically without hardcoding their network locations.

## Overview

In a microservices architecture, services may run on different hosts or ports, and their locations can change over time. Service Discovery simplifies service-to-service communication by maintaining a registry of available service instances.

This project is intended to demonstrate the fundamentals of service registration and discovery using Java and Spring Boot.

## Tech Stack

- **Language:** Java
- **Framework:** Spring Boot
- **Build Tool:** Maven
- **Microservices Infrastructure:** Spring Cloud
- **Service Registry:** Netflix Eureka, if configured in this project

## Key Concepts

- Service registration and discovery
- Centralized service registry
- Dynamic service lookup
- Microservices architecture
- Spring Boot application configuration

## Architecture

```text
        +----------------------+
        |  Service Registry    |
        |   (Eureka Server)    |
        +----------+-----------+
                   |
          Registers / Discovers
                   |
          +--------+--------+
          |                 |
    +-----v------+    +-----v------+
    |  Service A |    |  Service B |
    +------------+    +------------+
```

*Illustrative architecture; adapt it to the services actually implemented in this repository.*

## Getting Started

### Prerequisites

- Java Development Kit (JDK)
- Maven or the included Maven Wrapper
- An IDE such as IntelliJ IDEA

### Clone the Repository

```bash
git clone https://github.com/vivek-codes-source/ServiceDiscovery.git
cd ServiceDiscovery
```

### Build the Project

On Windows:

```bash
mvnw.cmd clean package
```

On macOS or Linux:

```bash
./mvnw clean package
```

### Run the Application

On Windows:

```bash
mvnw.cmd spring-boot:run
```

On macOS or Linux:

```bash
./mvnw spring-boot:run
```

## Learning Outcomes

- Understanding service discovery in distributed systems
- Exploring Spring Boot and Spring Cloud
- Learning how microservices can locate one another dynamically
- Understanding the role of a service registry in a microservices architecture

## Future Enhancements

- Integrate multiple sample microservices
- Configure client-side service discovery
- Integrate an API Gateway
- Add health checks and monitoring
- Explore load balancing across service instances

## Author

**Vivek Kumar Sahu**

GitHub: [vivek-codes-source](https://github.com/vivek-codes-source)

---

*This project is part of my journey toward building a strong foundation in Java backend development and microservices architecture.*
