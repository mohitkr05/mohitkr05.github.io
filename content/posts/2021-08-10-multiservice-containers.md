---
title: Multiservice containers
author: mohit
type: post
date: 2021-08-10T08:00:04+00:00
draft: true
url: /?p=2506
categories:
  - Containers
tags:
  - multi-service containers
  - system-d

---
Containers are build with the idea of microservices such that there is only one service in a container however, to cater to industry demand, where some organization want to run multiple services in a container can be achieved by running systemd into the container.Many organization want to take existing multi-service applications out of Virtual Machines and run them inside of containers, without changing the architecture of the application,  So running them as services launched out of unit files by systemd is one of the option.