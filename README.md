The Spring Integration Tutorial
===============================

# Tutorial Structure / Ideas

There are numreous ways we can develop a tutorial for *Spring Integration* and *Spring Batch*. I think the tutorial should be a continuation of the [Spring MVC Tutorial] (https://github.com/joshlong/the-spring-tutorial).

Basically, we have a **Customer Relationship Manager** (CRM) application that will be extended to provide the following 2 use-cases:

1. When users/customers are added, retrieve additional data from an external systems (using *Spring Integration*), e.g. (suggestion):
  - Convert (geocode) address information into Latitude/Longitude coordinates using WS/REST calls
  - Calculate periodically or upon event (e.g. user added) agregate data points, e.g. how many customer are in the same Zip/Postal Code. Trigger (Email) notifications, once certain thresholds are exceeded - e.g. more than 5 customers exist in the same ZIP/Postal  Code
  - Do a periodic data export and transfer the data via SFTP to a remote server
2. Provide a bulk-data import feature (utilizing *Spring Batch*). E.g. a CSV file, containing customer information is droped into a directory and we must pick it up, process and import the data. 

It looks like we could utilize [http://beta.generatedata.com/](http://beta.generatedata.com/) to generate interesting sets of sample data. 

3. As an adavanced chapter, we could demonstrate how to modularize portions of the application, e.g. using *RabbitMQ*
  - Take a look at Mark Fisher's Spring One demo: https://github.com/markfisher/springone-wgrus/tree/master/modular

To outline some of the contents, I have been using my [2012 SpringOne presentation](http://www.slideshare.net/hillert/introduction-to-spring-integration-and-spring-batch).

# Overview of the Tutorial

Over the course of this tutorial, you will learn how to use *Spring Integration*. We will show how to use *Spring Integration* to connect and integrate with external systems but we will also show how you can use *Spring Integration* as an **Intra Application Framwork** in order to improve maintainability and scalaiblity.

Furthermore, we will implement a use-case to handle the processing of large files using *Spring Batch*.

# Introduction to Spring Integration

* Light-weight messaging framework
* Provides an adapter-based platform

## Common Patterns

1. Retrieve
2. Parse
3. Transform
4. Transmit

## Enterprise Integration Patterns

Pipes and Filters at the core of Spring Integration’s architecture

* Endpoint (Filter)
* Channel (Pipe)
* Message

### What is in a Message?

* Structure of a Message
  - Headers
  - Payload
* Function of a Message
  - Document Message
  - Command Message
  - Event Message

### What is a Channel?
### What is an Endpoint?

### Common Enterprise Integration Patterns

#### Router
#### Transformer
...

## Why would I care?

Provides building blocks to implement systems that:

* are loosely Coupled (Logically or Physically)
* are Event Driven (EDA)
* have a staged event-driven architecture (SEDA)

Sophisticated support for synchronous / asynchronous messaging

## Integration Styles

* Business to Business Integration (B2B)
* Inter Application Integration
* Intra Application Integration

## Deployment Options

* Embedded as a library
* Stand-alone deployment
* War deployment

## Spring Integration Components and Adapters

Spring Integration provides many components...

# Build a first Spring Integration Application

> Not sure how this could changed to provide a better flow with the CRM sample application. Right at this point I would like to demonstrate the most simple Spring Integration Hello World example. The example below basically representst one of the Spring Integration STS templates.

User enters `String`, which will passed to the Gateway and the *Transformer* will convert the String to upper-case and the upper-case String is returned to the user.

1. Gateway
2. Request Channel
3. Transformer

- Explain the Gateway
- Explain Request Channel
- Explain the Transformer
- Explain that sometimes different component can accomplish the same task. Choose the component that fits functionally and semantically. E.g. instead of a Transformer you can use a *Service Activator*. 

- Show a very explicit sample first, e.g. with channels defined. Explained which elements are created implicitly, e.g. leave off the channels.

# The Channel Deep-Dive

* Direct Channel (Single Thread)
* Queue Channels

# Pollers

Pollers are used in both inbound and outbound messaging scenarios. Here are some use-cases that illustrate the scenarios in which Pollers are used:

* Polling certain external systems such as FTP Servers, Databases, Web Services
* Polling internal (pollable) Message Channels
* Polling internal services (E.g. repeatedly execute methods on a Java class)

# Integration with External Systems (Sample)

> This should probably be some more involved example using either the Twitter adapters or some other web-service to retrieve data (ideally retrieve data from multiple source) Aggregate them, process them and ultimately send them some place else (e.g. email)

# Modularizing the CRM Application

TBD

# Spring Batch

## Overview

TBD

### Integration Options between Spring Batch and Integration

Illustrate functionality provided by the Spring Batch Integration module: https://github.com/SpringSource/spring-batch-admin/tree/master/spring-batch-integration

## The Sample

* Add flat-file import capabilities to the CRM application.



