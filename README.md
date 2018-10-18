# Microservices example
This is example of microservice architecture pattern

### Example consist of 5 microservices
![-](/etc/diagram.png)

### UI gateway
This microservice performs authentication and routing to UI microservice

##### SSL
`ui-gateway` works on port 443. SSL certificate was created by using following command:
```
keytool -genkey -alias test_key -storetype PKCS12 -keyalg RSA -keysize 2048 -keystore keystore.p12 -validity 3650
```
and with *qwerty* password.

### Service Discovery server
Eureka server is used

### Config server
This microservice stores configs of all microservices

### Items UI
Example of UI

### Items service
Example of backend

### Implemented with
* Java 11
* Kotlin
* Spring Cloud (Spring Cloud Gateway, Netflix (Eureka, Hystrix, Feign, Ribbon))
* Gradle Kotlin DSL
* JUnit

### Other used technologies
* Webjars
* Thymeleaf
