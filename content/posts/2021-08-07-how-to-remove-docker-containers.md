---
title: How to remove docker container(s)
author: mohit
type: post
date: 2021-08-07T14:43:15+00:00
draft: true
url: /?p=2396
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
  - containers
  - docker

---
<p class="md-end-block md-p md-focus">
  <span class="md-plain md-expand">There are multiple ways that you can use to remove the containers. </span><span class="md-plain">The easiest way to remove the container is using the </span><span class="md-meta-i-c md-link"><a href="https://docs.docker.com/engine/reference/commandline/container_rm/"><span class="md-plain">docker rm command</span></a></span><span class="md-plain">.</span>
</p>

&nbsp;

### To stop a single container

&nbsp;

`docker rm container_id_or_name`

The _rm_ command has following options

<table>
  <tr>
    <td>
      Name, shorthand
    </td>
    
    <td>
      Default
    </td>
    
    <td>
      Description
    </td>
  </tr>
  
  <tr>
    <td>
      <code class="highlighter-rouge">--force</code> , <code class="highlighter-rouge">-f</code>
    </td>
    
    <td>
    </td>
    
    <td>
      Force the removal of a running container (uses SIGKILL)
    </td>
  </tr>
  
  <tr>
    <td>
      <code class="highlighter-rouge">--link</code> , <code class="highlighter-rouge">-l</code>
    </td>
    
    <td>
    </td>
    
    <td>
      Remove the specified link
    </td>
  </tr>
  
  <tr>
    <td>
      <code class="highlighter-rouge">--volumes</code> , <code class="highlighter-rouge">-v</code>
    </td>
    
    <td>
    </td>
    
    <td>
      Remove anonymous volumes associated with the container
    </td>
  </tr>
</table>

Now you can use the command to stop one container, example. When the command will be successfully executed, it will provide the id or name as the output.

&nbsp;

#####  You can provide the container ID as the argument for the rm command

<code class="EnlighterJSRAW" data-enlighter-language="generic">docker rm container_id</code>

&nbsp;

Example:

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~$ docker rm 4013041080cd
4013041080cd</pre>

#####  You can provide the container Name as the argument for the rm command

&nbsp;

`<code class="EnlighterJSRAW" data-enlighter-language="generic">docker rm container_name`</code>

Example :``

``

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~$ docker rm affectionate_engelbart
affectionate_engelbart</pre>

&nbsp;

#### To remove all the stopped containers

&nbsp;

You can use the option prune to remove all the stopped containers.

Example:

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~$ docker container prune
WARNING! This will remove all stopped containers.
Are you sure you want to continue? [y/N] y
Deleted Containers:
96b8fcc01f3e71b29b0a60821a4044aee691cee604cd793a1a74e9ddd1a3f2d3
b48b537bb1db9096391b6c55a5fbc0f89bc227b946753852fc7694af00625eaf
60fd9a785cda32d4228e6378c37881ac988f0728de19edc7a085d0ff83ff5f22

Total reclaimed space: 197B</pre>

&nbsp;

#### To remove all the containers (even the active one)

&nbsp;

&nbsp;