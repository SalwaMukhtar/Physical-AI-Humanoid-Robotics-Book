---
sidebar_position: 1
---

# ROS 2 Fundamentals

This chapter covers the fundamental concepts of ROS 2.

## Nodes

A ROS 2 node is a process that performs computation. It is a fundamental concept in ROS 2, and a robot system is typically composed of many nodes. For example, a node might be responsible for controlling a motor, reading a sensor, or planning a path.

Nodes can communicate with each other using topics, services, and actions.

## Topics

Topics are named buses over which nodes exchange messages. Topics are one of the main ways that data is moved between nodes and other parts of the system.

A node can publish messages to a topic, and any number of nodes can subscribe to that topic to receive the messages.

## Services

Services are another way for nodes to communicate. They are based on a request-reply model. One node offers a service, and another node can call that service. The service call blocks until the service provider has completed the request and returned a result.
