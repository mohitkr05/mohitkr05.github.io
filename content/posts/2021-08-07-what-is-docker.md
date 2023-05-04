---
title: What is Docker?
author: mohit
type: post
date: 2021-08-07T09:34:01+00:00
draft: true
url: /?p=2399
site-sidebar-layout:
  - default
  - default
site-content-layout:
  - default
  - default
theme-transparent-header-meta:
  - default
  - default
categories:
  - Docker
tags:
  - docker
  - docker architecture
  - docker introduction

---
Docker has multiple meanings. Docker is the name of the company called **Docker, Inc **which is an American technology company that develops productivity tools built around Docker, an open source project that automates the deployment of code inside [software containers][1]. Docker is one of the most popular containerization platforms available in the market today. It was developed by Solomon Hykes. Docker software has multiple options , however the software that hosts the containers is called **Docker Engine**.

Docker provides the ability to package and run an application in a loosely isolated environment called a container and thus it helps in the separation of the applications from your infrastructure and thus software can be delivered quickly. Docker helps in implementing CI/CD pipelines and this can significantly reduce the delay between writing code and running it in production.

Docker has become one of the most popular container-management platforms.  The advantage of using docker over a virtual machine is that the overhead layer of the kernel and operating system is removed and a true micro service architecture can be achieved. You can read more about the [differences between a Container and Virtual Machine][2] here.

&nbsp;

&nbsp;

<figure style="width: 1009px" class="wp-caption aligncenter"><img decoding="async" loading="lazy" src="https://docs.docker.com/engine/images/architecture.svg" alt="Docker Architecture Diagram | Image Source - Docker Docs" width="1009" height="527" /><figcaption class="wp-caption-text">Docker Architecture Diagram | Image Source &#8211; Docker Docs [https://docs.docker.com/get-started/overview/]</figcaption></figure>Docker is implemented using a client server architecture. The client talks to the daemon. Daemon takes care of all the functions related to docker. Docker client can be executed in the same system or in remote system.  The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface. The third component of the Docker architecture is the Docker Registry which hosts the Docker Images.

 [1]: https://dailytechlearning.com/cloud-computing/containers/what-are-containers/
 [2]: https://dailytechlearning.com/?p=2466&preview=true