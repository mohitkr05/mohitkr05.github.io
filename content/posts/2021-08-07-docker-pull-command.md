---
title: Docker Pull command
author: mohit
type: post
date: 2021-08-07T10:09:48+00:00
draft: true
url: /?p=2407
featured_image: http://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-15_33_05-Httpd-Official-Image-_-Docker-Hub-—-Mozilla-Firefox.png
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
  - pull command

---
To use an image, either you can have it located in the docker host, or you need to fetch the image from a [docker registry .][1] <a href="https://hub.docker.com/" target="_blank" rel="noreferrer noopener">Dockerhub</a> is the Docker’s offical registry , from where you can fetch multiple community images. There are tons of official and vendor-specific pre-built images in Dockerhub such as Ubuntu, Python, CentOs, Nginx, Apache, Java, NodeJs, etc.

You can browse the docker hub repository for the required image.

&nbsp;

<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2414" src="http://54.206.253.95/wp-content/uploads/2021/08/2021-08-07-15_33_05-Httpd-Official-Image-_-Docker-Hub-—-Mozilla-Firefox.png" alt="docker registry search" width="1440" height="467" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-15_33_05-Httpd-Official-Image-_-Docker-Hub-—-Mozilla-Firefox.png 1440w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-15_33_05-Httpd-Official-Image-_-Docker-Hub-—-Mozilla-Firefox-300x97.png 300w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-15_33_05-Httpd-Official-Image-_-Docker-Hub-—-Mozilla-Firefox-1024x332.png 1024w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-15_33_05-Httpd-Official-Image-_-Docker-Hub-—-Mozilla-Firefox-768x249.png 768w" sizes="(max-width: 1440px) 100vw, 1440px" /> 

&nbsp;

The other option is to look for the image using the docker search command.

``

<pre class="EnlighterJSRAW" data-enlighter-language="generic">docker search &lt;image&gt;</pre>

``

&nbsp;

``

Example:

```<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2415" src="http://54.206.253.95/wp-content/uploads/2021/08/2021-08-07-15_35_11-aws-1.png" alt="" width="1032" height="422" />`

&nbsp;

The pull command has following options

``

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~$ docker pull --help

Usage: docker pull [OPTIONS] NAME[:TAG|@DIGEST]

Pull an image or a repository from a registry

Options:
-a, --all-tags Download all tagged images in the repository
--disable-content-trust Skip image verification (default true)
--platform string Set platform if server is multi-platform capable
-q, --quiet Suppress verbose output</pre>

``

&nbsp;

``

&nbsp;

To pull the image, you can use the pull command, the syntax is

``

<pre class="EnlighterJSRAW" data-enlighter-language="generic">docker pull &lt;image:tag&gt;</pre>

``

&nbsp;

``

`Example:`

 `<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2416" src="http://54.206.253.95/wp-content/uploads/2021/08/2021-08-07-15_35_34-aws-1.png" alt="" width="712" height="154" /><br />
` 

&nbsp;

Now you can check the images in your docker host.

<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2417" src="http://54.206.253.95/wp-content/uploads/2021/08/2021-08-07-15_38_42-aws-1.png" alt="" width="547" height="92" /> 

&nbsp;

Please share your thoughts, about the docker pull command.

&nbsp;

&nbsp;

 [1]: https://dailytechlearning.com/cloud-computing/docker/docker-registry