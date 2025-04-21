# EMS AlgaSensors
This is a project built during the AlgaWorks Microservices Specialist Course (EMS) Level 1 - Software architecture and microservices.

It simulates a temperature management application and has 3 microservices as submodules:

# device-management
Sensors CRUD, configuration and remote management.

Endpoints:
- `POST /api/sensors`: create a new sensor
- `GET /api/sensors`: retrieve all sensors
- `GET /api/sensors/{sensorId}`: retrieve a specific sensor
- `PUT /api/sensors/{sensorId}`: update a specific sensor
- `DELETE /api/sensors/{sensorId}`: delete a specific sensor
- `PUT /api/sensors/{sensorId}/enable`: activate a specific sensor
- `DELETE /api/sensors/{sensorId}/enable`: deactivate a specific sensor

# temperature-processing
Temperatures real time data receiver.

Endpoints:
- `POST /api/sensors/{sensorId}/temperatures/data`: receive sensor data

# temperature-monitoring
Temperatures data analysis and reports.

Endpoints:

- `GET /api/sensors/{sensorId}/temperatures`: retrieve all temperature registrations
- `PUT /api/sensors/{sensorId}/alert`: update a specific temperature alert configuration
- `GET /api/sensors/{sensorId}/alert`: retrieve a specific temperature alert configuration
- `DELETE /api/sensors/{sensorId}/alert`: delete a specific temperature alert configuration
- `GET /api/sensors/{sensorId}/monitoring`: retrieve a specific temperature monitoring
- `PUT /api/sensors/{sensorId}/monitoring/enable`: activate a specific temperature monitoring
- `DELETE /api/sensors/{sensorId}/monitorig/enable`: deactivate a specific temperature monitoring

# The technologies involved are:
- Java 21 with Lombok
- Spring Boot with Spring Web, Spring Data JPA and Spring AMQP
- RabbitMQ
- Docker
- Gradle
