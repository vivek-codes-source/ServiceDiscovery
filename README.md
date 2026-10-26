Service Discovery

A Service Discovery Server built using Spring Boot and Netflix Eureka Server. It provides a central registry where microservices can register themselves and discover other registered services dynamically.

🚀 Overview

In a microservices architecture, services need a reliable way to find and communicate with one another without hardcoding hostnames or port numbers.

This project uses Netflix Eureka Server to provide a centralized service registry for service registration and discovery.

🛠️ Tech Stack
Java 17
Spring Boot 4.1.0
Spring Cloud Netflix Eureka Server
Apache Maven
Lombok
Spring Boot DevTools
✨ Key Features
Centralized service registry for microservices.
Dynamic service registration and discovery.
Reduced dependency on hardcoded service URLs.
Integration with the Spring Cloud ecosystem.
Maven-based build and dependency management.
📋 Prerequisites

Make sure you have the following installed:

Java Development Kit (JDK) 17
Maven, or use the included Maven Wrapper
Git
📥 Getting Started
1. Clone the repository
bash
git clone https://github.com/vivek-codes-source/ServiceDiscovery.git

2. Navigate to the project directory
bash
cd ServiceDiscovery

3. Build the project

On Windows:

bash
mvnw.cmd clean package


On Linux or macOS:

bash
chmod +x mvnw
./mvnw clean package

4. Run the application

On Windows:

bash
mvnw.cmd spring-boot:run


On Linux or macOS:

bash
./mvnw spring-boot:run

⚙️ Configuration

Configure the Eureka server in src/main/resources/application.properties or application.yml.

Example configuration for a standalone Eureka server:

properties
spring.application.name=service-discovery
server.port=8761

eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false


Note: Add or verify these settings in your project before relying on this configuration. The example assumes a standalone Eureka server.

🌐 Access the Eureka Dashboard

After starting the application, open:

text
http://localhost:8761


The Eureka dashboard displays registered services when the server is configured and running correctly.

🏗️ Architecture
text
        Service A
            |
            | Register / Discover
            |
            v
    +-------------------+
    | Eureka Server     |
    | Service Registry  |
    +-------------------+
            ^
            | Register / Discover
            |
        Service B

Service Discovery Server: Maintains the service registry.
Service A and Service B: Register with Eureka and discover other services when configured as Eureka clients.
📁 Project Structure
text
ServiceDiscovery/
├── src/
│   ├── main/
│   │   ├── java/
│   │   └── resources/
│   └── test/
├── .mvn/
├── mvnw
├── mvnw.cmd
├── pom.xml
└── README.md

🧪 Testing

Run the test suite using the Maven Wrapper.

Linux/macOS:

bash
./mvnw test


Windows:

bash
mvnw.cmd test

📚 Learning Objectives
Understanding service discovery in microservices.
Setting up a Netflix Eureka Server.
Exploring service registration and discovery.
Learning the fundamentals of Spring Cloud.
🤝 Contributing

Contributions, suggestions, and improvements are welcome.

Fork the repository.
Create a feature branch.
Commit your changes.
Open a pull request.
📄 License

No license information has been specified. Please check the repository for licensing terms before reusing or distributing this project.
