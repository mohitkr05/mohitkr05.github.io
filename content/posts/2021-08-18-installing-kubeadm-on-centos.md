---
title: Installing Kubeadm on Centos
author: mohit
type: post
date: 2021-08-18T06:01:32+00:00
draft: true
url: /?p=2546
categories:
  - Kubernetes
tags:
  - kubernetes

---
<img decoding="async" loading="lazy" class="alignnone size-large wp-image-2548" src="http://54.206.253.95/wp-content/uploads/2021/08/Kubeadm_sethostname.png" alt="" width="587" height="141" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/Kubeadm_sethostname.png 587w, https://www.mohitkr.com/wp-content/uploads/2021/08/Kubeadm_sethostname-300x72.png 300w" sizes="(max-width: 587px) 100vw, 587px" />

&nbsp;

#### Disable SELINUX

&nbsp;

To disable SELINUX, you can use the following two options

&nbsp;

Firstly, you can set the parameter setenforce to zero

<code class="EnlighterJSRAW" data-enlighter-language="generic">setenforce 0&lt;br />
</code>

&nbsp;

Or you can permanently edit the  /etc/sysconfig/selinux file

<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2547" src="http://54.206.253.95/wp-content/uploads/2021/08/disable_selinux.png" alt="" width="971" height="213" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/disable_selinux.png 971w, https://www.mohitkr.com/wp-content/uploads/2021/08/disable_selinux-300x66.png 300w, https://www.mohitkr.com/wp-content/uploads/2021/08/disable_selinux-768x168.png 768w" sizes="(max-width: 971px) 100vw, 971px" /> 

&nbsp;

#### Install Docker