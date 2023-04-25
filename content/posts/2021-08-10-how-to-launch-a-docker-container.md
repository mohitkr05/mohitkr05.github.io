---
title: How to launch a Docker container
author: mohit
type: post
date: 2021-08-10T11:12:32+00:00
draft: true
url: /?p=2510
site_layout:
  - full-width
  - full-width
categories:
  - Docker
tags:
  - docker container run

---
To launch a docker container you can use the _docker run_ command or _docker container run_

The docker run command has an extensive list of options.

<pre class="EnlighterJSRAW" data-enlighter-language="generic">Usage:  docker run [OPTIONS] IMAGE [COMMAND] [ARG...]

Run a command in a new container

Options:
      --add-host list                  Add a custom host-to-IP mapping (host:ip)
  -a, --attach list                    Attach to STDIN, STDOUT or STDERR
      --blkio-weight uint16            Block IO (relative weight), between 10 and 1000, or 0 to disable (default 0)
      --blkio-weight-device list       Block IO weight (relative device weight) (default [])
      --cap-add list                   Add Linux capabilities
      --cap-drop list                  Drop Linux capabilities
      --cgroup-parent string           Optional parent cgroup for the container
      --cgroupns string                Cgroup namespace to use (host|private)
                                       'host':    Run the container in the Docker host's cgroup namespace
                                       'private': Run the container in its own private cgroup namespace
                                       '':        Use the cgroup namespace as configured by the
                                                  default-cgroupns-mode option on the daemon (default)
      --cidfile string                 Write the container ID to the file
      --cpu-period int                 Limit CPU CFS (Completely Fair Scheduler) period
      --cpu-quota int                  Limit CPU CFS (Completely Fair Scheduler) quota
      --cpu-rt-period int              Limit CPU real-time period in microseconds
      --cpu-rt-runtime int             Limit CPU real-time runtime in microseconds
  -c, --cpu-shares int                 CPU shares (relative weight)
      --cpus decimal                   Number of CPUs
      --cpuset-cpus string             CPUs in which to allow execution (0-3, 0,1)
      --cpuset-mems string             MEMs in which to allow execution (0-3, 0,1)
  -d, --detach                         Run container in background and print container ID
      --detach-keys string             Override the key sequence for detaching a container
      --device list                    Add a host device to the container
      --device-cgroup-rule list        Add a rule to the cgroup allowed devices list
      --device-read-bps list           Limit read rate (bytes per second) from a device (default [])
      --device-read-iops list          Limit read rate (IO per second) from a device (default [])
      --device-write-bps list          Limit write rate (bytes per second) to a device (default [])
      --device-write-iops list         Limit write rate (IO per second) to a device (default [])
      --disable-content-trust          Skip image verification (default true)
      --dns list                       Set custom DNS servers
      --dns-option list                Set DNS options
      --dns-search list                Set custom DNS search domains
      --domainname string              Container NIS domain name
      --entrypoint string              Overwrite the default ENTRYPOINT of the image
  -e, --env list                       Set environment variables
      --env-file list                  Read in a file of environment variables
      --expose list                    Expose a port or a range of ports
      --gpus gpu-request               GPU devices to add to the container ('all' to pass all GPUs)
      --group-add list                 Add additional groups to join
      --health-cmd string              Command to run to check health
      --health-interval duration       Time between running the check (ms|s|m|h) (default 0s)
      --health-retries int             Consecutive failures needed to report unhealthy
      --health-start-period duration   Start period for the container to initialize before starting health-retries countdown (ms|s|m|h) (default 0s)
      --health-timeout duration        Maximum time to allow one check to run (ms|s|m|h) (default 0s)
      --help                           Print usage
  -h, --hostname string                Container host name
      --init                           Run an init inside the container that forwards signals and reaps processes
  -i, --interactive                    Keep STDIN open even if not attached
      --ip string                      IPv4 address (e.g., 172.30.100.104)
      --ip6 string                     IPv6 address (e.g., 2001:db8::33)
      --ipc string                     IPC mode to use
      --isolation string               Container isolation technology
      --kernel-memory bytes            Kernel memory limit
  -l, --label list                     Set meta data on a container
      --label-file list                Read in a line delimited file of labels
      --link list                      Add link to another container
      --link-local-ip list             Container IPv4/IPv6 link-local addresses
      --log-driver string              Logging driver for the container
      --log-opt list                   Log driver options
      --mac-address string             Container MAC address (e.g., 92:d0:c6:0a:29:33)
  -m, --memory bytes                   Memory limit
      --memory-reservation bytes       Memory soft limit
      --memory-swap bytes              Swap limit equal to memory plus swap: '-1' to enable unlimited swap
      --memory-swappiness int          Tune container memory swappiness (0 to 100) (default -1)
      --mount mount                    Attach a filesystem mount to the container
      --name string                    Assign a name to the container
      --network network                Connect a container to a network
      --network-alias list             Add network-scoped alias for the container
      --no-healthcheck                 Disable any container-specified HEALTHCHECK
      --oom-kill-disable               Disable OOM Killer
      --oom-score-adj int              Tune host's OOM preferences (-1000 to 1000)
      --pid string                     PID namespace to use
      --pids-limit int                 Tune container pids limit (set -1 for unlimited)
      --platform string                Set platform if server is multi-platform capable
      --privileged                     Give extended privileges to this container
  -p, --publish list                   Publish a container's port(s) to the host
  -P, --publish-all                    Publish all exposed ports to random ports
      --pull string                    Pull image before running ("always"|"missing"|"never") (default "missing")
      --read-only                      Mount the container's root filesystem as read only
      --restart string                 Restart policy to apply when a container exits (default "no")
      --rm                             Automatically remove the container when it exits
      --runtime string                 Runtime to use for this container
      --security-opt list              Security Options
      --shm-size bytes                 Size of /dev/shm
      --sig-proxy                      Proxy received signals to the process (default true)
      --stop-signal string             Signal to stop a container (default "SIGTERM")
      --stop-timeout int               Timeout (in seconds) to stop a container
      --storage-opt list               Storage driver options for the container
      --sysctl map                     Sysctl options (default map[])
      --tmpfs list                     Mount a tmpfs directory
  -t, --tty                            Allocate a pseudo-TTY
      --ulimit ulimit                  Ulimit options (default [])
  -u, --user string                    Username or UID (format: &lt;name|uid&gt;[:&lt;group|gid&gt;])
      --userns string                  User namespace to use
      --uts string                     UTS namespace to use
  -v, --volume list                    Bind mount a volume
      --volume-driver string           Optional volume driver for the container
      --volumes-from list              Mount volumes from the specified container(s)
  -w, --workdir string                 Working directory inside the container
