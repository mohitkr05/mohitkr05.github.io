---
title: Types of Docker Images
author: mohit
type: post
date: 2021-08-10T07:32:03+00:00
draft: true
url: /?p=2497
featured_image: http://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-10-12_59_15-Window.png
categories:
  - Docker
tags:
  - docker-images
  - types of images

---
The docker images can be classified into two categories

&nbsp;

  * **Ready to use or Application Images**
  * **Base Images**

<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2498" src="http://54.206.253.95/wp-content/uploads/2021/08/2021-08-10-12_59_15-Window.png" alt="types of docker images" width="507" height="472" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-10-12_59_15-Window.png 507w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-10-12_59_15-Window-300x279.png 300w" sizes="(max-width: 507px) 100vw, 507px" /> 

**Ready to use Images :** Application images can be considered as ready to use images and they are either maintained by the docker hub, or the community. These images work on some base image or Parent image. A Parent image is the image on which your image is based on. It refers to the contents of the <code class="highlighter-rouge">FROM</code> instruction in the Dockerfile.

As you can see in the below example, the ready to use image is created with a _FROM_ instruction using the parent debian image.

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

&nbsp;

**Base Images :** The images which emulate the operating system are termed as base images.

Base image, can be created from the Docker’s reserved, minimal image, <code class="highlighter-rouge">scratch</code>, as a starting point for building containers.

Using the <code class="highlighter-rouge">scratch</code> “image” signals to the build process that you want the next command in the <code class="highlighter-rouge">Dockerfile</code> to be the first filesystem layer in your image.

<pre class="EnlighterJSRAW" data-enlighter-language="generic"># syntax=docker/dockerfile:1
FROM scratch
ADD hello /
CMD ["/hello"]
</pre>

&nbsp;

[Reference][1]

 [1]: https://docs.docker.com/develop/develop-images/baseimages/