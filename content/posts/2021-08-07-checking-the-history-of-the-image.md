---
title: Checking the history of the image
author: mohit
type: post
date: 2021-08-07T11:09:50+00:00
draft: true
url: /?p=2433
categories:
  - Docker
tags:
  - docker
  - image history

---
You can use the image history command to check the history of the image

&nbsp;

<pre class="highlight"><code>&lt;code class="EnlighterJSRAW" data-enlighter-language="generic">docker image history [OPTIONS] IMAGE</code>&lt;/code></pre>

This is an example of the history of the [httpd][1] image.

<pre class="EnlighterJSRAW" data-enlighter-language="generic">IMAGE          CREATED        CREATED BY                                      SIZE      COMMENT
bde40dcb22a7   34 hours ago   /bin/sh -c #(nop)  CMD ["httpd-foreground"]     0B
&lt;missing&gt;      34 hours ago   /bin/sh -c #(nop)  EXPOSE 80                    0B
&lt;missing&gt;      34 hours ago   /bin/sh -c #(nop) COPY file:c432ff61c4993ecd…   138B
&lt;missing&gt;      34 hours ago   /bin/sh -c #(nop)  STOPSIGNAL SIGWINCH          0B
&lt;missing&gt;      34 hours ago   /bin/sh -c set -eux;   savedAptMark="$(apt-m…   61.2MB
&lt;missing&gt;      2 weeks ago    /bin/sh -c #(nop)  ENV HTTPD_PATCHES=           0B
&lt;missing&gt;      2 weeks ago    /bin/sh -c #(nop)  ENV HTTPD_SHA256=1bc826e7…   0B
&lt;missing&gt;      2 weeks ago    /bin/sh -c #(nop)  ENV HTTPD_VERSION=2.4.48     0B
&lt;missing&gt;      2 weeks ago    /bin/sh -c set -eux;  apt-get update;  apt-g…   7.38MB
&lt;missing&gt;      2 weeks ago    /bin/sh -c #(nop) WORKDIR /usr/local/apache2    0B
&lt;missing&gt;      2 weeks ago    /bin/sh -c mkdir -p "$HTTPD_PREFIX"  && chow…   0B
&lt;missing&gt;      2 weeks ago    /bin/sh -c #(nop)  ENV PATH=/usr/local/apach…   0B
&lt;missing&gt;      2 weeks ago    /bin/sh -c #(nop)  ENV HTTPD_PREFIX=/usr/loc…   0B
&lt;missing&gt;      2 weeks ago    /bin/sh -c #(nop)  CMD ["bash"]                 0B
&lt;missing&gt;      2 weeks ago    /bin/sh -c #(nop) ADD file:45f5dfa135c848a34…   69.3MB
</pre>

