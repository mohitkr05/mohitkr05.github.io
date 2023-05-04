---
title: Vagrant — The complete tutorial
author: mohit
type: post
date: 2023-03-28T20:37:47+00:00
url: /cloud-computing/virtualization/vagrant-the-complete-tutorial/
featured_image: http://www.mohitkr.com/wp-content/uploads/2023/03/vagrant-logo-967334594.png
ampforwp-amp-on-off:
  - default
categories:
  - Virtualization
tags:
  - vagrant
  - virtualization

---
<p id="7137">
  Vagrant is a powerful tool that allows developers to easily create and manage virtual development environments. It is an open-source tool that can be used on Windows, macOS, and Linux operating systems. With Vagrant, developers can ensure that their development environment is consistent across different machines, and can easily share and collaborate on development environments with others.
</p>

<div class="wp-block-image">
  <figure class="aligncenter size-large"><img decoding="async" loading="lazy" width="1024" height="601" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-10-1024x601.png" alt="" class="wp-image-2926" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-10-1024x601.png 1024w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-10-300x176.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-10-768x451.png 768w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-10.png 1094w" sizes="(max-width: 1024px) 100vw, 1024px" /><figcaption class="wp-element-caption">Vagrant components</figcaption></figure>
</div>

<p id="6a15">
  One of the key features of Vagrant is its ability to create and manage virtual machines (VMs). A virtual machine is a software-based simulation of a physical computer. With Vagrant, developers can create and configure virtual machines, which can be useful for testing and development purposes.
</p>

<p id="cc1a">
  Vagrant can be used in conjunction with other tools such as VirtualBox, VMware, and Hyper-V, to create and manage virtual machines. Once a virtual machine is created, developers can then use Vagrant to provision and configure the virtual machine. This can include installing software, configuring settings, and running scripts.
</p>

<p id="7a49">
  One of the most powerful features of Vagrant is its ability to share and collaborate in development environments. Vagrant allows developers to share their development environment in the form of a “<em>Vagrantfile</em>”.
</p>

<p id="7a49">
  A Vagrantfile is a script that contains all the necessary information to create and configure a virtual machine. This means that other developers can easily reproduce the same development environment, ensuring consistency across different machines.
</p>

<p id="a1e8">
  Vagrant can also be integrated with other tools such as Ansible, Chef, and Puppet for further automation of development environment provisioning and configuration. This can save time and reduce the chance of errors when setting up development environments.
</p>

