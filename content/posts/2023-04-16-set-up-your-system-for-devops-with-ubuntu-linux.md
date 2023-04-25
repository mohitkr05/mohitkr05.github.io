---
title: Set up your system for DevOps with Ubuntu Linux
author: mohit
type: post
date: 2023-04-16T10:29:46+00:00
url: /general/set-up-your-system-for-devops-with-ubuntu-linux/
featured_image: http://www.mohitkr.com/wp-content/uploads/2023/04/image-36.png
categories:
  - Development
  - General
tags:
  - AWS
  - development tools
  - initial pc configuration
  - LIGHTSAIL
  - system setup
  - tools
  - vagrant
  - virtualization
  - WORDPRESS

---
In today&#8217;s fast-paced software development world, DevOps has become an essential approach for creating, testing and delivering software products at a rapid pace. To set up your system for DevOps, you need to have the right tools and applications installed on your system. Setting up your system for DevOps is a crucial step in the software development process, as it can save you time and improve your productivity. In this guide, we will explore the essential tools and applications that you need to install required tools on your system to set it up for DevOps, including development tools, automation tools, and other software applications. With these tools in place, you&#8217;ll be ready to start building and delivering high-quality software products with the speed and efficiency of DevOps.

This is continuation to my previous post of [setting my system for Development][1]

## <a href="https://git-scm.com/" target="_blank" rel="noopener nofollow" title="">Git</a> {.wp-block-heading}

Git is a free and open-source distributed version control system that was created by Linus Torvalds in 2005. It was designed to be fast, efficient, and scalable, making it ideal for managing both small and large software development projects.

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="739" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-34-1024x739.png" alt="" class="wp-image-3002" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-34-1024x739.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-34-300x216.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-34-768x554.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-34.png 1074w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

Git allows developers to track changes in source code, collaborate with others, and maintain a history of project revisions. It accomplishes this by allowing multiple users to work on the same codebase simultaneously, while also providing a system for managing changes to the codebase and reconciling any conflicts that may arise.

To Install git you can use the apt package manager with the following command.

<pre class="wp-block-code"><code>sudo apt-get install git</code></pre>

<div class="wp-block-image">
  <figure class="aligncenter size-full"><img decoding="async" loading="lazy" width="800" height="440" src="http://www.mohitkr.com/wp-content/uploads/2023/04/image-30.png" alt="" class="wp-image-2995" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-30.png 800w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-30-300x165.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-30-768x422.png 768w" sizes="(max-width: 800px) 100vw, 800px" /></figure>
</div>

One of the main advantages of Git is its ability to create and manage branches, which allows developers to experiment with new features and ideas without affecting the main codebase. Git also provides a robust set of tools for merging and integrating these changes back into the main codebase, enabling teams to work together effectively on complex software projects.



This is the first step in setting up your system for DevOps.

## <a href="http://ohmyz.sh/" target="_blank" rel="noopener" title="oh-my-zsh">oh-my-zsh</a> {.wp-block-heading}

oh-my-zsh is an open-source framework for managing the Zsh shell. It was created by Robby Russell in 2009 and has since become one of the most popular Zsh frameworks available. Oh My Zsh is designed to make it easy to configure and customize your Zsh shell, with a range of plugins, themes, and settings that can be easily added and managed.

One of the main advantages of Oh My Zsh is its extensive library of plugins, which can be used to add additional functionality and features to your Zsh shell. These plugins cover a wide range of use cases, from auto-completion and syntax highlighting to Git integration and custom aliases.

In addition to its plugins, Oh My Zsh also includes a range of customizable themes that can be used to change the look and feel of your Zsh shell. Themes can be easily installed and customized, allowing you to create a personalized and professional-looking shell environment.

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="599" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-35-1024x599.png" alt="oh-my-zsh home page" class="wp-image-3003" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-35-1024x599.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-35-300x175.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-35-768x449.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-35.png 1318w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

Oh My Zsh is also highly customizable, with a range of settings and options that can be adjusted to suit your specific needs and preferences. Whether you&#8217;re a novice user or an experienced developer, Oh My Zsh offers a powerful and flexible framework for managing your Zsh shell and enhancing your productivity.

