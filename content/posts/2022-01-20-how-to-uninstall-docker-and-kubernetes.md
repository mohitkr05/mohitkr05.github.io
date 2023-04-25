---
title: How to uninstall Docker and Kubernetes
author: mohit
type: post
date: 2022-01-20T04:47:00+00:00
draft: true
url: /?p=2568
categories:
  - Containers
  - Docker
  - Kubernetes
tags:
  - docker
  - kubernetes
  - uninstall

---
## Uninstall Docker from Ubuntu

Execute the below commands to completely uninstall Docker from Ubuntu

<pre><code class="language-bash">sudo apt-get purge -y docker-engine docker docker.io docker-ce docker-ce-cli
sudo apt-get autoremove -y --purge docker-engine docker docker.io docker-ce  
sudo rm -rf /var/lib/docker /etc/docker
sudo rm /etc/apparmor.d/docker
sudo rm -rf /var/run/docker.sock</code></pre>

## Uninstall Docker from CentOS/Redhat

<pre><code class="language-bash">sudo yum remove docker-engine docker docker.io docker-ce docker-ce-cli
sudo rm -rf /var/lib/docker /etc/docker</code></pre>

## Uninstall Kubernetes from Ubuntu

<pre><code class="language-bash">kubeadm reset
sudo apt-get purge kubeadm kubectl kubelet kubernetes-cni kube* 
sudo apt-get autoremove
sudo rm -rf ~/.kube</code></pre>

## Uninstall Kubernetes from CentOS

<pre><code class="language-bash">kubeadm reset
sudo yum remove kubeadm kubectl kubelet kubernetes-cni kube*
sudo yum autoremove
sudo rm -rf ~/.kube</code></pre>