</pre>

&nbsp;

&nbsp;

### Starting a container without any options

If we execute the docker run command without any options, the container will execute in the attached mode. The details of detached vs foreground mode can be found in the [docker reference.][1]

So in the foreground mode, <code class="highlighter-rouge">docker&lt;br />
run</code> can start the process in the container and attach the console to the process’s standard input, output, and standard error. This is not useful when you are using an application image, but only useful if you are working with an image which has _tty_ access.

&nbsp;

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~/config$ docker container run --name=web1 nginx
/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration
/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/
/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh
10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf
10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf
/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh
/docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh
/docker-entrypoint.sh: Configuration complete; ready for start up
2021/08/10 10:27:09 [notice] 1#1: using the "epoll" event method
2021/08/10 10:27:09 [notice] 1#1: nginx/1.21.1
2021/08/10 10:27:09 [notice] 1#1: built by gcc 8.3.0 (Debian 8.3.0-6)
2021/08/10 10:27:09 [notice] 1#1: OS: Linux 5.8.0-1041-aws
2021/08/10 10:27:09 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2021/08/10 10:27:09 [notice] 1#1: start worker processes
2021/08/10 10:27:09 [notice] 1#1: start worker process 31
</pre>

&nbsp;

<figure id="attachment_2519" aria-describedby="caption-attachment-2519" style="width: 640px" class="wp-caption alignnone"><img decoding="async" loading="lazy" class="wp-image-2519 size-large" src="https://dailytechlearning.com/wp-content/uploads/2021/08/Docker_Run_Without_Option-1024x208.png" alt="Docker run command in foreground mode" width="640" height="130" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/Docker_Run_Without_Option-1024x208.png 1024w, https://www.mohitkr.com/wp-content/uploads/2021/08/Docker_Run_Without_Option-300x61.png 300w, https://www.mohitkr.com/wp-content/uploads/2021/08/Docker_Run_Without_Option-768x156.png 768w, https://www.mohitkr.com/wp-content/uploads/2021/08/Docker_Run_Without_Option.png 1206w" sizes="(max-width: 640px) 100vw, 640px" /><figcaption id="caption-attachment-2519" class="wp-caption-text">Docker run command in foreground mode</figcaption></figure>