This is the example of the [WordPress][2] image.

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~/config$ docker image history wordpress:latest
IMAGE          CREATED       CREATED BY                                      SIZE      COMMENT
baf5889057ff   8 days ago    /bin/sh -c #(nop)  CMD ["apache2-foreground"]   0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  ENTRYPOINT ["docker-entry…   0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) COPY file:5be6bcc31206cb82…   3.37kB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) COPY --chown=www-data:www-…   5.46kB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  VOLUME [/var/www/html]       0B
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;  version='5.8';  sha1='…   52.8MB
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;  a2enmod rewrite expire…   51.2kB
&lt;missing&gt;      8 days ago    /bin/sh -c {   echo 'error_reporting = E_ERR…   331B
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;  docker-php-ext-enable …   173B
&lt;missing&gt;      8 days ago    /bin/sh -c set -ex;   savedAptMark="$(apt-ma…   36.6MB
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;  apt-get update;  apt-g…   46.9MB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  CMD ["apache2-foreground"]   0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  EXPOSE 80                    0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) WORKDIR /var/www/html         0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) COPY file:e3123fcb6566efa9…   1.35kB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  STOPSIGNAL SIGWINCH          0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  ENTRYPOINT ["docker-php-e…   0B
&lt;missing&gt;      8 days ago    /bin/sh -c docker-php-ext-enable sodium         17B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) COPY multi:e4407f0002276f0…   6.76kB
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;   savedAptMark="$(apt-m…   60.3MB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) COPY file:ce57c04b70896f77…   587B
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;   savedAptMark="$(apt-m…   11.6MB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  ENV PHP_SHA256=8e078cd7d2…   0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  ENV PHP_URL=https://www.p…   0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  ENV PHP_VERSION=7.4.22       0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV GPG_KEYS=42670A7FE4D0…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_LDFLAGS=-Wl,-O1 -…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_CPPFLAGS=-fstack-…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_CFLAGS=-fstack-pr…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_EXTRA_CONFIGURE_A…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_EXTRA_BUILD_DEPS=…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c {   echo '&lt;FilesMatch \.php$&gt;';  …   237B
&lt;missing&gt;      2 weeks ago   /bin/sh -c a2dismod mpm_event && a2enmod mpm…   68B
&lt;missing&gt;      2 weeks ago   /bin/sh -c set -eux;  apt-get update;  apt-g…   45.9MB
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV APACHE_ENVVARS=/etc/a…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV APACHE_CONFDIR=/etc/a…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c set -eux;  mkdir -p "$PHP_INI_DIR…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_INI_DIR=/usr/loca…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c set -eux;  apt-get update;  apt-g…   227MB
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHPIZE_DEPS=autoconf …   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c set -eux;  {   echo 'Package: php…   46B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  CMD ["bash"]                 0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop) ADD file:45f5dfa135c848a34…   69.3MB
</pre>

&nbsp;

You can also supply option &#8220;-H&#8221; to check for the human readable size of the image.

&nbsp;

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~/config$ docker image history wordpress:latest -H
IMAGE          CREATED       CREATED BY                                      SIZE      COMMENT
baf5889057ff   8 days ago    /bin/sh -c #(nop)  CMD ["apache2-foreground"]   0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  ENTRYPOINT ["docker-entry…   0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) COPY file:5be6bcc31206cb82…   3.37kB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) COPY --chown=www-data:www-…   5.46kB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  VOLUME [/var/www/html]       0B
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;  version='5.8';  sha1='…   52.8MB
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;  a2enmod rewrite expire…   51.2kB
&lt;missing&gt;      8 days ago    /bin/sh -c {   echo 'error_reporting = E_ERR…   331B
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;  docker-php-ext-enable …   173B
&lt;missing&gt;      8 days ago    /bin/sh -c set -ex;   savedAptMark="$(apt-ma…   36.6MB
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;  apt-get update;  apt-g…   46.9MB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  CMD ["apache2-foreground"]   0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  EXPOSE 80                    0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) WORKDIR /var/www/html         0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) COPY file:e3123fcb6566efa9…   1.35kB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  STOPSIGNAL SIGWINCH          0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  ENTRYPOINT ["docker-php-e…   0B
&lt;missing&gt;      8 days ago    /bin/sh -c docker-php-ext-enable sodium         17B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) COPY multi:e4407f0002276f0…   6.76kB
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;   savedAptMark="$(apt-m…   60.3MB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop) COPY file:ce57c04b70896f77…   587B
&lt;missing&gt;      8 days ago    /bin/sh -c set -eux;   savedAptMark="$(apt-m…   11.6MB
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  ENV PHP_SHA256=8e078cd7d2…   0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  ENV PHP_URL=https://www.p…   0B
&lt;missing&gt;      8 days ago    /bin/sh -c #(nop)  ENV PHP_VERSION=7.4.22       0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV GPG_KEYS=42670A7FE4D0…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_LDFLAGS=-Wl,-O1 -…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_CPPFLAGS=-fstack-…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_CFLAGS=-fstack-pr…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_EXTRA_CONFIGURE_A…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_EXTRA_BUILD_DEPS=…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c {   echo '&lt;FilesMatch \.php$&gt;';  …   237B
&lt;missing&gt;      2 weeks ago   /bin/sh -c a2dismod mpm_event && a2enmod mpm…   68B
&lt;missing&gt;      2 weeks ago   /bin/sh -c set -eux;  apt-get update;  apt-g…   45.9MB
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV APACHE_ENVVARS=/etc/a…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV APACHE_CONFDIR=/etc/a…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c set -eux;  mkdir -p "$PHP_INI_DIR…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHP_INI_DIR=/usr/loca…   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c set -eux;  apt-get update;  apt-g…   227MB
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  ENV PHPIZE_DEPS=autoconf …   0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c set -eux;  {   echo 'Package: php…   46B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop)  CMD ["bash"]                 0B
&lt;missing&gt;      2 weeks ago   /bin/sh -c #(nop) ADD file:45f5dfa135c848a34…   69.3MB
</pre>

&nbsp;

 [1]: https://hub.docker.com/_/httpd
 [2]: https://hub.docker.com/_/wordpress