---
title: Creating an Image using a Dockerfile
author: mohit
type: post
date: 2021-08-07T11:42:26+00:00
draft: true
url: /?p=2435
categories:
  - General

---
You can [build an image using a docker file][1].

In this tutorial we are going to create an image using the base debian image and install apache2 over it. This would be our apache2 image.

&nbsp;

<pre class="EnlighterJSRAW" data-enlighter-language="generic">FROM debian:latest

MAINTAINER dailytechlearning

RUN apt-get update && apt-get install -y apache2 && apt-get clean && rm -rf /var/lib/apt/lists/*

ENV APACHE_USER www-data
ENV APACHE_GRP  www-data
ENV APACHE_LOG /var/log/apache2


EXPOSE 80

CMD ["usr/bin/apache2", "-D", "FOREGROUND"]
</pre>

<img decoding="async" loading="lazy" class="alignnone wp-image-2436" src="https://dailytechlearning.com/wp-content/uploads/2021/08/2021-08-07-17_11_36-aws-300x199.png" alt="" width="595" height="395" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_11_36-aws-300x199.png 300w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_11_36-aws-1024x680.png 1024w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_11_36-aws-768x510.png 768w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_11_36-aws.png 1050w" sizes="(max-width: 595px) 100vw, 595px" />

 [1]: https://dailytechlearning.com/cloud-computing/docker/docker-build-command-usage/