To Install oh-my-zsh you can follow these steps, you need to have curl and zsh before you can install oh-my-zsh

<pre class="wp-block-code"><code>sudo apt-get install curl zsh

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
</code></pre>

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="526" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-32-1024x526.png" alt="" class="wp-image-3000" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-32-1024x526.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-32-300x154.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-32-768x394.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-32-1536x788.png 1536w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-32.png 1547w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

## <a href="https://docs.docker.com/" target="_blank" rel="noopener" title="">Docker</a> {.wp-block-heading}

Docker is an open-source containerization platform that is designed to make it easier to create, deploy, and run applications in a variety of environments. It was created in 2013 and has since become one of the most popular tools for containerization.

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="444" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-36-1024x444.png" alt="Docker homepage" class="wp-image-3010" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-36-1024x444.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-36-300x130.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-36-768x333.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-36-1536x666.png 1536w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-36.png 1662w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

Docker enables developers to package their applications and dependencies into self-contained, portable containers, which can be run on any system that supports Docker. These containers are lightweight, fast, and secure, making them ideal for use in cloud environments, as well as in local development and testing.

One of the key advantages of Docker is its ability to simplify the deployment and management of applications. With Docker, developers can create a containerized application once, and then deploy it across multiple environments, without having to worry about compatibility issues or configuration differences.

Installation of Docker in Linux use the following command in Ubuntu Linux

<pre class="wp-block-code"><code>sudo apt-get install containerd docker docker-compose</code></pre>

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="365" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-37-1024x365.png" alt="Installing Docker on Ubuntu" class="wp-image-3011" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-37-1024x365.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-37-300x107.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-37-768x274.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-37-1536x547.png 1536w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-37.png 1675w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="502" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-38-1024x502.png" alt="Docker cli on Ubuntu" class="wp-image-3013" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-38-1024x502.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-38-300x147.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-38-768x376.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-38-1536x752.png 1536w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-38.png 1860w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

## <a href="https://www.virtualbox.org/" target="_blank" rel="noopener" title="VirtualBox">VirtualBox</a> {.wp-block-heading}

VirtualBox is a free and open-source virtualization software that allows users to run multiple operating systems on a single computer. It was created by Oracle Corporation in 2007 and has since become one of the most popular virtualization tools available.

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="435" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-39-1024x435.png" alt="VirtualBox homepage" class="wp-image-3017" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-39-1024x435.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-39-300x128.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-39-768x326.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-39-1536x653.png 1536w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-39.png 1715w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

VirtualBox works by creating a virtual environment in which you can install and run multiple operating systems, including Windows, Linux, and macOS. This virtual environment is isolated from your host operating system, which means that any changes or modifications you make to your virtual environment will not affect your host operating system.

<div class="wp-block-image">
  <figure class="aligncenter size-full"><img decoding="async" loading="lazy" width="963" height="577" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-40.png" alt="" class="wp-image-3018" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-40.png 963w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-40-300x180.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-40-768x460.png 768w" sizes="(max-width: 963px) 100vw, 963px" /></figure>
</div>

One of the main advantages of VirtualBox is its versatility. It can be used for a wide range of applications, from testing software and developing applications to running legacy software and experimenting with new operating systems. With VirtualBox, you can create and manage virtual machines with ease, allowing you to run multiple operating systems simultaneously and switch between them with just a few clicks.

To install VirtualBox, I am going to follow these steps

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="274" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-41-1024x274.png" alt="VirtualBox Installation" class="wp-image-3020" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-41-1024x274.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-41-300x80.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-41-768x206.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-41-1536x412.png 1536w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-41.png 1888w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

  * Add the following line to the /etc/apt/sources.list

<pre class="wp-block-code"><code>deb &#91;arch=amd64 signed-by=/usr/share/keyrings/oracle-virtualbox-2016.gpg] https://download.virtualbox.org/virtualbox/debian jammy contrib</code></pre>

  * Download the public key and install it