<p id="455c">
  To get started with Vagrant, you’ll first need to download and install it from the official website (<a class="ax wv" href="https://www.vagrantup.com/downloads.html" target="_blank" rel="noopener ugc nofollow">https://www.vagrantup.com/downloads.html</a>).
</p>

If you are looking for a complete course you can subscribe to this course.

`<div class="ufwp"><div class="ufwp-standard"><div class="ufwp-course ufwp-course--sale" data-ufwp-course-id="5080200"><a class="ufwp-course__link" href="https://www.udemy.com/course/vagrant-the-ultimate-course/" target="_blank" rel="nofollow" title="Vagrant - A hands-on course"><span class="ufwp-course__img"><img src="https://img-c.udemycdn.com/course/480x270/5080200_7247.jpg" alt="Vagrant - A hands-on course"></span><span class="ufwp-course__content"><span class="ufwp-course__title">Vagrant - A hands-on course</span><span class="ufwp-course__instructors">Mohit Kumar, 12 years experience in Solution Design and Architecture</span><span class="ufwp-course__headline">Use Vagrant to spin Virtual Machines, write Vagrantfiles and understand usage of Vagrant boxes and plugins</span><span class="ufwp-course__footer"><span class="ufwp-course__price ufwp-course__price--list">A$26.99</span><span class="ufwp-course__price">A$19.99</span><span class="ufwp-course__rating"><span class="ufwp-star-rating"><span style="width: 100%;"></span></span> 5 (3 ratings)</span></span></span></a></div></div></div>`

## Installation  {.wp-block-heading}

### Windows {.wp-block-heading}

  1. Visit the Vagrant downloads page at <a href="https://www.vagrantup.com/downloads.html" target="_blank" rel="noreferrer noopener">https://www.vagrantup.com/downloads.html</a>
  2. Scroll down to the Windows section and select the appropriate installer for your system, either 32-bit or 64-bit.
  3. Once the download is complete, double-click the installer to begin the installation process.
  4. Follow the prompts in the installation wizard to complete the installation. The default installation location is usually fine, but you can choose a custom location if you prefer.
  5. After the installation is complete, open the Command Prompt by pressing the Windows key + R, typing &#8220;cmd&#8221; and pressing Enter.
  6. In the Command Prompt, type &#8220;vagrant&#8221; and press Enter. This will confirm that Vagrant has been installed correctly.

### Linux &#8211; Debian {.wp-block-heading}

  1. Open a terminal window by pressing Ctrl + Alt + T.
  2. Update your system&#8217;s package list by running the following commands: 

<pre class="wp-block-code"><code>sudo apt update
sudo apt install -y software-properties-common apt-transport-https curl

curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo add-apt-repository "deb &#091;arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"

sudo apt update

sudo apt install vagrant

vagrant --version</code></pre>

<p id="455c">
  Once Vagrant is installed, you’ll need to install a provider, such as VirtualBox, VMware, or Hyper-V. Once you have Vagrant and a provider installed, you can use the following command to create a new virtual machine
</p>

<div class="wp-block-image">
  <figure class="aligncenter size-full"><img decoding="async" loading="lazy" width="879" height="696" src="https://www.mohitkr.com/wp-content/uploads/2023/04/image-11.png" alt="" class="wp-image-2928" srcset="https://www.mohitkr.com/wp-content/uploads/2023/04/image-11.png 879w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-11-300x238.png 300w, https://www.mohitkr.com/wp-content/uploads/2023/04/image-11-768x608.png 768w" sizes="(max-width: 879px) 100vw, 879px" /><figcaption class="wp-element-caption">Vagrant state machine</figcaption></figure>
</div>



<pre class="wp-block-preformatted"><span id="dae0" class="abv abw yg abs b bv abx aby y abz aca" data-selectable-paragraph="">vagrant <span class="hljs-keyword">init</span></span></pre>

<p id="c859">
  This command will create a new Vagrantfile in the current directory. You can then edit the Vagrantfile to configure the virtual machine to your liking. Once you have finished configuring the Vagrantfile, you can use the following command to start the virtual machine:
</p>

<pre class="wp-block-preformatted"><span id="fdc4" class="abv abw yg abs b bv abx aby y abz aca" data-selectable-paragraph="">vagrant up</span></pre>

<p id="7293">
  This command will start the virtual machine and provision it according to the settings in the Vagrantfile. To connect to the virtual machine, you can use the following command:
</p>

<pre class="wp-block-preformatted"><span id="cb8c" class="abv abw yg abs b bv abx aby y abz aca" data-selectable-paragraph="">vagrant ssh</span></pre>

<p id="7c0e">
  When you&#8217;re finished working with the virtual machine, you can use the following command to stop it:
</p>

<pre class="wp-block-preformatted"><span id="a1df" class="abv abw yg abs b bv abx aby y abz aca" data-selectable-paragraph="">vagrant halt</span></pre>

<p id="a280">
  And if you don&#8217;t need the virtual machine anymore, you can use the following command to destroy it:
</p>

<pre class="wp-block-preformatted"><span id="6406" class="abv abw yg abs b bv abx aby y abz aca" data-selectable-paragraph="">vagrant destroy</span></pre>

## Vagrantfile {.wp-block-heading}



A Vagrantfile is a configuration file used by Vagrant, a tool for managing and creating virtual machine environments. The Vagrantfile contains all the instructions necessary to create and configure a virtual machine (VM) according to specific requirements.

The Vagrantfile is essentially a Ruby script that defines the settings for a VM, including its base box (which specifies the operating system and software), the amount of RAM and CPU allocated to the VM, network settings, shared folders, and any additional software to be installed.

By specifying all these settings in the Vagrantfile, Vagrant can easily create and configure a new VM with a single command, allowing developers to quickly set up and tear down development environments. The Vagrantfile can also be version-controlled and shared with other developers, ensuring consistency and reproducibility of development environments.

<pre class="wp-block-code"><code>VAGRANT_API_VERSION = "2"

servers = &#091;
  {:hostname => "node1", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 1"},
  {:hostname => "node2", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 2"},
  {:hostname => "node3", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 3"}
]

Vagrant.configure(VAGRANT_API_VERSION) do |config|

  servers.each do |server|

    config.vm.define server&#091;:hostname] do |nodeconfig|

      nodeconfig.vm.box = server&#091;:box]
      nodeconfig.vm.hostname = server&#091;:hostname]
      nodeconfig.vm.post_up_message = server&#091;:message]
        nodeconfig.vm.provider "virtualbox" do |vb|
          # Display the VirtualBox GUI when booting the machine
          vb.gui = true
          # Customize the amount of memory on the VM:
          vb.memory = server&#091;:memory]
          vb.cpus = server&#091;:cpus]
          vb.customize &#091;"modifyvm", :id, "--nic2", "natnetwork", "--nat-network2", "NatNetwork"]
          # vb.customize &#091;"modifyvm", :id, "--memory", "2048"]
          # vb.customize &#091;"modifyvm", :id, "--cpus", "2"]
        end
      end

  end
end

VAGRANT_API_VERSION = "2"

servers = &#091;
  {:hostname => "node1", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 1"},
  {:hostname => "node2", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 2"},
  {:hostname => "node3", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 3"}
]

Vagrant.configure(VAGRANT_API_VERSION) do |config|

  servers.each do |server|

    config.vm.define server&#091;:hostname] do |nodeconfig|

      nodeconfig.vm.box = server&#091;:box]
      nodeconfig.vm.hostname = server&#091;:hostname]
      nodeconfig.vm.post_up_message = server&#091;:message]
        nodeconfig.vm.provider "virtualbox" do |vb|
          # Display the VirtualBox GUI when booting the machine
          vb.gui = true
          # Customize the amount of memory on the VM:
          vb.memory = server&#091;:memory]
          vb.cpus = server&#091;:cpus]
          vb.customize &#091;"modifyvm", :id, "--nic2", "natnetwork", "--nat-network2", "NatNetwork"]
          # vb.customize &#091;"modifyvm", :id, "--memory", "2048"]
          # vb.customize &#091;"modifyvm", :id, "--cpus", "2"]
        end
      end

  end
end

VAGRANT_API_VERSION = "2"

servers = &#091;
  {:hostname => "node1", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 1"},
  {:hostname => "node2", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 2"},
  {:hostname => "node3", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 3"}
]

Vagrant.configure(VAGRANT_API_VERSION) do |config|

  servers.each do |server|

    config.vm.define server&#091;:hostname] do |nodeconfig|

      nodeconfig.vm.box = server&#091;:box]
      nodeconfig.vm.hostname = server&#091;:hostname]
      nodeconfig.vm.post_up_message = server&#091;:message]
        nodeconfig.vm.provider "virtualbox" do |vb|
          # Display the VirtualBox GUI when booting the machine
          vb.gui = true
          # Customize the amount of memory on the VM:
          vb.memory = server&#091;:memory]
          vb.cpus = server&#091;:cpus]
          vb.customize &#091;"modifyvm", :id, "--nic2", "natnetwork", "--nat-network2", "NatNetwork"]
          # vb.customize &#091;"modifyvm", :id, "--memory", "2048"]
          # vb.customize &#091;"modifyvm", :id, "--cpus", "2"]
        end
      end

  end
end

VAGRANT_API_VERSION = "2"

servers = &#091;
  {:hostname => "node1", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 1"},
  {:hostname => "node2", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 2"},
  {:hostname => "node3", :cpus => 1, :memory => 512, :box=> "centos/7" , :message=> "custom message for vm 3"}
]

Vagrant.configure(VAGRANT_API_VERSION) do |config|

  servers.each do |server|

    config.vm.define server&#091;:hostname] do |nodeconfig|

      nodeconfig.vm.box = server&#091;:box]
      nodeconfig.vm.hostname = server&#091;:hostname]
      nodeconfig.vm.post_up_message = server&#091;:message]
        nodeconfig.vm.provider "virtualbox" do |vb|
          # Display the VirtualBox GUI when booting the machine
          vb.gui = true
          # Customize the amount of memory on the VM:
          vb.memory = server&#091;:memory]
          vb.cpus = server&#091;:cpus]
          vb.customize &#091;"modifyvm", :id, "--nic2", "natnetwork", "--nat-network2", "NatNetwork"]
          # vb.customize &#091;"modifyvm", :id, "--memory", "2048"]
          # vb.customize &#091;"modifyvm", :id, "--cpus", "2"]
        end
      end

  end
end
</code></pre>