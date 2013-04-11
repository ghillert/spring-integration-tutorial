The Spring Integration Tutorial
===============================

# Introduction

* Light-weight messaging framework
* Provides an adapter-based platform

## Common Patterns

1. Retrieve
2. Parse
3. Transform
4. Transmit

## Enterprise Integration Patterns

Using Spring Integration as an Intra Application Framwork
Handle Large Files Using Spring Batch

Pipes and Filters at the core of Spring Integration’s architecture

* Endpoint (Filter)
* Channel (Pipe)
* Message

### What is in a Message?
### What is a Channel?
### What is an Endpoint?

### Common Enterprise Integration Patterns

#### Router
#### Transformer

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

User enters `String`, which will passed to the Gateway and the *Transformer* will convert the String to upper-case and the upper-case String is returned to the user.

1. Gateway
2. Request Channel
3. Transformer

- Explain the Gateway
- Explain Request Channel
- Explain the Transformer
- Explain that sometimes different component can accomplish the same task. Choose the component that fits functionally and semantically. E.g. instead of a Transformer you can use a *Service Activator*. 

- Show a very explicit sample first, e.g. with channels defined. Explained which elements are created implicitly. 

# The Channel Deep-Dive

* Direct Channel 
* Queue Channels

# Pollers

Pollers are used in both inbound and outbound messaging scenarios. Here are some use-cases that illustrate the scenarios in which Pollers are used:

* Polling certain external systems such as FTP Servers, Databases, Web Services
* Polling internal (pollable) Message Channels
* Polling internal services (E.g. repeatedly execute methods on a Java class)

## Integration with External Systems (Sample)

...