<pre class="wp-block-code"><code>wget -O- https://www.virtualbox.org/download/oracle_vbox_2016.asc | sudo gpg --dearmor --yes --output /usr/share/keyrings/oracle-virtualbox-2016.gpg</code></pre>

  * Install VirtualBox

<pre class="wp-block-code"><code>sudo apt-get update
sudo apt-get install virtualbox-6.1</code></pre>

## <a href="https://www.vagrantup.com/" target="_blank" rel="noopener" title="Vagrant">Vagrant</a> {.wp-block-heading}

Vagrant is a popular open-source tool that is used for creating and managing virtual development environments. It was first released in 2010 by Mitchell Hashimoto and has since become a key tool for software developers and IT professionals alike.

Vagrant works by automating the creation and configuration of virtual machines, allowing developers to easily create and manage their development environments with ease. With Vagrant, developers can define their development environment in a simple configuration file, which can be easily shared and replicated across multiple systems.

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="474" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-42-1024x474.png" alt="vagrant home page" class="wp-image-3022" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-42-1024x474.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-42-300x139.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-42-768x356.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-42.png 1497w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

One of the main advantages of Vagrant is its flexibility. It supports a wide range of virtualization providers, including VirtualBox, VMware, and Hyper-V, allowing developers to choose the best virtualization platform for their specific needs. Vagrant also supports a wide range of operating systems, including Linux, Windows, and macOS, making it a versatile tool for developers working in different environments.

Use the following links to install Vagrant on your Linux box.

<pre class="wp-block-code"><code>wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb &#91;signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install vagrant</code></pre>

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="516" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-43-1024x516.png" alt="" class="wp-image-3023" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-43-1024x516.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-43-300x151.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-43-768x387.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-43-1536x775.png 1536w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-43.png 1755w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

## <a href="https://www.wireshark.org/" target="_blank" rel="noopener" title="Wireshark">Wireshark</a> {.wp-block-heading}

Wireshark is a free and open-source network protocol analyzer that allows users to capture, analyze, and troubleshoot network traffic. It was first released in 1998 as Ethereal, but was later renamed to Wireshark in 2006.

Wireshark works by capturing packets of network data and displaying them in a user-friendly interface. It supports a wide range of protocols, including Ethernet, Wi-Fi, TCP/IP, and HTTP, making it a versatile tool for network administrators and security professionals.

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="417" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-44-1024x417.png" alt="wireshark homepage" class="wp-image-3024" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-44-1024x417.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-44-300x122.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-44-768x313.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-44-1536x626.png 1536w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-44.png 1691w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

One of the main advantages of Wireshark is its ability to help troubleshoot network problems. With Wireshark, network administrators can quickly identify and isolate network issues, such as misconfigured routers, network congestion, or security breaches. Wireshark also provides a range of advanced features, such as the ability to filter and analyze network traffic, making it a powerful tool for network analysis and optimization.

Installation is simple, you just need to install Wireshark, tshark and Tcpdump

<pre class="wp-block-code"><code>sudo apt-get install wireshark tshark tcpdump</code></pre>

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="682" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-45-1024x682.png" alt="" class="wp-image-3025" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-45-1024x682.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-45-300x200.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-45-768x511.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-45.png 1439w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

This step is essential in setting up your system for DevOps as networking is a key factor of DevOps and as a DevOps engineer, you need to be aware of how the network is performing.

## <a title="Python" href="https://www.python.org/" target="_blank" rel="noopener">Python</a> {.wp-block-heading}

Python is a popular high-level programming language that is widely used in a variety of industries and applications. Created in the late 1980s by Guido van Rossum, Python has since become one of the most popular programming languages in the world, with a large and active community of developers and users.

One of the main advantages of Python is its simplicity and ease of use. Its clear and concise syntax makes it easy to read and write, making it an ideal choice for beginners and experienced developers alike. Python also has a vast standard library, which includes a wide range of modules and tools that can be used to develop a wide range of applications, from web development to scientific computing.

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="656" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-47-1024x656.png" alt="" class="wp-image-3028" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-47-1024x656.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-47-300x192.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-47-768x492.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-47.png 1304w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

