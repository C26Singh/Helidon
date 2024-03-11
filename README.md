# Helidon
Why Helidon?

Helidon is a collection of Java libraries for creating microservices-based applications.
modern and lightweight framework for building microservices in Java
well-suited for building cloud-native applications that can scale and perform well in distributed environments.


Helidon SE (Simple Edition):
lightweight framework that allows developers to build microservices using a functional programming model
It is designed to be flexible and can be used to build both traditional RESTful services and reactive microservices.


Helidon MP (MicroProfile):
Helidon MP is a set of libraries that implements the MicroProfile specifications for building microservices
MicroProfile is a set of standards for building microservices-based applications in Java
Helidon MP provides implementations of specifications such as JAX-RS for building RESTful APIs, CDI for dependency injection, and JSON-P for working with JSON data.

Use Helidon MP if

You want to base your application on modern enterprise Java standards such as Jakarta EE and MicroProfile.

You are familiar with Java EE, Jakarta EE or Spring Boot and would like to have a similar development experience.

You are migrating existing Java EE/Jakarta EE application to microservices.

You are planning to use CDI components or extensions.

You are planning to use JPA for data access and Jersey (JAX-RS) for RESTful services.


Prerequisites
Helidon requires Java and Maven. You might also need Docker and Kubernetes depending on how you plan to deploy your services.

Helidon requires Java 17+.
http://jdk.java.net/


Helidon requires Maven 3.6.1+.
https://maven.apache.org/download.cgi


You need Docker if you want to build and deploy Docker containers.
https://docs.docker.com/install/

If you want to deploy to Kubernetes, you need kubectl and a Kubernetes cluster (you can install one on your desktop.
https://kubernetes.io/docs/tasks/tools/install-kubectl/