&nbsp;

### Starting a container in detached mode

The other option is to execute the docker container in the detached mode by specifying the option -d

&nbsp;

<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2520" src="http://54.206.253.95/wp-content/uploads/2021/08/2021-08-10-16_03_57-Window.png" alt="" width="656" height="35" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-10-16_03_57-Window.png 656w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-10-16_03_57-Window-300x16.png 300w" sizes="(max-width: 656px) 100vw, 656px" /> 

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~/config$ docker container run -d  --name=web2 nginx
32c97c52ac7dae6549e8f2fa14a18c506af1164775ef0a79dd6b9557906719a9
</pre>

### Starting a container in interactive mode

The -i option is used to start the container in the interactive mode , the -t option is used to enable the container terminal

&nbsp;

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~/config$ docker container run --name=test -it centos:7
[root@23ea200ab903 /]#

[root@23ea200ab903 /]#
[root@23ea200ab903 /]# echo hello
hello

[root@23ea200ab903 /]# hostname
23ea200ab903
</pre>

### Create a container ID file

This option will create a container and save the Container ID to the <code class="highlighter-rouge">cidfile</code> If the file exists already, Docker will return an error.

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~$ docker run --cidfile=file.txt --name=test1 -it centos:7
[root@d67e77099a67 /]#
 
[root@d67e77099a67 /]#
[root@d67e77099a67 /]# echo hello world
hello world
 
[root@d67e77099a67 /]# exit
exit
 
ubuntu@ip-172-31-1-61:~$ cat file.txt
d67e77099a675f874b582be4e71a282896b193fd6d6f80b44823cbacb23edbc2ubuntu@ip-172-31-1-61:~$
</pre>

### Start container at specific directory

&nbsp;

You can use the -w option to start the container with a specific directory

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:~$ docker run -w /var/www/html -it centos:7
[root@2840ac3c0278 html]#

[root@2840ac3c0278 html]# pwd
/var/www/html
[root@2840ac3c0278 html]#
</pre>

### Mounting volume

The <code class="highlighter-rouge">-v</code> flag mounts the current working directory into the container.   In this example, we will see how you can mount a directory in the container and when the file is created in the directory from inside the container, it would be found in the docker host machine as well.

<pre class="EnlighterJSRAW" data-enlighter-language="generic">ubuntu@ip-172-31-1-61:/var/www/html$ docker run  -v /var/www/html:/var/www/html -it centos:7
[root@bd4d51888937 /]#
[root@bd4d51888937 /]# ls /var/www/html
[root@bd4d51888937 /]#
[root@bd4d51888937 /]# touch /var/www/html/helloworld.txt
[root@bd4d51888937 /]# exit
exit
 
ubuntu@ip-172-31-1-61:/var/www/html$ ls
helloworld.txt
ubuntu@ip-172-31-1-61:/var/www/html$
 
</pre>

&nbsp;

<img decoding="async" loading="lazy" class="alignnone size-full wp-image-2522" src="http://54.206.253.95/wp-content/uploads/2021/08/runwith_v_option.png" alt="" width="929" height="281" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/runwith_v_option.png 929w, https://www.mohitkr.com/wp-content/uploads/2021/08/runwith_v_option-300x91.png 300w, https://www.mohitkr.com/wp-content/uploads/2021/08/runwith_v_option-768x232.png 768w" sizes="(max-width: 929px) 100vw, 929px" /> 

&nbsp;

### Publish or expose the port

You can use the option -p to expose a port and attach the port to the container

<code class="EnlighterJSRAW" data-enlighter-language="generic">docker run -d -p 80:8081/tcp nginx</code>

&nbsp;

<img decoding="async" loading="lazy" class="alignnone size-large wp-image-2523" src="https://dailytechlearning.com/wp-content/uploads/2021/08/2021-08-10-16_40_52-Window-1024x141.png" alt="" width="648" height="89" srcset="https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-10-16_40_52-Window-1024x141.png 1024w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-10-16_40_52-Window-300x41.png 300w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-10-16_40_52-Window-768x106.png 768w, https://www.mohitkr.com/wp-content/uploads/2021/08/2021-08-10-16_40_52-Window.png 1221w" sizes="(max-width: 648px) 100vw, 648px" /> 

&nbsp;

What are the other options that we can use? Please leave your feedback.

&nbsp;

[Reference][2]

 [1]: https://docs.docker.com/engine/reference/run/#detached-vs-foreground
 [2]: https://docs.docker.com/engine/reference/commandline/run/