Another advantage of Python is its versatility. It can be used for a wide range of applications, from building desktop applications and web applications to data analysis and machine learning. Python also has a range of third-party libraries and frameworks, such as Django, Flask, NumPy, and TensorFlow, which can be used to extend its functionality and support a wide range of use cases.

Python3 is already installed with the latest releases of Ubuntu

Python is also highly portable, with versions available for all major operating systems, including Windows, Linux, and macOS. Its ease of use, versatility, and portability have made it a popular choice for developers and organizations of all sizes, making Python an essential tool for many different industries and applications.

<pre class="wp-block-code"><code>sudo apt-get install python3 python3-pip
</code></pre>

<div class="wp-block-image">
  <figure class="aligncenter size-full"><img decoding="async" loading="lazy" width="819" height="410" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-48.png" alt="" class="wp-image-3029" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-48.png 819w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-48-300x150.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-48-768x384.png 768w" sizes="(max-width: 819px) 100vw, 819px" /></figure>
</div>

Python plays a key factor in the automation of the system and thus it is must-have in setting up your system for DevOps.

## <a title="" href="https://www.ansible.com/" target="_blank" rel="noopener">Ansible</a> {.wp-block-heading}

Ansible is an open-source IT automation tool that is designed to simplify the deployment and management of software and infrastructure. It was created by Michael DeHaan in 2012 and has since become one of the most popular automation tools available.

Ansible works by using simple YAML-based configuration files to define tasks and workflows, making it easy for developers and IT professionals to automate complex processes. It can be used to automate a wide range of tasks, including software deployment, configuration management, and infrastructure provisioning.

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="421" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-46-1024x421.png" alt="ansible homepage" class="wp-image-3026" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-46-1024x421.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-46-300x123.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-46-768x316.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-46.png 1492w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

One of the main advantages of Ansible is its simplicity. It does not require any special agents or software to be installed on remote systems and can be easily configured and managed from a central control node. This makes it a highly scalable and flexible tool for managing large and complex environments.

To Install Ansible, follow these steps

<pre class="wp-block-code"><code>python3 -m pip install --user ansible</code></pre>

## <a href="https://www.terraform.io/" target="_blank" rel="noopener" title="">Terraform</a> {.wp-block-heading}

Terraform is an open-source infrastructure-as-code tool that is designed to automate the provisioning, deployment, and management of cloud-based infrastructure. Created by HashiCorp in 2014, Terraform has become a popular tool for DevOps engineers, cloud architects, and IT professionals.

<div class="wp-block-image">
  <figure class="aligncenter size-full"><img decoding="async" loading="lazy" width="640" height="275" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-50.png" alt="" class="wp-image-3062" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-50.png 640w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-50-300x129.png 300w" sizes="(max-width: 640px) 100vw, 640px" /></figure>
</div>

Terraform works by defining infrastructure as code, which allows developers to easily manage complex cloud environments using simple configuration files. With Terraform, users can define and manage infrastructure resources, such as virtual machines, networks, and storage, across a wide range of cloud providers, including AWS, Azure, and Google Cloud Platform.

<div class="wp-block-image">
  <figure class="aligncenter size-full"><img decoding="async" loading="lazy" width="640" height="270" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-49.png" alt="" class="wp-image-3061" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-49.png 640w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-49-300x127.png 300w" sizes="(max-width: 640px) 100vw, 640px" /></figure>
</div>

One of the main advantages of Terraform is its ability to provide a single, unified interface for managing cloud infrastructure. This enables users to manage complex cloud environments more efficiently and effectively, without the need for multiple tools or platforms.

Terraform also provides a range of advanced features, such as support for version control, testing, and automation, making it a powerful tool for managing cloud infrastructure at scale. Whether you&#8217;re a DevOps engineer, cloud architect, or IT professional, Terraform is a versatile and reliable tool that can help you automate and streamline your cloud infrastructure management.

To install Terraform use the following commands

<pre class="wp-block-code"><code>wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb &#91;signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform</code></pre>

## <a href="https://aws.amazon.com/cli/" target="_blank" rel="noopener" title="">AWS CLI</a> {.wp-block-heading}

