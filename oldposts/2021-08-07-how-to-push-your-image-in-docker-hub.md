---
title: How to Push your image in docker hub
author: mohit
type: post
date: 2021-08-07T12:01:02+00:00
draft: true
url: /?p=2438
featured_image: http://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_37_22-Image-Layer-Details-dailytechlearning_apache_2.4-sha256_fe53c98ab2f5777f50b0.png
categories:
  - Docker
tags:
  - docker
  - docker-hub

---
In this tutorial, I will show you, how you can upload your image directly to the docker hub. To use the services of docker hub, first you need to [create an account][1].

Use the command _docker login_ to login to the docker hub.

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~/config$ docker login
Login with your Docker ID to push and pull images from Docker Hub. If you don't have a Docker ID, head over to https://hub.docker.com to create one.
Username: &lt;username&gt;
Password:
WARNING! Your password will be stored unencrypted in /home/ubuntu/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded</pre>

Now you have to tag your image with the repository name that you have.

<code class="EnlighterJSRAW" data-enlighter-language="generic">docker tag apacheimage:latest dailytechlearning/apache:2.4</code>

&nbsp;

After the tagging is done you can push to the repository

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~/config$ docker push dailytechlearning/apache:2.4
The push refers to repository [docker.io/dailytechlearning/apache]
e6fdc4f3005d: Pushed
afa3e488a0ee: Mounted from library/debian
2.4: digest: sha256:fe53c98ab2f5777f50b07dd4139401427f5bf8a630b9ce204ae58ed68d1c9fca size: 741
</pre>

The image will be publicly available and you can see it online on the docker hub

&nbsp;

<img decoding="async" loading="lazy" class="alignnone size-large wp-image-2440" src="https://dailytechlearning.com/wp-content/uploads/2021/08/2021-08-07-17_31_22-dailytechlearning_apache-Tags-_-Docker-Hub-—-Mozilla-Firefox-1024x237.png" alt="" width="1024" height="237" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_31_22-dailytechlearning_apache-Tags-_-Docker-Hub-—-Mozilla-Firefox-1024x237.png 1024w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_31_22-dailytechlearning_apache-Tags-_-Docker-Hub-—-Mozilla-Firefox-300x69.png 300w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_31_22-dailytechlearning_apache-Tags-_-Docker-Hub-—-Mozilla-Firefox-768x177.png 768w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_31_22-dailytechlearning_apache-Tags-_-Docker-Hub-—-Mozilla-Firefox.png 1342w" sizes="(max-width: 1024px) 100vw, 1024px" /> 

You can see the details of the image as well online.

&nbsp;

<img decoding="async" loading="lazy" class="alignnone size-large wp-image-2450" src="https://dailytechlearning.com/wp-content/uploads/2021/08/2021-08-07-17_37_22-Image-Layer-Details-dailytechlearning_apache_2.4-sha256_fe53c98ab2f5777f50b0-1024x432.png" alt="" width="1024" height="432" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_37_22-Image-Layer-Details-dailytechlearning_apache_2.4-sha256_fe53c98ab2f5777f50b0-1024x432.png 1024w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_37_22-Image-Layer-Details-dailytechlearning_apache_2.4-sha256_fe53c98ab2f5777f50b0-300x127.png 300w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_37_22-Image-Layer-Details-dailytechlearning_apache_2.4-sha256_fe53c98ab2f5777f50b0-768x324.png 768w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-07-17_37_22-Image-Layer-Details-dailytechlearning_apache_2.4-sha256_fe53c98ab2f5777f50b0.png 1447w" sizes="(max-width: 1024px) 100vw, 1024px" /> 

&nbsp;

 [1]: https://dailytechlearning.com/cloud-computing/docker/how-to-create-an-account-on-docker-hub/