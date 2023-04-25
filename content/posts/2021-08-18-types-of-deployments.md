---
title: Types of Deployments
author: mohit
type: post
date: 2021-08-18T05:17:33+00:00
draft: true
url: /?p=2540
categories:
  - Containers
  - Virtualization
tags:
  - containers
  - docker
  - virtualization

---
**Traditional deployment :** Traditional deployment is the case where the applications are installed over a physical system. Applications is able to utilize all the system resources, however this may lead to resource allocation issues in case of multiple application environment. To counter this, we may use individual applications in their own physical server, but this is not cost effective.

**Virtualized deployment : **A solution where we can use a physical servers to run multiple Virtual Machines (VMs) on a single physical server&#8217;s CPU.  We logically separate the physical resources for each application into its own system. VMs provide better utilization and isolation of resources. Virtualization allows better utilization of resources in a physical server and allows better scalability because an application can be added or updated easily, reduces hardware costs, and much more.

**Container deployment :** Lightweight containers are similar to VMs as they use a concept of Namespace in order to deploy applications.A container has its own filesystem, however it shares the CPU, memory, process space, and more.