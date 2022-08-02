---
title: "BFF (Back-End For Front-End)"
date: 2022-08-01T23:44:56+10:00
tags: ["System Design"]
categories: ["Technology"]
---

#### **The issues of traditional "direct point to point approach"**

- Updating microservices will cause code change in front-end application and further cause new front-end application need to be deployed.
- Data from microservices may not be formatted, which causes additonal data transformer in front-end. You also have to orchestrate many API calls. They will make your front-end application increasingly complex and difficult to maintain.
- Huge number of calls you make in a point to point application may hurt the performance.

#### **How BFF works**

BFF is an API sittnig between front-end application and back-end microservices APIs. In this case...

1. The front-end will just make a single call to the BFF.
2. The BFF calls relevant microservices.
3. The BFF format the responses.
4. The BFF returns nicely formatted data back to the front-end.

#### **The benefits of BFF**

- Keep front-ends simple and light so it's easier to maintain.
- BFF can hide sensitive information from microservices.
