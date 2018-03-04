[![Codacy Badge](https://api.codacy.com/project/badge/Grade/c4667db20f45450489edd9cf440443a1)](https://www.codacy.com/app/prperiscal/general-purpose-eureka-service?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=prperiscal/general-purpose-eureka-service&amp;utm_campaign=Badge_Grade)

# general-purpose-environment

General purpose micro-services and architecture provide an extended and robust base from where a new project
can be started and developed following a consolidated agile approach and with the most used and assumed technologies in the 
micro-service spring development ecosystem.

Take a look on [General Purpose Environment](https://gist.github.com/prperiscal/900729941edc5d5ddaaf9e21e5055a62) to get more information on how everything integrates together and how the agile and continuous integration development should work.

# general-purpose-eureka-service

This project provides Netflix OSS integrations for Spring Boot apps through autoconfiguration and binding to the Spring Environment and other Spring programming model idioms. 

Client-side service discovery allows services to find and communicate with each other without hard coding hostname and port. The only ‘fixed point’ in such an architecture consists of a service registry with which each service has to register: this service.

## Contributing

Please read [CONTRIBUTING](https://gist.github.com/prperiscal/900729941edc5d5ddaaf9e21e5055a62) for details on our code of conduct, and the process for submitting pull requests to us.

## Workflow

Please read [WORKFLOW-BRANCHING](https://gist.github.com/prperiscal/ce8b8b5a9e0f79378475243e2d227011) for details on our workflow and branching directives. 

## Technologies involved

* [Spring 5.0.1.RELEASE](https://spring.io/) / [Spring boot 2.0.0.M7](https://projects.spring.io/spring-boot/)
* [Spring Cloud](https://cloud.spring.io/spring-cloud-netflix/)
  * [__Eureka Server__](https://github.com/Netflix/eureka/blob/master/README.md)

## Getting Started

Get you a copy of the project up and running on your local machine for development and testing purposes with:
```
git clone https://github.com/prperiscal/general-purpose-eureka-service
```
Also, this service can be started with docker:
```
docker pull quay.io/prperiscal/general-purpose-eureka-service:1.0.0-SNAPSHOT
```
Change the version as desire.

### Prerequisites

No prerequisites are need to run this service.

## Internals

Each micro-service who wants to register has to be hard coded the url of this service. That's why the definition of this path is critical and once defined
should not be changed.

The configuration is made inside the application.yml with the property:
```
eureka.client.service-url.defaultZone
```

## Authors

* **Pablo Rey Periscal** - *Initial work* -

See also the list of [contributors]() who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
