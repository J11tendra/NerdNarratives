# What is MQTT Protocol?

## Table of Contents

- [Introduction](#introduction)
- [What is MQTT?](#what-is-mqtt-1)
- [Importance of MQTT in IoT](#importance-of-mqtt-in-iot)
- [Understanding MQTT](#understanding-mqtt)
- [What are MQTT Components?](#what-are-mqtt-components)
- [Understanding MQTT With An Example](#understanding-mqtt-with-an-example)
- [Conclusion](#conclusion)

## Introduction

Welcome to the second article of our API series! In this article, we will learn about the MQTT protocol and its architecture, components, and real-world applications. If you are new to the series, we recommend starting with our first article where we discussed the basics of APIs and how they function.

**If you haven't read the first article yet, be sure to check it out:** [What is an API and How Does it Work?](https://dev.to/jitendrachoudhary/what-is-an-api-5225)

Now, let's continue with the MQTT protocol.

<!-- Image of Smart Home System -->

![IoT?](https://github.com/J11tendra/NerdNarratives/blob/main/What-is-MQTT-Protocol/assets/IoT.png?raw=true)

## What is MQTT?

<!-- A. Explanation of MQTT -->

MQTT stands for Messaging Queuing Telemetry Transport. MQTT is a standard messaging protocol for machine-to-machine communication. Smart home systems, scanners, sensors, and other IoT (Internet of Things) send and retrieve data over a network having a limited bandwidth. For devices having limited hardware capabilities, MQTT proves to be an efficient architecture for communication.

<!-- Image of Smart Home System -->

![Computer Hardware?](https://github.com/J11tendra/NerdNarratives/blob/main/What-is-MQTT-Protocol/assets/computer-hardware.png?raw=true)

## Importance of MQTT in IoT

<!-- B. Importance in IoT and remote communication -->

MQTT is the standard protocol for IoT devices to communicate with other machines. here are some main reasons:

**Lightweight And Scalable**

MQTT can be implemented on IoT devices with minimal usage of resources. It can even be used on microcontrollers. MQTT headers are small so that you can optimize the network bandwidth. As implementation of MQTT requires fewer resources it also requires less code that consumes very little power. MQTT also has built-in features so you get support for large IoT devices for communication.

**Reliable And Secure**

IoT devices connect via unreliable networks. MQTT re-connects quickly with built-in features. It offers three levels of quality-of-service for IoT use cases. MQTT also makes it easy to encrypt messages and authenticate devices and users using modern protocols such as OAuth and TLS1.3.

<!-- II. Understanding MQTT -->

## Understanding MQTT

<!-- A. Architecture overview -->

MQTT protocol uses a publish/service model for communication. Whereas, in HTTP a client sends a request for data or resources and the server responds with data after authentication. This is a very straightforward approach. However, In MQTT protocol works on the principles of the publish/subscribe model where it decouples the publisher (message provider) from the subscriber (message receiver). There is a message broker which handles all the communication between the publisher and the subscriber. The message broker filters the messages received from the publisher and correctly sends them to its subscriber; not exposing the two parties to each other. The broker does the decoupling as below:

**Space decoupling**

The two parties (publisher and subscriber) are not aware of each other's network information like IP addresses, port numbers, or even location.

**Time decoupling**

The publisher and subscriber don’t run or have network connectivity at the same time.

**Synchronization decoupling**

Both publishers and subscribers can send or receive messages independently without interrupting each other. For example, the subscriber does not have to wait for the publisher to send a message.

## What are MQTT components?

<!-- Image of How MQTT works -->

![How MQTT Works(diagram)?](https://github.com/J11tendra/NerdNarratives/blob/main/What-is-MQTT-Protocol/assets/mqtt-working.png?raw=true)

**MQTT Client**

A MQTT client is anything as big as a server or as small as a microcontroller that runs a MQTT library. If the client is sending messages, it acts as a publisher, and if it is receiving messages, it acts as a subscriber. Any device that communicates using MQTT over a network can be called an MQTT client device.

**MQTT broker**

The MQTT broker is a vital component that acts as a mediator between different clients. Its primary functions include receiving and filtering messages, identifying subscribed clients, and delivering the messages to them. In addition, the MQTT broker is responsible for other critical tasks such as authenticating and authorizing MQTT clients, forwarding messages to other systems for analysis, and managing missed messages and client sessions.

**MQTT connection**

To establish communication, clients and brokers use an MQTT connection. The MQTT client initiates the connection by sending a CONNECT message to the broker. The broker acknowledges the connection by responding with a CONNACK message. Communication between clients and the broker requires a TCP/IP stack. It's important to note that clients can only connect with the broker and not with each other.

## Understanding MQTT With An Example

Imagine you have a smart home setup with various IoT devices like sensors, switches, and lights. You want to control and monitor these devices remotely using your smartphone or computer. MQTT can facilitate communication between your devices and your control interface (smartphone or computer) efficiently and reliably.

<!-- Image of Smart Home System -->

![Smart Home System?](https://github.com/J11tendra/NerdNarratives/blob/main/What-is-MQTT-Protocol/assets/mqtt-connection.png?raw=true)

1. **Setup**:

   - You have an MQTT broker installed on a server (which could be a cloud-based service or a local server).
   - Each IoT device in your home (e.g., temperature sensors, motion sensors, smart lights) is equipped with an MQTT client.

2. **Publishing Data**:

   - Your temperature sensor periodically measures the temperature in a room.
   - When the temperature reading is taken, the sensor publishes this data to a specific MQTT topic, such as "home/living_room/temperature."
   - Similarly, your motion sensor detects movement and publishes an event to the topic "home/kitchen/motion."

3. **Subscribing to Topics**:

   - Meanwhile, your smartphone or computer is running an MQTT client application.
   - You subscribe to the topics you're interested in, such as "home/+/temperature" to receive temperature data from all rooms, or "home/+/motion" to monitor motion events in different areas.

4. **Receiving and Acting on Data**:

   - When a temperature reading is published to the "home/living_room/temperature" topic, your MQTT client on the smartphone receives this data.
   - The client application can then display the temperature on your smartphone's interface in real-time.
   - If the motion sensor in the kitchen publishes a "motion detected" event to the "home/kitchen/motion" topic, your smartphone receives this notification.

5. **Controlling Devices**:
   - Let's say you want to turn on the lights in your living room remotely.
   - You send a command to the MQTT broker, publishing a message to the topic "home/living_room/lights/set" with the desired action (e.g., "turn on").
   - The MQTT broker forwards this command to the MQTT client running on the smart light switch in your living room.
   - The smart light switch receives the command and turns on the lights accordingly.

## Conclusion

MQTT is a reliable and lightweight protocol that connects and controls IoT devices over constrained networks. It uses a publish/subscribe model that ensures efficient communication and enables remote monitoring and control. Its security features and support for various quality-of-service levels make it indispensable for a wide range of applications.

If you have read this far and find my blogs worth reading feel free to follow me here so you can get my next blog update straight in your feed.

**Interested in connecting on X? Say me Hi at [@JitendraC](https://twitter.com/jiitendraC)**

## Related Article: A Comprehensive Guide to MQTT Protocol

If you found this article informative and want to learn more about the MQTT protocol, be sure to check out [MQTT v5 – New Opportunities For IoT Development](https://mobidev.biz/blog/mqtt-5-protocol-features-iot-development).
