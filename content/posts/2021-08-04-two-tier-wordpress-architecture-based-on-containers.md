---
title: Two-Tier WordPress architecture based on Containers
author: mohit
type: post
date: 2021-08-04T09:53:44+00:00
draft: true
url: /?p=2390
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
  - Cloud Computing
  - WordPress

---
<p class="graf graf--p">
  This is a beginners level exercise for hosting a two-tier architecture on Docker Containers. WordPress is a monolithic application which was designed to work on shared servers, however to utilize the advantages of micro services, we need to segregate the data layer and the processing layer.
</p>

<p class="graf graf--p">
  The first split is to split the database and the web application handled by WordPress. The architecture that we are going to deploy is as follows
</p><figure class="graf graf--figure">

<img decoding="async" class="graf-image" src="https://cdn-images-1.medium.com/max/800/1*OkW9CNab5pe8q5HZLz6cDw.png" data-image-id="1*OkW9CNab5pe8q5HZLz6cDw.png" data-width="841" data-height="301" /> <figcaption class="imageCaption">Two tier WordPress architecture based on Docker Containers</figcaption></figure> 

<p class="graf graf--p">
  To deploy this architecture, we are going to use the following Docker community images.
</p>

<p class="graf graf--p">
  <a class="markup--anchor markup--p-anchor" href="https://hub.docker.com/_/mysql/" target="_blank" rel="noopener" data-href="https://hub.docker.com/_/mysql/">Mysql — Official Image | Docker Hub</a>
</p>

<p class="graf graf--p">
  <a class="markup--anchor markup--p-anchor" href="https://hub.docker.com/_/wordpress/" target="_blank" rel="noopener" data-href="https://hub.docker.com/_/wordpress/">WordPress — Official Image | Docker Hub</a>
</p>

<p class="graf graf--p">
  First of all, we can search the images, using the <em class="markup--em markup--p-em">docker search</em> command.
</p><figure class="graf graf--figure">

<img decoding="async" class="graf-image" src="https://cdn-images-1.medium.com/max/800/1*KAfwMtJsItGwJ1UvI8Z6aw.png" alt="using docker search to look for mysql images" data-image-id="1*KAfwMtJsItGwJ1UvI8Z6aw.png" data-width="934" data-height="408" /> </figure> <figure class="graf graf--figure"><img decoding="async" class="graf-image" src="https://cdn-images-1.medium.com/max/800/1*TaUDIY9NO-G1dWPdlhOakA.png" alt="Using docker search to find wordpress image" data-image-id="1*TaUDIY9NO-G1dWPdlhOakA.png" data-width="979" data-height="402" /></figure> 

<p class="graf graf--p">
  Then we can pull the desired images using <em class="markup--em markup--p-em">docker pull</em>
</p>

<pre class="graf graf--h4"><em class="markup--em markup--h4-em">docker pull mysql</em></pre><figure class="graf graf--figure">

<img decoding="async" class="graf-image" src="https://cdn-images-1.medium.com/max/800/1*5jQ-88Q37l8PX3NcNOV-QQ.png" data-image-id="1*5jQ-88Q37l8PX3NcNOV-QQ.png" data-width="719" data-height="92" /> </figure> 

<pre class="graf graf--h4"><em class="markup--em markup--h4-em">docker pull wordpress</em></pre><figure class="graf graf--figure">

<img decoding="async" class="graf-image" src="https://cdn-images-1.medium.com/max/800/1*S1JKwURWZfVWsLlEpBkUUA.png" alt="docker pull wordpress" data-image-id="1*S1JKwURWZfVWsLlEpBkUUA.png" data-width="811" data-height="394" /> </figure> 

<p class="graf graf--p">
  The next step is to create a custom network
</p>

<pre class="graf graf--h4"><em class="markup--em markup--h4-em">docker network create — subnet 192.168.10.0/24 — driver bridge webapp</em></pre>

&nbsp;

&nbsp;<figure class="graf graf--figure">

<img decoding="async" class="graf-image" src="https://cdn-images-1.medium.com/max/800/1*7M13l4e9MniaxpgS4PT8wg.png" data-image-id="1*7M13l4e9MniaxpgS4PT8wg.png" data-width="774" data-height="38" /> </figure> 

#### The network can be verified in the <em class="markup--em markup--h4-em">ip addr</em> command as well. {.graf.graf--h4}<figure class="graf graf--figure">

<img decoding="async" class="graf-image" src="https://cdn-images-1.medium.com/max/800/1*xZOru2ukR-Rjl9dV3SDhgw.png" data-image-id="1*xZOru2ukR-Rjl9dV3SDhgw.png" data-width="900" data-height="316" /> <figcaption class="imageCaption">ip address will show the custom network created</figcaption></figure> 

<p class="graf graf--p">
  Now we have a custom network created, we can spin up our containers with the required configuration
</p>

<pre class="graf graf--h4"><em class="markup--em markup--h4-em">docker run -it — name wpdb_mysql — network webapp -e MYSQL_ROOT_PASSWORD=LHSWCVAbzS -d mysql:latest</em></pre><figure class="graf graf--figure">

<img decoding="async" class="graf-image" src="https://cdn-images-1.medium.com/max/800/1*7B579N04EsFVlOwxQTWzfw.png" alt="starting the mysql container" data-image-id="1*7B579N04EsFVlOwxQTWzfw.png" data-width="1008" data-height="95" /> </figure> 

<p class="graf graf--p">
  We are going to use a custom port 8081 to expose it to the world for our WordPress server. The other parameters include the configuration of mySql database server. Node that as we are using a custom bridged network, in the host, I have just provided the container name as it would be accessible by name as well.
</p>

<pre class="graf graf--h4">docker run — name wp — network webapp -p 8081:80 -e WORDPRESS_DB_HOST=wpdb_mysql -e WORDPRESS_DB_USER=root -e WORDPRESS_DB_PASSWORD=LHSWCVAbzS -e WORDPRESS_DB_NAME=wpdb -d wordpress</pre><figure class="graf graf--figure">

<img decoding="async" class="graf-image" src="https://cdn-images-1.medium.com/max/800/1*aTmV3205nTI_lqcOTodHIg.png" data-image-id="1*aTmV3205nTI_lqcOTodHIg.png" data-width="1640" data-height="125" /> </figure> 

<p class="graf graf--p">
  Now, you can access your freshly installed website on your favorite browser as well.
</p><figure class="graf graf--figure">

<img decoding="async" class="graf-image" src="https://cdn-images-1.medium.com/max/800/1*PGHKQ-4jQPSJtP15T7iTMw.png" data-image-id="1*PGHKQ-4jQPSJtP15T7iTMw.png" data-width="1864" data-height="952" /> </figure> 

<p class="graf graf--p">
  <strong class="markup--strong markup--p-strong">Conclusion</strong>
</p>

<p class="graf graf--p">
  In this tutorial, I just covered splitting up of the database and web application provided by WordPress using containers in a custom bridged network. Please provide your feedback for any scope of improvements.
</p>