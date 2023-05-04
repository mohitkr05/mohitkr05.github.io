---
title: Setting up Wacom Tablets with Ubuntu
author: mohit
type: post
date: 2020-11-06T13:52:06+00:00
draft: true
url: /?p=97
categories:
  - Linux

---
<p id="a1d7" class="fw fx ef fy b fz ga gb gc gd ge gf gg gh gi gj gk gl gm gn go gp cz de" data-selectable-paragraph="">
  These are the steps required to set up a Wacom tablet with Ubuntu 16.04.
</p>

<h2 id="66b0" class="gq gr ef ap gs gt gu gv gw gx gy gz ha hb hc hd he hf hg hh hi hj hk hl hm hn de" data-selectable-paragraph="">
  Install Drivers
</h2>

<p id="62c6" class="fw fx ef fy b fz ho ga gb gc hp gd ge gf hq gg gh gi hr gj gk gl hs gm gn gp cz de" data-selectable-paragraph="">
  You can find instructions to directly install or build Wacom driver for Ubuntu <a class="dh ht" href="https://help.ubuntu.com/community/Wacom/LatestDriver" rel="noopener nofollow">here</a>. This should install <code>xserver-xorg-input-wacom</code>, <code>libwacom2</code>, and <code>libwacom-common</code>. Restart your computer once the drivers are installed. Upon restarting, you’ll know that the drivers are functioning properly if it appears under USB devices.
</p>

<pre class="hz ia ib ic id ie if ig"><span id="5e74" class="de gq gr ef hy b db ih ii w ij" data-selectable-paragraph="">✦ lsusb
Bus 003 Device 002: ID 056a:0017 Wacom Co., Ltd CTE-450 [Bamboo Fun]</span></pre>

<h2 id="8789" class="gq gr ef ap gs gt gu gv gw gx gy gz ha hb hc hd he hf hg hh hi hj hk hl hm hn de" data-selectable-paragraph="">
  Configuring Driver Settings
</h2>

<p id="024c" class="fw fx ef fy b fz ho ga gb gc hp gd ge gf hq gg gh gi hr gj gk gl hs gm gn gp cz de" data-selectable-paragraph="">
  You can use the driver’s CLI to configure your tablet, stylus, eraser, and cursor. Find your devices and set the options as desired. <a class="dh ht" href="http://linuxwacom.sourceforge.net/wiki/index.php/Tablet_Configuration" rel="noopener nofollow">This</a> guide provides an overview of the basic options.
</p>

<pre class="hz ia ib ic id ie if ig"><span id="3fa8" class="de gq gr ef hy b db ih ii w ij" data-selectable-paragraph="">✦ xsetwacom --list devices
Wacom BambooFun 4x5 Pad pad      id: 10 type: PAD       
Wacom BambooFun 4x5 Pen stylus   id: 11 type: STYLUS    
Wacom BambooFun 4x5 Pen eraser   id: 18 type: ERASER    
Wacom BambooFun 4x5 Pen cursor   id: 19 type: CURSOR</span></pre>

<p id="9188" class="fw fx ef fy b fz ik ga gb gc il gd ge gf im gg gh gi in gj gk gl io gm gn gp cz de" data-selectable-paragraph="">
  For examp<span id="rmm">l</span>e, you can change the softness of your styles with the following command.
</p>

<pre class="hz ia ib ic id ie if ig"><span id="cb07" class="de gq gr ef hy b db ih ii w ij" data-selectable-paragraph="">✦ xsetwacom --set "Wacom BambooFun 4x5 Pen stylus" PressureCurve 0 20 80 100</span></pre>