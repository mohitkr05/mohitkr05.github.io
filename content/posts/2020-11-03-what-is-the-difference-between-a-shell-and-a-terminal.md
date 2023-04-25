---
title: What is the difference between a shell and a terminal?
author: mohit
type: post
date: 2020-11-03T19:09:29+00:00
draft: true
url: /?p=21
featured_image: http://www.mohitkr.com/wp-content/uploads/2020/10/aaron-burden-WFzA16YoHcI-unsplash-scaled-1.jpg
categories:
  - Linux

---
The answer to the question can be illustrated by the following screenshot.

In this screenshot, I have captured the process of my &#8220;Shell&#8221; &#8211; bash and you can see that the shell is a child process of the parent process with pid &#8211; 14398. Which if I check is the pid for the mate-terminal. So to understand this simply, shell is  invoked as the child process of a terminal emulator in the current Linux environment.

<img decoding="async" loading="lazy" class="size-full wp-image-22" src="http://dailytechlearning.com/wp-content/uploads/2020/10/Screenshot-from-2020-10-29-00-04-44.png" alt="difference between a shell and terminal" width="720" height="203" srcset="https://www.mohitkr.com/wp-content/uploads/2020/10/Screenshot-from-2020-10-29-00-04-44.png 720w, https://www.mohitkr.com/wp-content/uploads/2020/10/Screenshot-from-2020-10-29-00-04-44-300x85.png 300w" sizes="(max-width: 720px) 100vw, 720px" /> 

**Terminal**

In unix terminology, a **terminal** is a particular kind of device file which implements a number of additional commands (ioctls) beyond read and write. Nowadays the terminals, which are called pseudo-terminals or pseudo-ttys, are provided (through a thin kernel layer) by programs called **terminal emulators**. Some types of terminal emulators include:

  * GUI applications running in the <a href="http://en.wikipedia.org/wiki/X_Window_System" rel="noreferrer">X Window System</a>: <a href="http://en.wikipedia.org/wiki/Xterm" rel="noreferrer">Xterm</a>, Gnome Terminal, Konsole, Terminator, etc.
  * <a href="http://en.wikipedia.org/wiki/Gnu_screen" rel="noreferrer">Screen</a> and <a href="http://en.wikipedia.org/wiki/Tmux" rel="noreferrer">tmux</a>, which provides a layer of isolation between a program and another terminal
  * Ssh, which connects a terminal on one machine with programs on another machine
  * Expect, for scripting terminal interactions

The word _terminal_ can also have a more traditional meaning of a device through which one interacts with a computer, typically with a keyboard and display. For example an X terminal is a kind of <a href="http://en.wikipedia.org/wiki/Thin_client" rel="noreferrer">thin client</a>, a special-purpose computer whose only purpose is to drive a keyboard, display, mouse and occasionally other human interaction peripherals, with the actual applications running on another, more powerful computer.

**Shell**

A **shell** is the primary command line interface that users see to invoke other programs. This is done by providing an interface to use to &#8220;talk-to&#8221; the kernel.

There are many different unix shells. Ubuntu&#8217;s default shell is <a href="http://en.wikipedia.org/wiki/Bash_(Unix_shell)" rel="noreferrer">Bash</a> (like most other Linux distributions). Popular alternatives include <a href="http://en.wikipedia.org/wiki/Zsh" rel="noreferrer">zsh</a> (which emphasizes power and customizability) and <a href="http://en.wikipedia.org/wiki/Friendly_interactive_shell" rel="noreferrer">fish</a>

The detailed answer is mentioned in the following [stackoverflow][1] article.

 [1]: https://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line