The AWS Command Line Interface (CLI) is an open-source tool that allows developers and IT professionals to interact with Amazon Web Services (AWS) from the command line. Created by Amazon in 2013, the AWS CLI has become a popular tool for managing and automating AWS services.

The AWS CLI works by providing a simple, unified interface for interacting with AWS services, making it easy to manage and automate AWS resources from the command line. With the AWS CLI, users can perform a wide range of tasks, such as creating and managing EC2 instances, managing S3 buckets, and configuring IAM policies.

One of the main advantages of the AWS CLI is its flexibility. It can be used on a wide range of platforms, including Windows, macOS, and Linux, and can be easily integrated with other command line tools and scripts. This makes it a highly versatile tool for managing and automating AWS services.

<pre class="wp-block-code"><code># Download the awscliv2.zip
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

# unzip the package
unzip awscliv2.zip

# run the install script
sudo ./aws/install

# Check the version
aws --version</code></pre>

## VS Code & VIM {.wp-block-heading}

**VS Code**

Visual Studio Code is a lightweight but powerful source code editor which runs on your desktop and is available for Windows, macOS and Linux. It comes with built-in support for JavaScript, TypeScript and Node.js and has a rich ecosystem of extensions for other languages and runtimes (such as C++, C#, Java, Python, PHP, Go, .NET)

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="793" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-28-1024x793.png" alt="VS code splash screen" class="wp-image-2991" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-28-1024x793.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-28-300x232.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-28-768x594.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-28.png 1031w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

To install VS code download the package and install it. You can use the dpkg command to install the package manager.

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="145" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-27-1024x145.png" alt="Installing VScode" class="wp-image-2990" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-27-1024x145.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-27-300x43.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-27-768x109.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-27.png 1249w" sizes="(max-width: 1024px) 100vw, 1024px" /></figure>
</div>

**Vim**

Vim is a highly configurable, open-source text editor that is known for its speed, efficiency, and versatility. Originally released in 1991, Vim is a descendant of the popular Vi editor and is designed to work in a terminal environment, making it ideal for use on servers or other systems without graphical interfaces.

<div class="wp-block-image">
  <figure class="aligncenter size-full"><img decoding="async" loading="lazy" width="800" height="403" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-29.png" alt="" class="wp-image-2993" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-29.png 800w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-29-300x151.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-29-768x387.png 768w" sizes="(max-width: 800px) 100vw, 800px" /></figure>
</div>

One of the things that sets Vim apart from other text editors is its extensive range of keyboard shortcuts and commands. These shortcuts allow experienced Vim users to navigate, edit, and manipulate text with incredible speed and precision, often without ever having to take their hands off the keyboard.

Another key feature of Vim is its high level of configuration. Users can customize the editor to suit their specific needs and preferences, from changing the appearance of the interface to defining their own key mappings and commands.

<pre class="wp-block-code"><code>sudo apt-get install vim</code></pre>

Despite its initial learning curve, Vim has developed a passionate following among developers, sysadmins, and other power users who value its speed, efficiency, and customizability. Whether you’re working on a remote server or just looking for a powerful text editor that can keep up with your workflow, Vim is definitely worth considering.

## Conclusion {.wp-block-heading}

In conclusion, setting up your system for DevOps can greatly improve your productivity and efficiency as a developer or IT professional. By installing the right tools and software, you can streamline your development workflows, automate repetitive tasks, and manage your infrastructure more effectively.

From version control systems like Git to automation tools like Ansible, there are many open-source tools available that can help you simplify and optimize your DevOps workflows. By choosing the right tools for your needs and customizing your Ubuntu system accordingly, you can create a powerful and efficient development environment that meets your specific requirements.

So, whether you&#8217;re just getting started with DevOps or looking to improve your existing workflows, be sure to take the time to set up your Ubuntu system with the right tools and software. With the right setup, you can streamline your development processes, reduce your workload, and achieve greater success in your projects.

 [1]: https://www.mohitkr.com/development/setting-up-my-new-pc-with-ubuntu-as-my-primary-development-workstation/