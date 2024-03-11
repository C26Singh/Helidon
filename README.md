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


Helidon CLI 
which helps in generating and building Helidon projects.


Helidon for Beginner
After reading this book, you will be able to do the following.
– Create and consume RESTful services
– Package and deploy your applications to Kubernetes
– Develop observable applications and utilize health
checks, metrics, and tracing
– Secure your services using OpenID Connect
– Work with data
– Make your applications resilient
– Understand and use reactive messaging and
reactive streams


Who This Book Is For
Cloud native app using helodon
developing portable applications using MicroProfile and Jakarta EE,


issue tracker 
https://github.com/Apress/Beginning-Helidon/issues.

To compile samples, you need the following tools installed:
– Linux or macOS environment. On Windows we
recommend using Windows Subsystem for
Linux (WSL).
– JDK 17
– Maven 3.9.0
– Some samples rely on using utilities like cURL


Cloud native:
Applications designed to operate in a cloud environment
utilizing all cloud benefits are called cloud native.

The main benefit of the cloud is the ability to scale applications
quickly


And what’s the right design for your service? Cloud-native applications
have some specific requirements

Your application should be containerized.
Your application should be observable provide some telemetry data to help identify and
quickly fix problems.

Your application should consume the least amount of
memory possible. In a typical cloud environment, you
pay for RAM.

Your application disk image footprint should be as
small as possible

Java EE was an excellent choice for building on-premises, backend applications for years.

There was a need for a new Java framework for building cloud-native
applications to compete with Spring Boot.


Introducing Helidon
 Helidon is a set of Java libraries
for developing cloud-native service

Helidon was designed to achieve the following high-level goals.

Netty is an asynchronous event-driven network application
framework for rapidly developing maintainable high-performance
protocol servers and clients. (


 Helidon keeps the number of third-party dependencies low
by design.


There are two standards in the Enterprise Java world now:
Jakarta EE and MicroProfile. Helidon fully supports MicroProfile and
partially Jakarta EE/Jakarta

. Jakarta EE is a successor of Java EE

GraalVM Native Image creates a native executable from your Java
application. With GraalVM Native Image, you don’t need JVM anymore

Supporting GraalVM Native Image became
a standard feature for modern microservices frameworks like Quarkus
and Micronaut.


 Helidon is an open source product hosted on GitHub at
https://github.com/helidon-io/helidon and licensed under
the Apache 2.0 license.

Helidon has two flavors: Helidon MP and Helidon SE{to solve a problem}


Helidon MP                                                         Helidon SE
Declarative style APIs                                                    Functional style APIs
Blocking, synchronous                                                     Reactive, non-blocking
Small memory footprint                                                    Tiny memory footprint
Annotations are heavily used                                              No annotations
Jakarta Contexts and Dependency Injection (CDI)                           No dependency injection
Full support of MicroProfile and partial support of                       No Enterprise Java
Jakarta EE
standards support


Jakarta EE
MicroProfile


Microprofile config
Microprofile fault tolerance
Microprofile metrics
MP JWT AUTH
MP Health Check
MP tracing
MP REST Client
MP Open API
MP REactive streams Operators
MP reactive messaging
Jakarta CDI
Jakarta Restful Web services
Jakarta JSON Processing
Jakarta JSON Binding
JAkarta Websocket
Jakarta Persistence
Jakarta transactions
Jakarta annotations
Cors
gRPC server & Client


Helidon SE
SE features APIs based on Java SE Flow API
 . It intensively uses the Builder pattern, fluent APIs, and lambdas.
 Neither annotations nor dependency injection is used
 The produced
code is very clean, and you have complete control over what the code is
doing because the framework doesn’t generate any code at a build or run time

A drawback is that more coding is required. Also, reactive programming is not easy to use.

The reactive web server APIs are inspired by Express. It makes Helidon
SE a good choice for JavaScript developers who want to switch to Java.

 Express is a fast, unopinionated, minimalist web framework
for Node.js

Note-But to use it effectively, you as a player need to know
how to play for this character. One wrong move, one slow reaction, and
your warrior is dead.

Which Flavor Should You Use?
MP or SE

you can use SE into MP but not vice versa.
Most MP features requires an initialized CDI container which doesn’t exist in SE.

Example Helidon SE functionality in Helidon MP is
reactive messaging

Tip If you don’t know which flavor to use, use Helidon MP

Use Helidon MP 
• You don’t know what flavor to choose.
• You want to use CDI and other MicroProfile
or Jakarta EE APIs.
• You are migrating from the existing
Java EE/Jakarta EE application.
• You are a Spring Boot or Java EE
developer and want a similar development
experience.

Use Helidon SE

•  Performance achieved by heavy
usage of concurrency is your
primary goal.
• You want to have complete control
of your application.
• You have experience with reactive
programming.
• Your application deals with
uploading files.
• Your application is not CDI based,
and you are not planning to use
any MicroProfile and Jakarta EE
APIs.


Summary
• Applications designed to operate in a cloud
environment utilizing all cloud benefits are called
cloud native.
• Helidon is a set of Java libraries for developing cloudnative services.
• Helidon comes in two flavors: Helidon MP (declarative
style APIs implementing MicroProfile and some
Jakarta EE specifications) and Helidon SE (reactive,
non-blocking APIs).
If you don’t know which flavor to use, use
Helidon MP.
