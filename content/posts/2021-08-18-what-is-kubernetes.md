---
title: What is Kubernetes?
author: mohit
type: post
date: 2021-08-18T05:11:25+00:00
draft: true
url: /?p=2538
categories:
  - Kubernetes
tags:
  - kubernetes

---
As per the definition from the official website [Kubernetes][1] is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation. It has a large, rapidly growing ecosystem. Kubernetes services, support, and tools are widely available.

Simply to state Kubernetes is the management and orchestration engines for containers.

Kubernetes play a key role, in ensuring that there is no downtime.As containers are isolated environment, they cannot work in cluster to provide high availability thus this role is performed by Kubernetes which for example if container goes down, can deploy another container Kubernetes provides a framework to run distributed systems resiliently and takes care of scaling and failover of application.

As per the Kubernetes website, Kubernetes provides you with:

  * **Service discovery and load balancing** Kubernetes can expose a container using the DNS name or using their own IP address. If traffic to a container is high, Kubernetes is able to load balance and distribute the network traffic so that the deployment is stable.
  * **Storage orchestration** Kubernetes allows you to automatically mount a storage system of your choice, such as local storages, public cloud providers, and more.
  * **Automated rollouts and rollbacks** You can describe the desired state for your deployed containers using Kubernetes, and it can change the actual state to the desired state at a controlled rate. For example, you can automate Kubernetes to create new containers for your deployment, remove existing containers and adopt all their resources to the new container.
  * **Automatic bin packing** You provide Kubernetes with a cluster of nodes that it can use to run containerized tasks. You tell Kubernetes how much CPU and memory (RAM) each container needs. Kubernetes can fit containers onto your nodes to make the best use of your resources.
  * **Self-healing** Kubernetes restarts containers that fail, replaces containers, kills containers that don&#8217;t respond to your user-defined health check, and doesn&#8217;t advertise them to clients until they are ready to serve.
  * **Secret and configuration management** Kubernetes lets you store and manage sensitive information, such as passwords, OAuth tokens, and SSH keys. You can deploy and update secrets and application configuration without rebuilding your container images, and without exposing secrets in your stack configuration.

&nbsp;

 [1]: https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/