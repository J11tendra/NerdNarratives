<!-- Banner Image -->

## Introduction

API is really useful for the integration of new applications with existing software systems. You don't have to build everything from scratch, API provides ready-to-use functionalities for your project.

A lot of times you hear the term "API" from other devs, Do you know what exactly "API" is? How it works? In this article, we'll learn about API.

<!-- api-working -->

![API Working](https://github.com/J11tendra/NerdNarratives/blob/main/what-is-api/assets/api-working.png?raw=true)

## What is API?

API stands for Application Protocol Interface. API is a mechanism that enables two different software components to communicate with each other which has its own set of rules and protocols.

In API, one application is a client and the other is a server. Here, the client can your mobile, laptop, or computer you are using to surf the internet. The server is a bigger computer that stores the data. A protocol is nothing but a set of rules to communicate.

So, let's understand this with an example: Imagine there is a vending machine in front of you. This machine can give you all sorts of drinks and snacks you need. You need to ask the machine in a specific way i.e. you select the goods you need and use a credit/debit card or maybe cash. That is kind of how an API works, but instead of snacks it delivers you the information and action on the server.

But, What is an API? Well, think of it like this: you have social media, games, and even weather apps on your phone/computer. All of this does some different work. Let's say the weather app shows today's weather information. But, the app doesn't create weather information itself, It talks to a server via an API and gets back the information you requested.

<!-- Image of vending machine -->

![Vending Machine Example](https://github.com/J11tendra/NerdNarratives/blob/main/what-is-api/assets/vending-machine.png?raw=true)

## How API Works?

Computers follow protocols to communicate with each other. Without a protocol, they don't have an expected form of communication.

Likewise, without a protocol, you press a button to get a lemonade from the vending machine. However, the machine returns coconut water. It's all chaos, right? This is where protocol comes in, it tells you what to do step by step, like "insert money, select an item, press the button," and so on.

Now, just like how vending machines have different protocols for different snacks (press A for lemonade, and B for coconut water), the internet also uses different protocols for different tasks.

On the web, there is HTTP protocol (which stands for Hyper Text Markup Language). APIs on the web use the HTTP protocol because it's easy to use and it's popular. The client requests along with a set of information so the server responds accordingly. The information sent along with the request includes:

- **URL** – a web address where you want to make a request
- **Method** – whether you want data already stored somewhere or want to save new data in a database e.g. GET, POST, DELETE, PUT, etc.
- **Header** – all the relevant information about your request including in what format the client device expects to receive the data
- **Body** – the body contains the actual requested data

<!-- api architecture -->

![API Architecture](https://github.com/J11tendra/NerdNarratives/blob/main/what-is-api/assets/api-architecture.png?raw=true)

## API Protocols

As the use of web APIs has increased, it has led to the development of certain protocols. These protocols provide users with a set of defined rules, or API specifications that create accepted data types commands, and syntax.

**SOAP API (Simple Object Access Protocol)**

These APIs use Simple Object Access Protocols. Client and server exchange messages using XML. This is a less flexible API that was more popular in the past.

**XML-RPC & JSON-RPC API (XML-Remote Procedure Call)**

These APIs are called Remote Procedure Calls. The client completes a function (or procedure) on the server, and the server sends the output back to the client mainly in XML or JSON.

**Websocket API**

Websocket API is another modern web API development that uses JSON objects to pass data. A WebSocket API supports two-way communication between client apps and the server. The server can send callback messages to connected clients, making it more efficient than REST API.

**REST APIs**

These are the most popular and flexible APIs found on the web today. The client sends requests to the server as data. The server uses this client input to start internal functions and returns output data to the client.

## Types of API

Today most APIs are web APIs that expose an application's data and functionality over the internet. Here are the four main types of web API:

**Open API**

Open APIs are open source application programming interfaces you can access with the HTTP protocol. Also known as public APIs, they have defined API endpoints and request and response formats.

**Private API**

Private APIs remain hidden from external users. These private APIs aren't available for users outside of the company and are instead intended to improve productivity and communication across different internal development teams.

**Partner API**

Partner APIs connect strategic business partners. Typically, developers access these APIs in self-service mode through a public API developer portal. Still, they need to complete an onboarding process and get login credentials to access partner APIs.

**Composite API**

Composite APIs combine multiple data or service APIs. They allow programmers to access several endpoints in a single call. Composite APIs are useful in microservices architecture where performing a single task may require information from several sources.

## Conclusion

API is nothing a mechanism for two application to communicate with certain set of information.

Because APIs allow companies to open access to their resources while maintaining security and control, they have become a valuable aspect of modern business and personal projects. It is important to understand API.

Interesting in connecting on X? Say me Hi at [@JitendraC](https://twitter.com/JiitendraC)
