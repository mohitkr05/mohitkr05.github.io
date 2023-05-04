---
title: Docker Images command
author: mohit
type: post
date: 2021-08-07T10:53:58+00:00
draft: true
url: /?p=2423
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
  - docker-images

---
Docker Images are built using multiple file layers that are all read-only. Each instruction that we specify inside a Dockerfile creates a separate image layer on top of the previous ones. The image layers contains all the code, libraries, dependencies, binaries, and configuration files that are specific to the container environment that we want to create for our application.

You can check the docker images with the docker images command.

<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2424" src="http://54.206.253.95/wp-content/uploads/2021/08/2021-08-07-15_52_43-aws-1.png" alt="" width="623" height="98" /> 

The display format contains the repository, tage, image Id , time created and size.

The docker images command has following options

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~$ docker images --help

Usage:  docker images [OPTIONS] [REPOSITORY[:TAG]]

List images

Options:
  -a, --all             Show all images (default hides intermediate images)
      --digests         Show digests
  -f, --filter filter   Filter output based on conditions provided
      --format string   Pretty-print images using a Go template
      --no-trunc        Don't truncate output
  -q, --quiet           Only show image IDs
</pre>

You can check the SHA-256 digest for the integrity verification purpose as well, using the &#8211;digests option

<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2426" src="http://54.206.253.95/wp-content/uploads/2021/08/2021-08-07-16_14_23-aws-1.png" alt="" width="1140" height="101" /> 

&nbsp;

Also, you can check all the tag available for a particular docker image by using the command

<code class="EnlighterJSRAW" data-enlighter-language="generic">docker image &lt;image-name&gt;</code>

<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2427" src="http://54.206.253.95/wp-content/uploads/2021/08/2021-08-07-16_19_28-aws-1.png" alt="" width="632" height="70" /> 

&nbsp;