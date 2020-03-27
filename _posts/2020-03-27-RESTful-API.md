---
layout: post
title: What is RESTful API design
date: 2020-03-27 16:42:20 +0800
description: Some basic understandings about what is RESTful API and what's the design principal
img: RESTful.png # Add image post (optional)
tags: [Blog, Study]
author: Aquariusx
---
# RESTful API

>In my daily engineering life, I often heard people say we should make our APIs more RESTful. However, only few of them know what RESTful really means. So I search the internet and found some good posts about how to understand it. Copy their brief ideas here and may it helpful to someone or myself in the future.

## What is it

### REpresentational State Transfer

It means when a RESTful API is called, the server will transfer to the client a representation of the state of the requested resource.

### coined by Roy Fielding in 2000

### architecture style for designing loosely coupled applications over HTTP

## Principals

### Uniform Interface

Each request to server must contain an uri to a resource and enough information for server to process the request.
The server's response must contain enough information for the client to understand the resource.
Different clients look the same, whether the client is a chrome browser, a linux server, a python script, an android app or anything else.

### client - server seperation

The client and the server act independently, each on its own, and the interaction between them is only in the form of requests, initiated by the client only, and responses, which the server send to the client only as a reaction to a request.

### stateless

Stateless means the server does not remember anything about the user who uses the API.
Each individual request contains all the information the server needs to perform the request and return a response.

### layered system

Between the client who requests a representation of a resource’s state, and the server who sends the response back, there might be a number of servers in the middle. These servers might provide a security layer, a caching layer, a load-balancing layer, or other functionality. Those layers should not affect the request or the response. The client is agnostic as to how many layers, if any, there are between the client and the actual server responding to the request.

### cacheable

In REST, caching shall be applied to resources when applicable, and then these resources MUST declare themselves cacheable. Caching can be implemented on the server or client-side.

## Key Concepts

### client

- the person or software who uses the API. It can be a developer

### resource

- any object the API can provide information about